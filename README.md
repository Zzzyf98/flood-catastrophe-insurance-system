This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Project Overview

This is a Flood Catastrophe Insurance System built with Next.js. The system provides comprehensive flood risk assessment and insurance management capabilities, including urban spatial element visualization, disaster event repository, risk mapping, asset management, and catastrophe modeling.

## Key Features

1. **Urban Spatial Elements**: Visualization of urban geography, infrastructure, and socioeconomic data layers
2. **Disaster Event Repository**: Historical and stochastic disaster event data management
3. **Risk Map**: Multi-hazard risk visualization with exposure analysis
4. **Asset Management**: Insurance asset tracking and risk assessment
5. **Catastrophe Model**: Flood catastrophe modeling and simulation
6. **Accessibility**: Integration with global weather data and warning systems

## System Architecture

The system is built with the following technologies:
- **Frontend**: Next.js 15, React 19, TypeScript
- **UI Components**: Tailwind CSS, shadcn/ui
- **Mapping**: Leaflet, react-leaflet
- **State Management**: React Hooks
- **Data Visualization**: Custom charting components
- **API Communication**: Axios
- **File Handling**: JSZip, shpjs
- **GIS Server**: GeoServer (hosted on 143.89.22.7:8090 and 143.89.23.123:8080)

All map layers are served through GeoServer instances. The system retrieves spatial data from these servers to visualize various urban elements, disaster events, and risk maps.

## Project Structure

```
src/
├── app/                 # Next.js app router pages
│   ├── cityinfo/        # Urban Spatial Elements module
│   ├── disasterinfo/    # Disaster Event Repository module
│   ├── riskmap/         # Risk Map module
│   ├── asset/           # Asset Management module
│   ├── model/           # Login page for Catastrophe Model
│   ├── oasis/           # Main dashboard for Catastrophe Model
│   ├── fuzhu/           # Accessibility module
│   ├── earth/           # Earth weather visualization
│   ├── usercenter/      # User profile and settings
│   └── layout.tsx       # Root layout component
├── components/          # Reusable UI components
│   └── ui/              # shadcn/ui components
└── lib/                 # Utility functions
```

## Module Descriptions

### 1. Urban Spatial Elements (`/cityinfo`)
Visualizes various urban spatial data layers including:
- Basic Geography (Topography, Geomorphology, River Network, Administrative Boundary, Annual Rainfall)
- Infrastructure (Buildings, Roads, Land Use, Drainage Systems, Defensive Embankments, Service Reservoirs)
- Socioeconomic (Population Density, Economic Data, Industrial & Commercial, Nighttime Light Index, POI)

### 2. Disaster Event Repository (`/disasterinfo`)
Manages historical and stochastic disaster events with:
- Historical disaster event listing and details
- Stochastic event ID input for 10,000-year simulations
- Event filtering by time, type, and region
- Event comparison and export functionality

### 3. Risk Map (`/riskmap`)
Provides multi-hazard risk visualization:
- Multi-hazard selection (Typhoon, Rainstorm, Flood, Geological)
- Exposure analysis (Population, Building Cost, Critical Infrastructure)
- Location-based risk querying
- Risk report generation and download

### 4. Asset Management (`/asset`)
Manages insured assets with:
- Asset import/export functionality
- Asset attribute filtering
- Asset grouping and batch operations
- Detailed asset information display
- Asset and risk zone analysis

### 5. Catastrophe Model (`/model` and `/oasis`)
Handles catastrophe modeling and simulation:
- User authentication (default: admin/123)
- Project creation and management
- Model parameter configuration
- Simulation execution and monitoring
- Result visualization and download

### 6. Accessibility (`/fuzhu`)
Provides auxiliary functionalities:
- Earth-map integration with global weather data
- Warning message center
- User permissions and logs
- System settings

### User Center (`/usercenter`)
Manages user profiles and settings:
- Profile information management
- Account settings (password change, 2FA)
- Notification preferences
- Activity log tracking

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
