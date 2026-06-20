---
title: 5. Navigation Principles
---
## Direction and Bearings
*   **True North:** The geographic North Pole. It does not move and serves as the reference point for *True Bearings*.
*   **Relative North:** The direction the ship's bow is pointing. It moves when the ship moves and serves as the reference point for *Relative Bearings*.
*   **True Bearing:** The direction of an object measured clockwise from True North ($0^\circ - 359^\circ$).
*   **Relative Bearing:** The direction of an object measured clockwise from Relative North / the ship's bow ($0^\circ - 359^\circ$).

![[Pasted image 20260427125129.png]]

## Distance and Units of Measurement
Distance is the spatial separation between two points.

**Common Navigation Units:**
*   Nautical Mile (NM)
*   Statute Mile (SM)
*   Kilometer (Km) / Meters (m) / Centimeters (cm)
*   Feet (ft) / Inches (in)

**Important Conversions:**
*   $1 \text{ NM} = 1,852 \text{ m } (1.852 \text{ km})$
*   $1 \text{ NM} = 1.15 \text{ SM}$
*   $1 \text{ NM} = 6,076 \text{ ft}$
*   $1 \text{ SM} = 1,609 \text{ m } (1.609 \text{ km})$
*   $1 \text{ m} = 3.28 \text{ ft}$
*   $1 \text{ ft} = 30.48 \text{ cm}$
*   $1 \text{ in} = 2.54 \text{ cm}$

### Great Circles vs. Small Circles
On a flat surface, the shortest distance between two points is a straight line. This is **not true** on Earth because it is a sphere.

*   **Great Circle:** A plane passing through the sphere that intersects its exact center, dividing the Earth into two perfectly equal parts. *(The Equator and all lines of Longitude are great circles).*
*   **Small Circle:** A plane passing through the sphere that does *not* intersect the center, dividing the Earth into unequal parts. *(All lines of Latitude, except the Equator, are small circles).*

![[Pasted image 20260427124522.png]]

## Types of Routes in Navigation

#### 1. Great Circle Route (Orthodromic Route)
*   An arc of a great circle that joins two points on the Earth's surface.
*   It is the **shortest physical route** between two points on a sphere.
*   **Drawback:** The compass bearing changes constantly as you cross all meridians at different angles, making it difficult to follow manually.

#### 2. Rhumb Line (Loxodromic Route)
*   An arc of a spherical helix that joins two points on the Earth's surface.
*   The route cuts across all meridians at the **same exact angle**.
*   The angle between the meridian (longitude) and the course is constant (i.e., your heading stays the same).
*   On a standard 2D Mercator map, a Rhumb Line appears as a perfectly straight line.
*   **Advantage:** The course is much easier to follow because you do not have to change your bearing.

![[Pasted image 20260427124645.png|470]]
*A rhumb line (blue) compared to a great-circle arc (red) between Lisbon, Portugal and Havana, Cuba. Top: orthographic projection. Bottom: Mercator projection.*

### Navigating a Great Circle Route
**Question:** How do you handle the constantly changing bearings of a Great Circle Route?
**Answer:** Simplified Navigation.
1.  Split the entire Great Circle route into smaller, manageable segments.
2.  Set a constant bearing (Rhumb Line) for each individual segment.
3.  This results in multiple straight-line paths that closely approximate the shortest path (the great circle arc). Simply follow that segmented path.