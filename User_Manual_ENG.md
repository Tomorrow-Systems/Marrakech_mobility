# Marrakech Mobility Projects - User Manual

## Table of Contents

1. [Getting Started](#1-getting-started)
2. [Admin Dashboard Overview](#2-admin-dashboard-overview)
3. [Managing Projects](#3-managing-projects)
4. [Managing Stories](#4-managing-stories)
5. [Managing Infrastructure](#5-managing-infrastructure)
6. [Managing Groups](#6-managing-groups)
7. [Using the Map Editor](#7-using-the-map-editor)
8. [Settings & Customization](#8-settings--customization)
9. [Backup & Restore](#9-backup--restore)
10. [Public Website Features](#10-public-website-features)

---

## 1. Getting Started

### 1.1 Accessing the Admin Panel

1. Navigate to your website's homepage
2. Click the **Admin** button in the navigation bar (if visible)
3. Or go directly to `/admin` in your browser
4. Enter your username and password
5. Click **Login**

> **Default Credentials:**
> - Username: `admin`
> - Password: `admin123`
> 
> ⚠️ Please change these credentials after first login!

### 1.2 Admin Dashboard Layout

After logging in, you'll see:

- **Header**: Shows your username, Home button, and Logout button
- **Tabs**: Projects, Stories, Infrastructure, Groups, Settings
- **Map Editor Button**: Orange/accent-colored button to access the map editor
- **Action Buttons**: Context-specific buttons (New Project, New Story, etc.)

---

## 2. Admin Dashboard Overview

### 2.1 Navigation Tabs

| Tab | Purpose |
|-----|---------|
| **Projects** | Manage mobility projects |
| **Stories** | Create narrative content with chapters |
| **Infrastructure** | Manage infrastructure points |
| **Groups** | Organize projects and stories into groups |
| **Settings** | Configure branding, language, map layers |

### 2.2 Common Actions

- **Search**: Use the search box to filter items
- **Edit**: Click the pencil icon or "Edit" button
- **Delete**: Click the trash icon (confirmation required)
- **Reorder**: Use up/down arrows to change display order

---

## 3. Managing Projects

### 3.1 Creating a New Project

1. Click the **Projects** tab
2. Click **New Project** button
3. Fill in the project details (see sections below)
4. Click **Save** or **Create Project**

### 3.2 Project Fields Explained

#### Basic Information

| Field | Description | Example |
|-------|-------------|---------|
| **Project ID** | Unique identifier (can be edited) | `can-marrakech-01` |
| **Name** | Project title | `Boulevard Extension Phase 1` |
| **Type** | Category of project | `Voirie & Mobilité` |
| **Status** | Current state | `done`, `in_progress`, `future` |
| **Progress** | Completion percentage | `75%` |
| **District** | Location/area | `Marrakech - Zone Nord` |

#### Descriptions

| Field | Description |
|-------|-------------|
| **Short Description** | Brief summary (shown in cards) |
| **Description** | Full detailed description |
| **Objectives** | List of project goals (one per line) |

#### Metrics

| Field | Description |
|-------|-------------|
| **Length (km)** | Route length in kilometers |
| **Stations** | Number of stations/stops |
| **Intersections** | Number of intersections |

#### Dates

| Field | Description |
|-------|-------------|
| **Start Date** | When project began |
| **End Date** | When project completed |
| **Planned Date** | Expected completion (for future projects) |

#### Budget

| Field | Description |
|-------|-------------|
| **Budget** | Project cost | `81.12 MDH` |

> 💡 Budget visibility can be toggled on/off in Settings

### 3.3 Adding Images to Projects

#### Step-by-Step:

1. In the project edit form, find the **Images** section
2. Click **Add Image** or drag files to upload
3. For each image, you can set:
   - **Caption**: Description of the image
   - **Category**: Choose from:
     - `before` - State before project
     - `after` - State after completion

#### Before/After Images:

When you have images in both "before" and "after" categories, the project detail page will automatically display them in separate sections, making it easy for visitors to see the transformation.

#### Image Tips:
- Supported formats: JPG, PNG, GIF, WebP, SVG
- Maximum file size: 50MB per image
- Recommended: Use high-quality images (at least 1200px wide)

### 3.4 Adding Videos to Projects

#### Option 1: YouTube Videos (Recommended)

1. Find the **Videos** section in project edit
2. Click **Add Video**
3. Select type: **YouTube/Embed**
4. Paste the YouTube URL:
   - Full URL: `https://www.youtube.com/watch?v=VIDEO_ID`
   - Short URL: `https://youtu.be/VIDEO_ID`
5. Add a title for the video
6. Save

#### Option 2: Direct Video Upload

1. Click **Add Video**
2. Select type: **Upload**
3. Click to select or drag a video file
4. Supported formats: MP4, WebM, MOV, AVI
5. Maximum size: 500MB

#### Video Display:
- YouTube videos will show an embedded player
- Uploaded videos will use the browser's native video player

### 3.5 Project Geometry (Map Location)

1. Click **Edit Geometry** or use the **Map Editor** button
2. See [Section 7: Using the Map Editor](#7-using-the-map-editor) for details

### 3.6 Connected Projects

Link related projects together:

1. Find the **Connected Projects** section
2. Select projects from the dropdown
3. These will appear as links on the project detail page

### 3.7 Project Display Order

Control the order projects appear:

1. In the Projects list, use the **↑** and **↓** buttons
2. Or edit the **Display Order** field (lower numbers appear first)

---

## 4. Managing Stories

### 4.1 Understanding Stories

Stories are narrative content that can span multiple chapters. Each story can:
- Have a cover image
- Contain multiple chapters
- Link to projects and infrastructure
- Include images and videos

### 4.2 Creating a New Story

1. Click the **Stories** tab
2. Click **New Story** button
3. Fill in story details:

| Field | Description |
|-------|-------------|
| **Title** | Story headline |
| **Summary** | Brief description (shown in cards) |
| **Content** | Main story content (optional) |
| **Cover Image** | Main image for the story card |
| **Published** | Toggle to make story visible |

### 4.3 Adding a Cover Image

#### Option 1: Upload Image

1. Click **Upload Cover Image**
2. Select an image file from your computer

#### Option 2: Use URL

1. Click **Use URL**
2. Paste the direct image URL

### 4.4 Managing Chapters

Chapters are sections within a story that can be navigated individually.

#### Adding a Chapter:

1. Open a story for editing
2. Scroll to the **Chapters** section
3. Click **Add Chapter**
4. Fill in:
   - **Title**: Chapter heading
   - **Text**: Chapter content
   - **Project Links**: Select related projects
   - **Images**: Add chapter-specific images
   - **Videos**: Add YouTube or uploaded videos
   - **Map Focus**: Set coordinates to highlight on map

#### Chapter Order:

Use the drag handles or order field to arrange chapters.

#### Map Focus Setting:

1. Click **Set Map Focus**
2. Enter latitude, longitude, and zoom level
3. When readers view this chapter, the map will focus on this location

### 4.5 Publishing Stories

Stories have a published/unpublished status:

- **Published**: Visible on the public Stories page
- **Unpublished**: Only visible in admin

Toggle the **Published** switch to control visibility.

---

## 5. Managing Infrastructure

### 5.1 What is Infrastructure?

Infrastructure items are points of interest like:
- Transportation hubs (airports, train stations)
- Utilities
- Public spaces
- Parking facilities

### 5.2 Creating Infrastructure

1. Click the **Infrastructure** tab
2. Click **New Infrastructure**
3. Fill in:

| Field | Description |
|-------|-------------|
| **ID** | Unique identifier |
| **Name** | Infrastructure name |
| **Type** | Type of infrastructure |
| **Category** | Category classification |
| **Description** | Detailed description |
| **Visible** | Show/hide on map |

### 5.3 Adding Geometry

1. Click **Edit Geometry**
2. Use the Map Editor to place points, draw lines, or create polygons
3. See [Section 7](#7-using-the-map-editor) for detailed instructions

### 5.4 Point Panel Information

For marker points on the map, you can add panel information that appears when clicked:

- **Panel Title**: Title shown in the info panel
- **Panel Description**: Description text
- **Panel Image**: Image shown in the panel

---

## 6. Managing Groups

### 6.1 Understanding Groups

Groups help organize projects and stories into categories. They provide:
- Filtering on the public pages
- Visibility control for multiple items
- Organization for large numbers of items

### 6.2 Project Groups

1. Click the **Groups** tab
2. Select **Project Groups**
3. Click **New Group**
4. Configure:

| Field | Description |
|-------|-------------|
| **Name** | Group name |
| **Description** | Group description |
| **Projects** | Select projects to include |
| **Hidden Projects** | Projects in group but not shown |
| **Visible** | Show/hide entire group |

### 6.3 Story Groups

Similar to project groups but for stories:

1. Click the **Groups** tab
2. Select **Story Groups**
3. Click **New Group**
4. Add stories to the group

### 6.4 Visibility Control

Groups provide two levels of visibility:

1. **Group Visibility**: Toggle the entire group on/off
2. **Hidden Items**: Hide specific items within a visible group

This allows flexible control over what appears on the public site.

---

## 7. Using the Map Editor

### 7.1 Accessing the Map Editor

1. Click the accent-colored **Map Editor** button in admin
2. Or navigate directly to `/admin/map-editor`

### 7.2 Drawing Tools

| Tool | Icon | Purpose |
|------|------|---------|
| **Marker** | 📍 | Place single points |
| **Line** | ➖ | Draw routes/paths |
| **Polygon** | ⬡ | Create areas/zones |
| **Edit** | ✏️ | Modify existing shapes |
| **Delete** | 🗑️ | Remove shapes |

### 7.3 Placing Markers

1. Click the **Marker** tool
2. Click on the map where you want the marker
3. A marker will be placed
4. Click the marker to add panel information:
   - Panel Title
   - Panel Description
   - Panel Image (upload or URL)

### 7.4 Drawing Lines

1. Click the **Line** tool
2. Click to start the line
3. Click to add more points
4. Double-click to finish the line

Lines are useful for:
- Roads
- Bus routes
- Walking paths
- Project corridors

### 7.5 Drawing Polygons

1. Click the **Polygon** tool
2. Click to create vertices
3. Click the first point again to close the polygon

Polygons are useful for:
- District boundaries
- Project zones
- Areas of interest

### 7.6 Editing Geometry

1. Click the **Edit** tool
2. Click on a shape to select it
3. Drag vertices to reposition
4. Click **Save** when done

### 7.7 Map Layers

Change the map background:

1. Click the **Layers** button
2. Select from available layers:
   - OpenStreetMap (default)
   - Satellite
   - Terrain
   - Dark Mode
   - Light Mode
   - Topographic
   - And more...

### 7.8 Icon Customization

#### Using Custom Icons:

1. In the Map Editor, find the **Icons** panel
2. Select from the SVG library
3. Or upload new SVG icons

#### Icon Sizes:

Three separate size controls:

| Control | Affects |
|---------|---------|
| **Project Icons** | Project marker sizes |
| **Infrastructure Icons** | Infrastructure marker sizes |
| **Custom Icons** | Uploaded custom icon sizes |

Adjust the slider to change icon sizes (small → large).

### 7.9 Importing KML

Import existing geographic data:

1. Click **Import KML**
2. Select a .kml or .kmz file
3. The geometry will be added to the current layer

### 7.10 Exporting KML

Export data for use in other applications:

1. Click **Export KML**
2. Select items to export
3. Download the generated KML file

---

## 8. Settings & Customization

### 8.1 Language Settings

1. Go to **Settings** tab
2. Find **Language** section
3. Select:
   - **Français** - French interface
   - **English** - English interface

The entire website will switch to the selected language.

### 8.2 Branding Settings

#### Logo Upload:

1. Go to **Settings** → **Branding**
2. Click **Upload Logo**
3. Select your logo image
4. The logo will appear in the navigation bar

#### Favicon:

1. Find **Favicon** section
2. Upload your favicon image (recommend 32x32 or 64x64 pixels)

#### Accent Color:

Customize the primary color used throughout the site:

1. Find **Accent Color** section
2. Use the RGB sliders or enter values:
   - **R** (Red): 0-255
   - **G** (Green): 0-255
   - **B** (Blue): 0-255
3. Preview updates in real-time

#### Background Color:

Customize the background color:

1. Find **Background Color** section
2. Adjust RGB values as needed

### 8.3 Visibility Toggles

| Toggle | Effect |
|--------|--------|
| **Show Admin Button** | Show/hide admin button in public navbar |
| **Show Budget** | Show/hide budget information on projects |

### 8.4 Map Layer Configuration

Configure which map layers are available:

1. Go to **Settings** → **Map Layers**
2. Toggle layers on/off
3. Available layers:
   - OpenStreetMap
   - Satellite
   - Terrain
   - Dark Mode
   - Light Mode
   - Topographic
   - Watercolor
   - Streets
   - Outdoors
   - Hybrid

### 8.5 Icon Size Settings

Adjust default icon sizes for the map:

1. Go to **Settings** → **Icon Sizes**
2. Three separate controls:
   - **Project Icons**: Size for project markers
   - **Infrastructure Icons**: Size for infrastructure markers
   - **Custom Icons**: Size for custom uploaded icons
3. Use the slider (values typically 16-64 pixels)

### 8.6 Home Page CMS

Customize the home page content:

1. Go to **Settings** → **Home Content**
2. Edit sections:

**Hero Section:**
- Hero Title
- Hero Subtitle
- Hero Background Image

**Statistics:**
- Number of Projects
- Kilometers
- Intersections

**About Section:**
- About Title
- About Text
- About Image

---

## 9. Backup & Restore

### 9.1 Creating a Backup

Backup all your data regularly:

1. Go to **Settings** tab
2. Find **Backup & Restore** section
3. Click **Download Backup**
4. Save the JSON file to a safe location

The backup includes:
- All projects
- All stories and chapters
- All infrastructure
- All groups
- All settings
- Home page content

### 9.2 Restoring from Backup

⚠️ **Warning**: Restoring will replace all current data!

1. Go to **Settings** → **Backup & Restore**
2. Click **Restore from Backup**
3. Select your backup JSON file
4. Confirm the restoration
5. Wait for the process to complete

### 9.3 Importing Individual Projects

Import a single project without affecting other data:

1. Go to **Settings** → **Import**
2. Click **Import Project**
3. Select a project JSON file
4. If the ID already exists, a new ID will be generated

---

## 10. Public Website Features

### 10.1 Home Page

The public home page displays:
- Hero section with title and image
- Statistics overview
- Category links
- Featured content

### 10.2 Interactive Map

The map page (`/map`) features:

#### Filters:
- **Status**: Filter by done/in progress/future
- **Type**: Filter by project type
- **Search**: Text search for projects
- **Groups**: Filter by project groups (collapsible sections)

#### Map Interaction:
- Click markers to see project details
- Click lines/polygons to select projects
- Use the side panel to view full details
- Click images to open lightbox gallery

### 10.3 Projects Page

The projects page (`/projects`) shows:
- Grid of project cards
- Filtering by group
- Search functionality
- Click to view full details

### 10.4 Stories Page

The stories page (`/story`) displays:
- Carousel of story cards
- Group filtering with badges
- Click to read full story with chapters
- Navigation between chapters

### 10.5 Project Detail Page

Individual project pages show:
- Hero image/gallery
- Before/After image sections
- Description and objectives
- Project metrics
- Related stories
- Videos (YouTube embedded)
- Map location

### 10.6 Language Switching

Users can switch languages:
- Look for the language toggle (FR/EN)
- Click to switch between French and English
- All content will update to the selected language

### 10.7 Media Lightbox

When viewing images:
- Click any image to open fullscreen
- Use arrows to navigate between images
- Click outside or press Escape to close
- Works on project pages, stories, and map panels

---

## Quick Reference

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| Escape | Close dialogs/lightbox |
| Arrow Left/Right | Navigate images in lightbox |

### File Size Limits

| Type | Maximum Size |
|------|--------------|
| Images | 50 MB |
| Videos | 500 MB |
| Icons | 5 MB |
| Logos | 10 MB |
| SVG Library | 2 MB |
| KML Files | 10 MB |

### Supported File Formats

| Type | Formats |
|------|---------|
| Images | JPG, JPEG, PNG, GIF, WebP, SVG |
| Videos | MP4, WebM, MOV, AVI |
| Icons | PNG, SVG, ICO |
| Geographic | KML, KMZ |

---

## Troubleshooting

### Common Issues

**Q: I can't see my changes on the public site**
- Make sure the item is published/visible
- Check group visibility settings
- Clear your browser cache

**Q: Images aren't uploading**
- Check file size (max 50MB)
- Ensure correct format (JPG, PNG, etc.)
- Try a different browser

**Q: YouTube video isn't playing**
- Verify the URL is correct
- Make sure the video is public on YouTube
- Try the full YouTube URL format

**Q: Map geometry isn't saving**
- Click Save after making changes
- Ensure you have edit permissions
- Try refreshing and re-drawing

### Getting Help

If you encounter issues:
1. Check the system logs (Settings → System Logs)
2. Take a screenshot of any error messages
3. Contact your administrator

---

*User Manual v1.0*
*Tomorrow Systems Projects Platform*
*Last Updated: December 2025*
