
# Marrakech Mobility Projects – Interactive Web Platform (Flask + React)
## SPECIFICATION.md

---

## 1. Project Overview

### 1.1 Title
**Marrakech Mobility Projects – Interactive Map, Detailed Project Pages, Storytelling & Admin CMS**

### 1.2 Objective
Develop a fully interactive web application to showcase **Marrakech mobility projects**, with:

- A **Landing Page** presenting achievements and categories.
- An **Interactive Map** showing all projects with filters and connectivity.
- A **Storytelling Page** explaining the evolution of mobility.
- A dedicated **Project Detail Page** for every project (images, videos, metrics, descriptions).
- An **Admin Page** to add/edit/delete projects and draw map geometries.
- Full geospatial visualization (points, lines, polygons).
- Full media support (images, videos, galleries).
- Fully dynamic content stored in database or JSON.

The goal is to give the public and decision‑makers an intuitive, rich, and informative view of all mobility-related efforts.

---

## 2. Target Users

### 2.1 Public Users
- **City Officials & Planners**
- **Citizens & Residents**
- **Transport Engineers & Consultants**
- **Investors / Researchers / Students**

They want quick access to:
- What projects exist?
- What is done/in progress/planned?
- Where are projects physically located?
- How do projects connect?
- What are the benefits?

### 2.2 Professional Users
- Engineers  
- City planners  
- Mobility consultants  
- Investors  

They need:
- High‑level summaries  
- Accurate geospatial data  
- Connectivity between networks  
- Detailed project pages  

### 2.3 Admin Users
Responsible for:
- Adding new projects  
- Editing geometries  
- Updating statuses  
- Uploading images & videos  
- Ensuring data accuracy  

Secure access via `/admin`.

---

## 3. High-Level Architecture

### 3.1 Pages / Routes

| Route | Description |
|-------|-------------|
| `/` | Landing Page |
| `/map` | Interactive Map Page |
| `/story` | Storytelling Page |
| `/projects/:id` | Full Project Detail Page |
| `/admin` | Admin Dashboard (login + editor) |
| `/admin/editor/:id` | Edit existing project |
| `/admin/new` | Create new project |

---

### 3.2 Frontend (React SPA)

Main components:

**Global**
- `Navbar`, `Footer`, theming

**Landing Page**
- Hero section  
- Stats  
- Highlights  
- Categories  
- Project Preview List  

**Map Page**
- MapView (Leaflet/Mapbox)  
- FilterPanel  
- ProjectList  
- ProjectDetailPanel  
- CorridorOverlay  
- Legend  

**Story Page**
- StoryTimeline  
- StoryChapters  
- Chapter detail view  
- Map CTA  
- Project CTA  

**Project Detail Page**
- Header  
- Meta Summary  
- Image Gallery  
- Video Section  
- Full Description  
- Connectivity Section  
- Back to Map/Story Buttons  

**Admin Page**
- AdminLogin  
- AdminProjectList  
- AdminProjectForm  
- AdminMapEditor (draw/edit geometry)  
- Icon/Color Selector  

---

## 4. Backend Architecture (Flask)

### 4.1 Public API Endpoints

#### `GET /api/projects`
Returns full list of projects.

Supports filters:
- `status`
- `type`
- `district`
- `from_year`
- `to_year`

#### `GET /api/projects/<id>`
Returns full project details including:
- geometry
- metrics
- images
- videos
- connectivity
- media URLs
- descriptions

#### `GET /api/corridors`
Optional – geometric corridors linking multiple projects.

#### `GET /api/stories`
Optional – storytelling content.

---

### 4.2 Admin Endpoints (Protected)

#### `POST /api/login`
Authenticates admin.

#### `POST /api/projects`
Creates new project.

#### `PUT /api/projects/<id>`
Edits project.

#### `DELETE /api/projects/<id>`
Deletes project.

#### `POST /api/upload`
(Optional) Handle media uploads.

---

## 5. Data Model

### 5.1 Project Model (Extended)

```
{
  "id": "BHNS_L5",
  "name": "Ligne BHNS L5",
  "status": "in_progress",
  "progress_status":"30%",
  "type": "bhns",
  "district": "Gueliz",

  "geometry": {
    "type": "LineString",
    "coordinates": []
  },

  "short_description": "",
  "description": "",

  "length_km": 0,
  "stations_count": 0,
  "intersections_count": 0,

  "start_date": "",
  "end_date": "",
  "planned_date": "",
  "budget": 0,

  "images": [
    { "url": "", "caption": "" }
  ],

  "videos": [
    { "url": "", "title": "" }
  ],

  "map_style": {
    "icon": "bus",
    "color": "#FF8800"
  },

  "connected_project_ids": [],
  "links": []
}
```

### 5.2 Story Model

```
{
  "id": "",
  "title": "",
  "summary": "",
  "chapters": [
    {
      "id": "",
      "title": "",
      "text": "",
      "project_ids": [],
      "map_focus": {}
    }
  ]
}
```

---

## 6. Page Specifications

### 6.1 Landing Page

Sections:
- Hero (title, subtitle, main CTAs)
- KPIs (Done / In Progress / Future)
- Categories grid
- Highlighted flagship projects
- Short list preview
- Footer call-to-action to map and story

CTA Buttons:
- “Explore Map”
- “View Story”
- “Browse Projects”

---

## 6.2 Map Page (`/map`)

Features:
- Fully interactive map (Leaflet/Mapbox)
- Supports:
  - LineString
  - Point
  - Polygon
- Color based on `map_style` or fallback rules
- Filters:
  - Status
  - Type
  - District
  - Timeline slider
  - projects
  - points of intrests
- Left or right drawer with:
  - Project list
  - Search
  - Sorting
  - when clicking item (project on the drawer it acts as a filter and shows only that project on map)
- When clicking a feature:
  - Open ProjectDetailPanel
  - Show short description
  - Show badges
  - Show image
  - Button: **“View Full Project Page”**
  - Button: “Zoom to Project”
  - Button: “Highlight Connectivity”

---

## 6.3 Storytelling Page (`/story`)

Elements:
- Hero section
- Timeline component (years/phases)
- Story cards
- Chapter detail view
- Rich text
- Images
- Links:
  - “Open on Map”
  - “Open Project Page”
- Cross-navigation:
  - Previous chapter
  - Next chapter

---

## 6.4 Project Detail Page (`/projects/:id`)

Sections:

### Header
- Title
- Status & Type badges
- District
- Last updated

### Meta Summary
- Length, stations, intersections count
- Start/end/planned dates
- Budget

### Image Gallery
- Scrollable
- Captions

### Video Section
- YouTube / mp4 embeds
- Thumbnails

### Full Description
- Rich multi-paragraph text
- Optionally structured into:
  - Context
  - Objectives
  - Execution
  - Impact

### Connectivity Section
- List of related projects
- Each item with:
  - “View Project”
  - “Open on Map”

### Maps & Links
- Button: **“Open on Interactive Map”**
- Button: “Back to Story” (if navigation state indicates origin)

---

## 6.5 Admin Page (`/admin`)

### Login
- Password input
- Simple session cookie

### Admin Dashboard
- Project table:
  - ID, name, status, type, district
  - Buttons:
    - Edit
    - Delete
    - View on Map

### Admin Project Editor
- Form fields:
  - Name, ID (auto or manual)
  - Status (dropdown)
  - Type (dropdown)
  - District
  - Short description
  - Full description
  - Length, metrics
  - Dates
  - Budget
  - Image URLs list
  - Video URLs list
  - Map icon selector
  - Color picker

### Map Editor
- Add geometry:
  - Point
  - LineString
  - Polygon (optional)
- Edit geometry:
  - Drag vertices
  - Add/remove segments

All saved to backend via PUT.

---

## 7. User Flows

### Public
- Landing → Map  
- Landing → Story  
- Landing → Project Page  
- Map → Project Page  
- Story → Map  
- Story → Project Page  

### Admin
- Login → Dashboard  
- Dashboard → Create project  
- Dashboard → Edit project  
- Dashboard → Delete project  

---

## 8. Non‑Functional Requirements

### Performance
- Frontend caching
- Lazy-loading images/videos
- Optimized geometries
- DB queries cached

### Security
- Admin password stored server-side
- HTTPS mandatory
- No public write endpoints

### Accessibility
- Labels + icons
- Colorblind-safe design
- ARIA support

### Localization
- French, English & Arabic UI support
- Multi-language content option later

---

## 9. Deliverables

- Full React frontend
- Full Flask backend
- Complete API
- Admin CMS
- Map layers & geometry editor
- Complete documentation
- Docker files for deployment

---