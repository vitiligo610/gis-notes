---
title: 3. Scale & Projections
---

## Map Scale
Scale is used to represent the massive Earth within the limited space we have. It is a unitless measure and acts as a ratio.

Ways to represent map scale:
1.  **Fractional:** $1:15,046$ or $\frac{1}{15,046}$
2.  **Verbal:** (e.g., "One inch represents one mile")
3.  **Graphical:** A scale bar.

## Map Projections
It is impossible to translate a 3D spherical world to a 2D plane without introducing distortion. 

*   A **projection** is the systematic conversion of 3D spherical coordinates to a 2D planar coordinate system using mathematical equations.
*   There are multiple projections available because there is no single "best" option.
*   **Crucial Rule:** Shape and Area cannot be preserved correctly together in a single projection.

Projections are classified in two main ways:
### 1. By Information They Preserve
*   **Conformal Projections:** Preserve angles (shape). *Example: Mercator projection.*
*   **Equal-Area Projections:** Preserve area. *Example: Lambert cylindrical equal-area.*
*   **Azimuthal Projections:** Preserve direction. *Example: Polar azimuthal projection (measurements are true from the center point/poles only).*
*   **Equidistant Projections:** Preserve distance (measurements are true from a specific central point).
*   **Compromise Projections:** Preserve nothing perfectly, but balance distortions to look visually appealing. *Example: Robinson projection.*
### 2. By Developable Surface
A developable surface is a geometric figure that can be flattened into a plane without distortion. Information is systematically transferred from a reference globe to this surface.
*   **Types:** Cylinder, Cone, and Plane.

![[Pasted image 20260427124238.png]]

**Lines of Tangency & Secancy:**
*   **Line of Tangency:** The line where the reference globe touches the developable surface. 
    *   The scale of the map is true at this line (no distortion).
    *   Map scale is always calculated at this line.
    *   These lines are often standard parallels (lines of latitude).
    *   The least amount of distortion occurs around this line.
*   **Secant Projections:** The surface intersects the globe, creating *two* tangent lines. This generally provides more accurate information across a wider area.
*   **Orientation Variations:**
    *   **Transverse Projection:** Rotated $90^\circ$.
    *   **Oblique Projection:** Rotated at an oblique/obtuse angle.
*   When creating a projection, cartographers can choose their own specific longitude line to center the map on.

## References
- *Understanding Map Projections* - https://kartoweb.itc.nl/geometrics/Map%20projections/Understanding%20Map%20Projections.pdf