# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a web-based subnet calculator tool that helps network administrators design and visualize IP subnets. It supports multiple cloud provider modes (AWS, Azure, GCP, OCI) with different subnet reservation rules.

## Key Files and Structure

- `dist/index.html` - Main application entry point
- `dist/js/main.js` - Core JavaScript logic including subnet calculations
- `README.md` - Project documentation with cloud subnet specifications

## Cloud Subnet Modes

The application supports 5 subnet modes with different address reservation rules:
1. **Standard** - Reserves 2 addresses (network + broadcast)
2. **AWS** - Reserves 5 addresses (network + 3 reserved + broadcast)
3. **Azure** - Reserves 5 addresses (network + 3 reserved + broadcast)
4. **GCP** - Reserves 4 addresses (network + 2 reserved + broadcast)
5. **OCI** - Reserves 3 addresses (network + 1 reserved + broadcast)

## Key Functions

The main subnet calculation functions are in `dist/js/main.js`:
- `subnet_usable_first(network, netSize, operatingMode)` - Calculates first usable IP
- `subnet_usable_last(network, netSize, operatingMode)` - Calculates last usable IP
- `subnet_last_address(network, netSize)` - Calculates last IP in subnet

## Development Workflow

To build and run:
```bash
cd src
npm install
npm run build
npm start
```

The application will be available at `./dist/index.html` in a browser.