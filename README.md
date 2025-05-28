# DroneForensics

![DroneForensics Logo](https://github.com/username/DroneForensics/raw/main/images/logo.png)

A comprehensive drone forensics analysis tool with an intuitive GUI for extracting, analyzing, and visualizing data from drone flight logs and telemetry dumps.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/downloads/)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Supported Drone Models](#supported-drone-models)
- [Installation](#installation)
- [Usage](#usage)
- [Data Analysis Capabilities](#data-analysis-capabilities)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## Overview

DroneForensics is a specialized tool designed for digital forensic investigators, security researchers, and drone enthusiasts to analyze flight data from various drone models. The tool provides a user-friendly interface for extracting valuable information from drone telemetry dumps, reconstructing flight paths, analyzing payload data, and generating comprehensive reports for investigative purposes.

## Features

- **Intuitive GUI**: User-friendly interface for easy data analysis
- **Multi-format Support**: Import data from CSV, DAT, BIN, and LOG files
- **Flight Path Reconstruction**: Visualize drone flight paths on interactive maps
- **Telemetry Analysis**: Detailed analysis of speed, altitude, battery levels, and other telemetry data
- **Payload Identification**: Identify and analyze payload data (camera, sensors, etc.)
- **Timeline Generation**: Create detailed timelines of drone activities
- **Geospatial Mapping**: Plot flight data on maps with customizable layers
- **Media Extraction**: Extract and analyze embedded media files
- **Anomaly Detection**: Identify unusual patterns or behaviors in flight data
- **Comprehensive Reporting**: Generate detailed PDF/HTML reports for investigations
- **Data Export**: Export processed data in various formats (CSV, KML, JSON)
- **Batch Processing**: Analyze multiple flight logs simultaneously

## Supported Drone Models

DroneForensics supports data extraction and analysis from various popular drone models:

- DJI (Phantom, Mavic, Inspire, Matrice series)
- Parrot (Anafi, Bebop, Disco)
- Yuneec (Typhoon, H520)
- Autel Robotics (EVO series)
- 3DR Solo
- Custom and DIY drones using common flight controllers (Pixhawk, Ardupilot, etc.)

## Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git (optional, for cloning the repository)

### Standard Installation

```bash
# Clone the repository
git clone https://github.com/username/DroneForensics.git
cd DroneForensics

# Create and activate virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch the application
python droneforensics.py
```

### Standalone Executable

For users who prefer not to install Python, standalone executables are available for Windows, macOS, and Linux from the [releases page](https://github.com/username/DroneForensics/releases).

## Usage

### Quick Start

1. Launch DroneForensics
2. Click "Open File" and select your drone data file (CSV, DAT, BIN, LOG)
3. The tool will automatically detect the drone model and data format
4. Navigate through the tabs to access different analysis features:
   - Flight Path: View and analyze the drone's flight path on a map
   - Telemetry: Analyze speed, altitude, battery, and other sensor data
   - Payload: Examine payload information and extracted media
   - Timeline: View a chronological timeline of the drone's activity
   - Report: Generate comprehensive analysis reports

### Command Line Usage

DroneForensics also supports command-line operation for batch processing:

```bash
python droneforensics.py --cli --input flight_log.csv --output report.pdf --format pdf
```

## Data Analysis Capabilities

### Flight Path Reconstruction

- 2D and 3D visualization of flight paths
- Altitude heat mapping
- Speed analysis along flight path
- Waypoint identification
- Home point and return-to-home path analysis
- No-fly zone violation detection

### Telemetry Analysis

- Altitude profiles (relative and absolute)
- Speed analysis (horizontal and vertical)
- Battery consumption patterns
- Motor/ESC performance data
- Signal strength analysis
- Controller input reconstruction
- Sensor data analysis (IMU, barometer, compass)

### Payload Analysis

- Camera operation timeline
- Photo/video geolocation
- Gimbal movement analysis
- Sensor payload data extraction
- Custom payload identification

### Timeline Features

- Chronological event reconstruction
- Anomaly highlighting
- Correlation of telemetry events with payload operation
- Time-based filtering and searching
- Event categorization and tagging

## Screenshots

![Main Interface](https://github.com/username/DroneForensics/raw/main/images/screenshot1.png)
*Main interface showing flight path reconstruction*

![Telemetry Analysis](https://github.com/username/DroneForensics/raw/main/images/screenshot2.png)
*Telemetry data analysis with interactive graphs*

![Report Generation](https://github.com/username/DroneForensics/raw/main/images/screenshot3.png)
*Sample forensic report generation interface*

## Contributing

Contributions to DroneForensics are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please ensure your code follows the project's coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Project Structure

```
DroneForensics/
├── droneforensics.py         # Main application entry point
├── requirements.txt          # Python dependencies
├── LICENSE                   # License file
├── README.md                 # This readme file
├── docs/                     # Documentation
├── src/
│   ├── gui/                  # GUI components
│   │   ├── __init__.py
│   │   ├── main_window.py
│   │   ├── map_view.py
│   │   ├── telemetry_view.py
│   │   ├── timeline_view.py
│   │   └── report_view.py
│   ├── core/                 # Core functionality
│   │   ├── __init__.py
│   │   ├── parser.py         # Data parser for different formats
│   │   ├── analyzer.py       # Data analysis engine
│   │   ├── mapper.py         # Geospatial mapping functions
│   │   └── reporter.py       # Report generation
│   ├── models/               # Data models
│   │   ├── __init__.py
│   │   ├── telemetry.py
│   │   ├── flight_path.py
│   │   └── payload.py
│   └── utils/                # Utility functions
│       ├── __init__.py
│       ├── file_utils.py
│       ├── geo_utils.py
│       └── time_utils.py
├── tests/                    # Unit tests
└── resources/                # Application resources
    ├── icons/
    ├── sample_data/
    └── templates/
```
