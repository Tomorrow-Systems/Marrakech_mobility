# **Marrakech Mobility Projects – Interactive Web Platform (Flask + React)**  
## **SPECIFICATION.md**

## **1. Project Overview**

### **1.1 Title**  
**Marrakech Mobility Projects – Interactive Map & Timeline**

### **1.2 Objective**  
Develop a web application that showcases **mobility projects in Marrakech** using:

- A **Landing Page** (non-map) that highlights project summaries, categories, and key statistics.
- A separate **Map Page** with a fully interactive geospatial view.
- Detailed project information (images, KPIs, connectivity).
- Filters for status, category, district, and timeline.
- Connectivity visualization between projects (corridors).

---

## **2. Target Users**

- **City Officials & Planners**
- **Citizens & Residents**
- **Transport Engineers & Consultants**
- **Investors / Researchers / Students**

Users should be able to:

- Explore Done / In Progress / Future mobility projects.
- See how projects connect structurally.
- Understand progress visually on the map.
- Discover summary information from the landing page.

---

## **3. High-Level Architecture**

### **3.1 Pages**

The platform consists of **two main pages**:

- `/` → **Landing Page** (overview + summaries)
- `/map` → **Interactive Map Page** (data visualization)

### **3.2 Frontend (React SPA)**

- Uses client-side routing to manage pages.
- Fetches data from Flask API.
- Components include:
  - `<Navbar>`
  - `<LandingHero>`
  - `<KeyStatsSection>`
  - `<StatusOverviewSection>`
  - `<ProjectHighlightsSection>`
  - `<ProjectCategoriesSection>`
  - `<ProjectListPreview>`
  - `<MapView>`
  - `<FilterPanel>`
  - `<ProjectList>`
  - `<ProjectDetailPanel>`
  - `<Legend>`
  - `<CorridorOverlay>` (optional)

### **3.3 Backend (Flask REST API)**

- Serves JSON data:
  - `/api/projects`
  - `/api/projects/<id>`
  - `/api/corridors` (optional)
- Stores data initially in static JSON files (upgradable to DB later).
- No HTML rendering; React handles UI.

### **3.4 Data Storage**

- Phase 1: JSON dataset (simple, fast for development)
- Phase 2: Optional database (PostgreSQL/SQLite)

---

## **4. API Specification**

Base URL: `/api`

### **4.1 GET /api/projects**

Returns list of all mobility projects.

**Optional query parameters:**

- `status=done,in_progress,future`
- `type=bhns,bus,cycling,intersection,pedestrian,parking,other`
- `district=<string>`
- `from_year=<year>`
- `to_year=<year>`

Used by:

- Landing Page (stats, highlights, previews)
- Map Page (initial dataset)
- Filter operations

---

### **4.2 GET /api/projects/<id>**

Returns full details of a single mobility project.

Used by Map Page + Landing Page modals.

---

### **4.3 GET /api/corridors** (optional)

Returns corridor definitions (grouped projects).

---

## **5. Data Model Specification (JSON)**

```json
{
  "id": "BHNS_L5",
  "name": "Ligne BHNS L5",
  "status": "in_progress",
  "type": "bhns",
  "geometry": {
    "type": "LineString",
    "coordinates": []
  },
  "district": "Gueliz",
  "description": "Projet de ligne BHNS pour améliorer la mobilité structurante...",
  "length_km": 12.3,
  "stations_count": 18,
  "intersections_count": 12,
  "start_date": "2023-01-15",
  "end_date": "2025-06-30",
  "planned_date": null,
  "budget": 540000000,
  "images": [
    {
      "url": "/images/bhns_l5/render.jpg",
      "caption": "Vue d’artiste de la station principale."
    }
  ],
  "connected_project_ids": ["BHNS_L6", "STATION_GUELIZ"],
  "links": ["https://example.com/bhns-l5"]
}
```

---

## **6. Landing Page Specification (`/`)**

### **6.1 Sections**

#### **Navbar**
Links:
- Projects Overview  
- Interactive Map → `/map`

#### **Hero Section**
- Title & subtitle
- Key numbers
- CTA → `/map`
- Secondary CTA → scroll to project categories

#### **Key Statistics**
Generated from `/api/projects`:
- Total projects
- Done / In Progress / Future
- Optional: km of corridors, intersections upgraded

#### **Status Overview**
Three blocks with:
- Status summary
- Project counts
- Link → `/map?status=...`

#### **Project Highlights**
Show 3–6 flagship projects with:
- Image
- Status
- Description
- “View on Map” → `/map?focus=<id>`

#### **Project Categories**
- BHNS
- Bus Lines
- Cycling
- Traffic Lights
- Parking
- Pedestrian zones

Each clickable → `/map?type=<category>`

#### **Projects List Preview**
- Name
- Status
- Type
- “View on Map”

#### **Final CTA**
Button → `/map`

---

## **7. Map Page Specification (`/map`)**

### **7.1 Structure**
- Map area
- Side panel with filters + list
- Detail panel on project click

### **7.2 Map Features**
- Pan & zoom  
- Base layers  
- Markers / lines / polygons  
- Status color coding:
  - Green → Done  
  - Orange → In Progress  
  - Blue → Future  

### **7.3 Filter Panel**
Filters by:
- Status  
- Type  
- District  
- Timeline (year slider)

### **7.4 Project List**
Shows:
- Name  
- Status  
- Type  
- District  

Click → select project on the map.

### **7.5 Project Detail Panel**
Shows:
- Title  
- Status  
- Description  
- Key metrics  
- Images  
- Connectivity list  
- Button to highlight connected projects  

### **7.6 Corridor Mode**
Toggle:
- Fetches `/api/corridors`
- Shows corridor overlays

---

## **8. User Flows**

### **8.1 Landing → Map**
1. User opens `/`
2. Clicks map button
3. Goes to `/map`
4. Selects project → sees details

### **8.2 Highlighted Project → Focused Map**
1. User clicks highlight card
2. Goes to `/map?focus=<id>`
3. Map focuses project

### **8.3 Category → Filtered Map**
1. User clicks category card
2. Goes to `/map?type=cycling`
3. Map filtered

### **8.4 Landing Only**
User browses list without map.

---

## **9. Non-Functional Requirements**

### **Performance**
- Cache project list in frontend  
- Lazy-load images  
- Efficient map rendering  

### **Responsiveness**
- Landing and map must work on mobile/tablet/desktop  
- Collapsible panels on small screens  

### **Accessibility**
- Colorblind-safe palette  
- Keyboard-friendly navigation  
- ARIA labels  

### **Localization**
Must support:
- French  
- Arabic  
- Optional English  

---

## **10. Deliverables**

- Flask backend:
  - `/api/projects`
  - `/api/projects/<id>`
  - `/api/corridors`

- React frontend:
  - Landing page (`/`)
  - Map page (`/map`)

- JSON dataset

---

## **11. Future Extensions**
- Admin dashboard  
- JWT user authentication  
- Story mode (guided tours)  
- Realtime project progress data integration  
- Open Data exports (CSV, GeoJSON)

---

**End of SPECIFICATION.md**
