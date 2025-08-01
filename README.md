# 🗺️ AtlasPipe — Geospatial ETL Pipeline

A modular ETL pipeline for extracting, transforming, and loading geospatial data from heterogeneous sources into ArcGIS SDE.

## 💡 Philosophy

Simplicity over complexity. Each task is discrete and standards-driven. YAML-configured, task-executed, and GIS-native.

## 🚀 Tasks

```bash
python run.py --download    # Fetch all data sources
python run.py --process     # Transform to target schema
python run.py --load_sde    # Load into SDE geodatabase
python run.py --cleanup     # Remove scratch data
python run.py               # Full ETL sequence

🧱 Architecture
text
Copy code
config.yaml
├── handlers/     # OGC, ArcGIS, REST, HTTP, Atom
├── processors/   # ArcPy geoprocessing
├── loaders/      # SDE writers
└── utils/        # Logging, naming, config, cleanup

⚙️ Prerequisites
ArcGIS Pro 3.3 (Python 3.11, arcpy)

Valid SDE connection

File system access

✅ Configuration
See config.yaml for source definitions and workspace paths.

🧪 Testing
Malformed config handling

Network/service outages

Data with Swedish characters

Geometry issues, field validation
