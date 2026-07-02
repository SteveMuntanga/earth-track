# earth-track

**earth-track** is a lightweight Linux command-line utility that opens geographic coordinates directly in Google Earth Pro.

Google Earth Pro does not provide a documented command-line option for opening coordinates directly. **earth-track** bridges that gap by accepting coordinates in `latitude,longitude` format, automatically generating a KML file, and launching Google Earth Pro at the requested location.

It is designed for OSINT analysts, digital investigators, GIS professionals, security researchers, and anyone who frequently works with geographic coordinates.

## Features

* Lightweight Bash script
* Opens coordinates directly in Google Earth Pro
* Accepts coordinates in `latitude,longitude` format
* Automatically generates a standards-compliant KML file
* Reuses a cached KML file for efficiency
* No external dependencies beyond Google Earth Pro

## Requirements

* Linux
* Google Earth Pro

## Installation

Clone the repository:

```bash
git clone https://github.com/stevemuntanga/earth-track.git
cd earth-track
```

Make the script executable:

```bash
chmod +x earth-track
```

Install it system-wide:

```bash
sudo cp earth-track /usr/local/bin/
```

## Usage

Launch Google Earth Pro at a specific location:

```bash
earth-track -26.2023,28.0436
```

Example:

```bash
earth-track 51.5007,-0.1246
```

The script will:

1. Parse the supplied coordinates.
2. Generate a KML file in `~/.cache/google-earth/`.
3. Launch Google Earth Pro centered on the specified location.

## Why earth-track?

While Google Earth Pro can open KML files, it lacks a simple command-line interface for opening coordinates directly. This utility eliminates the extra steps by converting coordinates into a temporary KML file behind the scenes.

This makes it ideal for automation, scripting, and OSINT workflows.

## Roadmap

Future enhancements may include:

* Support for Google Maps URLs
* Support for OpenStreetMap URLs
* Support for Bing Maps URLs
* Support for Plus Codes
* Address and place-name lookup
* KML/KMZ input support
* Multiple destination applications (Google Earth Web, Marble, etc.)

Contributions and feature requests are welcome.

## License

This project is licensed under the MIT License.
