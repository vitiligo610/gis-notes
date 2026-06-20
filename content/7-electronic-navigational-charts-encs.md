---
title: 7. Electronic Navigational Charts (ENCs)
---
## Introduction to ENCs and the IHO
Electronic Navigational Charts (ENC) are vector data sets that support all types of marine navigation.  When building marine navigation software, you cannot simply use standard web-mapping tiles (like Google Maps or standard GeoJSON). Commercial and recreational marine navigation relies on highly regulated, legally certified chart data.

* **IHO (International Hydrographic Organization):** The global intergovernmental body that sets the rules and standards for marine cartography and navigation.
* **ENC (Electronic Navigational Chart):** An official, standardized **vector** database containing all the chart information necessary for safe navigation. 
* **Vector vs. Raster:** Unlike paper chart scans (rasters), ENCs are vector-based. This means every buoy, depth contour, and landmass is stored as a mathematical object (point, line, or polygon) with associated metadata. This allows the software to trigger alarms (e.g., "Warning: Shallow water ahead") which is impossible with raster images.

![[Pasted image 20260620115302.png]]
## S-57: The Data Standard
**S-57** is the legacy - but currently globally ubiquitous - IHO standard for the exchange of digital hydrographic data. Marine software must be capable of parsing S-57 files.

The following are the core concepts of S-57 Standard:
* **Object-Oriented:** Everything on the map is a "Feature Object" or a "Spatial Object."
    *   *Spatial Objects:* The actual geometry (a point coordinate, a line, an area).
    *   *Feature Objects:* The real-world meaning of that geometry (e.g., a "Light", a "Buoy", a "Depth Area").
* **Attributes:** Every feature has attributes. A buoy might have attributes for its shape, color, and radar reflectivity.
* **Cells (Files):** S-57 data is distributed in files called "Cells" (usually with a `.000` file extension). A cell covers a specific rectangular geographic area at a specific navigational purpose (scale).
* **ISO 8211:** Under the hood, S-57 files are encoded using an old, complex binary format called ISO 8211. 

> [!Tip]
> Writing an ISO 8211 parser from scratch is notoriously difficult. Most modern marine engines utilize existing libraries (like `GDAL`/`OGR`) to decode S-57 into more manageable formats like GeoJSON or SQLite databases before processing.
## S-52: The Presentation Standard
While S-57 dictates *what* the data is, **S-52** dictates exactly *how it must be drawn on the screen*. 

Because marine navigation is safety-critical, a UI developer cannot just pick arbitrary colors or icons for map features. 
* **Standardized Symbology:** S-52 provides a massive library of very specific vector symbols, line styles, and color palettes that must be used.
* **Conditional Rendering rules:** The way an object is drawn changes based on user settings and context. 
    * *Example:* A depth contour line might be drawn differently depending on the ship's current draft (depth in the water) set by the captain.
* **Color Palettes (Day/Dusk/Night):** S-52 requires software to support different color schemes to protect the mariner's night vision. The exact RGB values for every single pixel color are strictly defined by the IHO.
## S-100: The Modern Framework
S-57 is rigid, difficult to update, and limited strictly to 2D chart data. The IHO has developed **S-100** as the modern replacement, based on modern ISO geospatial standards (ISO 19100 series).
### Why S-100 is important:
* **Extensibility:** It is not just one standard, but a framework. It allows for "plug-and-play" data models.
*   **Beyond Base Maps:** S-100 supports dynamic, multi-dimensional data. 
    * **S-101:** The new standard for the vector ENCs (replacing S-57).
    * **S-102:** High-resolution 3D bathymetry (underwater terrain).
    * **S-104:** Water level/Tidal data.
    * **S-111:** Surface currents.    
## Security: S-63 Encryption
Commercial ENCs are not free; they are sold by hydrographic offices. To prevent piracy, the IHO created the **S-63** standard.
* S-63 is simply S-57 data that has been encrypted and digitally signed.
* To read S-63 charts, your software requires specific decryption keys (User Permits and Cell Permits) and must be registered with an IHO scheme administrator. 

## References
- Introduction to Electronic Chart Systems and ECDIS | https://www.iho-ohi.net/english/about-encs/enc-production/general.html
- IHO Standards & Specifications | https://iho.int/en/standards-and-specifications
- IHO Publications | https://docs.iho.int/iho_pubs/IHO_Download.htm