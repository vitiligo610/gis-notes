---
title: 6. Understanding Spatial Data
---
## Composition of a GIS dataset
A GIS dataset is basically made up of three things:
### 1. Building Blocks
- Building blocks, aka Entities, represent the object we are mapping.
- They could be points, lines or pixels in an image.
- There are different types of entities that are good at representing different types of features.
### 2. Attributes
- Attributes provide information about the object.
- They can be as simple as different colors representing different features.
- And they can be as complex as a table of information.
### 3. Spatial Relationship
- This defines the relationships objects have with each other, aka topology.
- This allows us to analyze our data and be able to tell which points fall in which area.
- They are especially important for networks e.g. roads, rivers, etc.

## Types of Data
There are mainly two data types that are used to represent GIS data. Each of them has its own benefits.
### 1. Raster Data Model
- In simplest terms, raster formats are like digital image files.
- It consists of regular grid of cells that covers the area of intent.
- Each cell is a pixel.
- The resolution of raster data refers to how much area each pixel covers e.g 1m^2
- **Pros:** In GIS, it is very good for storing continuous attributes, e.g. elevation, pollution, height crime level.
- **Cons**: It is bad for storing discrete objects e.g. buildings. Plus it can't handle complex attributes.

There are various file formats used to store raster data. Some of them are: TIFF, JPEG, PNG, IMG, PCI, PCX, ECW.

![[Pasted image 20260619223907.png]]

### 2. Vector Grid Model
- For a vector data model, data is made up of coordinate pairs with labels instead of pixels.
- There are three key elements for a vector model: point, line, and polygon (area).
	- Points join to create lines. Lines join to form a polygon or cover an area
- One must keep in mind that these coordinates are always precise although they may not be accurate.
- For vector data, attributes are stored in a separate vector attribute table, like a spreadsheet.
	- Each row represents a single feature
	- and it can have many columns with different types of data (see image below)
- **Pros:** It is really good for showing individual features, but difficult to show continuous data (although contour lines can be used for continuous data). It can also handle complex attributes really well. Features can connect as well overlap on top of each other.
- **Cons:** It may give impression of precision.

There are a number of file formats used for vector data such as SHP (shape files), GPKG, GeoJSON, GML, and many more.

![[Pasted image 20260619223803.png]]

### 3. Other Data Types
There are other less common but more specialized data formats such as Triangular irregular networks and Unstructured mesh. 

> [!tip]
> Rasters and Vectors are much more common and are sufficient for most GIS tasks.

## Resources
- https://youtu.be/3JD_EzuoTUs?si=4J1eIvO8RysADicJ