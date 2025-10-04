🛫 Indian Flight Route Network Analysis

📄 Overview:
This project visualizes the flight route network of India using open-source datasets and Python. Airports, routes, and India’s geographic boundary are integrated to generate a multi-origin multi-destination (OD) flight network. Routes are drawn as paths, airports are sized by connectivity, and results are exported as both static maps and animated videos.

📊 Project Specifications:
| Attribute          | Details                                                                   |
| ------------------ | ------------------------------------------------------------------------- |
| **Title**          | Indian Flight Route Network Analysis                                      |
| **Study Area**     | India (Domestic & International airports connected to Indian hubs)        |
| **Data Sources**   | OpenFlights Database (airports.dat, routes.dat), India Boundary Shapefile |
| **Platform**       | Python (GeoAI / GIS Analysis)                                             |
| **Spatial Scale**  | National (India)                                                          |
| **Analysis**       | Route visualization, hub identification, animation                        |
| **Output Formats** | PNG maps, MP4 animation, GeoDataFrame (airports + routes)                 |

⚙️ Dependencies:
Install required packages:pip install pandas geopandas matplotlib shapely cartopy pyproj numpy

📦 Package Breakdown:
      pandas → Tabular data handling (CSV for routes, airports).
      geopandas → Geospatial vector data (airports shapefile, boundaries).
      matplotlib → Plotting static & animated maps.
      shapely → Creating route geometries (LineString).
      cartopy → Map projections & geodesic plotting.
      pyproj → Great-circle geodesic calculations.
      numpy → Numerical operations for interpolation.
✅ The rest (os, urllib.request, matplotlib.patches, etc.) are part of the Python standard library or included in matplotlib itself — no extra install needed.

🚀 Workflow:
    A[🎯 Define Objective] --> B[📂 Collect Airport & Route Data]
    B --> C[🧹 Filter Indian Airports & Routes]
    C --> D[🛫 Build Great Circle Routes (PyProj)]
    D --> E[🗺️ Visualize with Cartopy]
    E --> F[🎥 Animate Routes Over Time]
    F --> G[📤 Export PNG + MP4 Outputs]

📌 Key Parameters:
| Parameter           | Value                   | Description                              |
| ------------------- | ----------------------- | ---------------------------------------- |
| **Projection**      | EPSG:4326 (WGS84)       | Geographic CRS                           |
| **Visualization**   | PlateCarree             | Map extent for India                     |
| **Route Curvature** | PyProj `Geod.npts`      | 100 interpolated points for great-circle |
| **Airport Symbol**  | Blue circles            | Edge highlighted in cyan                 |
| **Extras**          | Scale bar & North arrow | Added for cartographic clarity           |

📦 Outputs:
| Output Type       | Format       | Description                         |
| ----------------- | ------------ | ----------------------------------- |
| **Static Map**    | PNG          | Indian airports + curved routes     |
| **Animated Map**  | MP4          | Route buildup animation             |
| **Airport Layer** | GeoDataFrame | Indian airports with coordinates    |
| **Routes Layer**  | GeoDataFrame | Curved LineStrings for flight paths |

⚡ Highlights:
    ✅ OpenFlights global dataset filtered for India
    ✅ visualization of routes
    ✅ Airports labeled & styled with cyan halos
    ✅ Scale bar and north arrow for clarity
    ✅ Animated MP4 showing step-by-step route buildup
    ✅ GIS-ready outputs (GeoDataFrames)

📍 Data Sources:
    ✈️ Airports Data: "https://raw.githubusercontent.com/jpatokal/openflights/master/data/airports.dat"
    🛫 Routes Data: "https://raw.githubusercontent.com/jpatokal/openflights/master/data/routes.dat"

✍️ Author:
    Subham Roy ✨🌟
    📧 Email: subhamofficwork@gmail.com
    🔗 LinkedIn: [Subham Roy](https://www.linkedin.com/in/subham-roy-601867167?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3B2tlU2GXwQfmIQ5nAbBR26g%3D%3D)
    📚 Google Scholar: [Subham Roy](https://scholar.google.com/citations?user=bTxDrQgAAAAJ&hl=en)
    📝 ResearchGate: [Subham Roy](https://www.researchgate.net/profile/Subham-Roy-14)
    💬 Telegram: [Subham Roy](https://t.me/SubhamGeospatialAI)

✅ Conclusion:
      This project shows a complete Python geospatial workflow for visualizing Indian airport connectivity. 
      With open-source data and libraries:
        Built an Indian OD network from airports and routes
        Generated flight paths using geodesics
        Exported static and animated maps
        Produced cartography-ready outputs
      This framework supports aviation studies, policy analysis, and visualization of regional connectivity — and can be extended for global air traffic analysis.
