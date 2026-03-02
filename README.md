# CRS Clock Ring Station (CRS-0000)

A web-based dashboard application for the United States Postal Service (USPS) to manage and monitor Clock Ring Stations (CRS).

## Overview

The CRS Clock Ring Station app provides a centralized interface for managing USPS clock ring station hardware and configuration. It displays a list of registered CRS devices along with their configuration details such as Reader IDs, timeout settings, available actions, and assigned areas.

## Features

- **CRS List Dashboard** – View all registered Clock Ring Stations in a sortable, searchable table.
- **Search** – Filter CRS entries in real time using the search bar.
- **Export** – Download the current CRS list for offline review.
- **Add CRS** – Register a new Clock Ring Station directly from the dashboard.
- **Collapsible Sidebar** – Expand or collapse the navigation sidebar to maximize screen space.
- **Pagination** – Navigate large CRS datasets with configurable items-per-page controls.
- **Navigation Links** – Quick access to related modules: CRS, OPR, Clock Rings, Badges, and TACS.

## Tech Stack

| Library | Purpose |
|---|---|
| [Bootstrap 5](https://getbootstrap.com/) | UI layout and component styling |
| [Bootstrap Icons](https://icons.getbootstrap.com/) | Icon set |
| [Bootstrap Table](https://bootstrap-table.com/) | Enhanced data table with sorting and filtering |
| [Luxon](https://moment.github.io/luxon/) | Date and time utilities |
| [Lodash](https://lodash.com/) | JavaScript utility functions |
| [SignalR](https://dotnet.microsoft.com/apps/aspnet/signalr) | Real-time communication |
| [onScan.js](https://github.com/axenox/onscan.js) | Barcode / badge scanner input handling |
| [page.js](https://github.com/visionmedia/page.js) | Client-side routing |

## Project Structure

```
crs-clockringstation-0000-app/
└── src/
    └── Web/
        ├── default.html          # Main application entry point
        └── wwwroot/
            ├── css/
            │   └── images/       # USPS logo assets
            └── lib/              # Third-party client-side libraries
                ├── bootstrap/
                ├── bootstrap-icons/
                ├── bootstrap-table/
                ├── lodash/
                ├── luxon/
                ├── microsoft/
                │   ├── signalr/
                │   └── signalr-protocol-msgpack/
                ├── onscan/
                ├── page/
                └── vanillajs/
```

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Edge, Firefox, Safari)
- A local web server or IDE with live-preview capability (e.g., [VS Code Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer))

> **Note:** Opening `default.html` directly via the `file://` protocol may block some browser features. Serving the files through a local HTTP server is recommended.

### Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/marcel-curtusan-usps/crs-clockringstation-0000-app.git
   cd crs-clockringstation-0000-app
   ```

2. Open `src/Web/default.html` using a local web server.  
   For example, with the VS Code **Live Server** extension, right-click `default.html` and select **Open with Live Server**.

3. The CRS List Dashboard will open in your default browser.

## CRS Table Columns

| Column | Description |
|---|---|
| CRS Name | Unique identifier for the Clock Ring Station |
| Reader ID | Hardware reader identifier |
| Reset Timeout | Duration (in seconds) before the station resets |
| Confirmation Timeout | Duration (in seconds) to wait for user confirmation |
| Available Action | Supported ring action codes (e.g., BT, OL, IL, ET, MV, TR) |
| Area | Physical area or zone assignment |

## Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request.

## License

This project is maintained by USPS. All rights reserved.
