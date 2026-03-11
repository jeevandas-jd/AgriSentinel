# AgriSentinel
### Satellite-Guided Crop Damage Verification System

AgriSentinel is an AI-powered agricultural damage assessment platform that integrates satellite intelligence and mobile computer vision to automate crop loss verification for insurance and government recovery programs.

The system creates a **Top-Down to Ground-Truth pipeline** where satellite data detects potential crop damage zones and a mobile application guides farmers to collect AI-verifiable ground evidence.

---

# 1. Objectives

- Automate crop damage detection using satellite imagery.
- Reduce manual field inspections by government officials.
- Provide scientifically verified evidence for insurance claims.
- Enable faster compensation for farmers affected by wildlife conflict and natural disasters.

---

# 2. System Architecture

The platform consists of three major modules.

## 2.1 Satellite Scout (Macro Analysis)

Detects potential crop damage areas using satellite imagery.

Functions:

- NDVI based crop health monitoring
- Delta NDVI change detection
- Identification of damage hotspots
- Satellite imagery comparison (before/after)

Technologies:

- Google Earth Engine
- Planet NICFI satellite imagery
- Python
- Geospatial analysis

Output:

- Top damage hotspots
- GPS coordinates sent to mobile app

---

## 2.2 Mobile Truth Walk (Ground Verification)

Guides the farmer to satellite-detected hotspots and collects ground evidence.

Functions:

- GPS guided navigation to damage location
- On-device image analysis
- Semantic segmentation for damaged crops
- Healthy vs destroyed pixel ratio
- Tree canopy loss estimation

Technologies:

- Flutter mobile app
- TensorFlow Lite
- U-Net segmentation model
- GPS and compass sensors

Output:

- Verified damage images
- AI damage estimation
- Geotagged evidence

---

## 2.3 Smart Claims Engine

Generates a verified claim dossier for insurance and government review.

Functions:

- Document OCR verification
- Land ownership validation
- Damage cause classification
- Automated report generation

Technologies:

- Python backend
- Firebase Firestore
- Firebase Storage
- OCR pipeline

Output:

- AI verified claim report
- Evidence linked with satellite and ground data
- AIMS compliant claim dossier PDF

---

# 3. Database Components

Main data entities:

- Farmers
- Farm Plots
- Satellite Analysis
- Damage Reports
- Evidence
- Claim Dossier

All data is stored using Firebase Firestore and linked to cloud storage for imagery and documents.

---

# 4. AI Models

## Satellite Analysis

- NDVI calculation
- Vegetation health anomaly detection

## Mobile Vision

- U-Net semantic segmentation
- Crop damage pixel classification

## Future Work

- Damage cause classification
- Wildlife damage detection
- Flood vs wind damage identification

---

# 5. Development Phases

## Phase 1: Satellite Detection

- Setup Google Earth Engine
- Fetch satellite imagery
- Implement NDVI analysis
- Detect crop health anomalies

## Phase 2: Mobile Evidence Collection

- Build Flutter application
- Implement GPS guided hotspot navigation
- Integrate camera capture
- Implement TFLite segmentation model

## Phase 3: Claim Verification

- Document OCR pipeline
- Database schema
- Evidence storage
- Claim report generation

## Phase 4: Smart Claim Generation

- AI-based damage assessment
- Automatic PDF claim dossier
- Insurance claim format generation

---

# 6. Expected Impact

For Farmers:

- Faster insurance payouts
- Reduced manual inspection delays
- Objective crop damage evidence

For Government:

- Reduced fraudulent claims
- Automated damage verification
- Improved agricultural disaster response

---

# 7. Future Extensions

- Wildlife detection using drone imagery
- Temporal crop health modeling
- Integration with government crop insurance platforms
- Satellite guided disaster early warning system

---

# 8. Tech Stack

AI / Data Science
- Python
- PyTorch / TensorFlow
- U-Net
- YOLOv8

Remote Sensing
- Google Earth Engine
- Planet NICFI imagery

Mobile
- Flutter
- TensorFlow Lite

Cloud
- Firebase Firestore
- Firebase Storage
