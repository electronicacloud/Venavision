# VenaVision: Real-Time NIR Vein Imaging System
VenaVision is a medical instrumentation project designed to assist healthcare professionals in locating veins for venipuncture. By utilizing Near-Infrared (NIR) imaging and advanced digital signal processing, the system enhances the contrast of subcutaneous veins in real-time.

**Overview**

The system captures NIR light reflected from the skin. Deoxygenated hemoglobin in the blood absorbs NIR light more than surrounding tissues, creating a map of the venous structure. This map is then processed through a pipeline of filters to produce a high-contrast projection.

**Key Features**

Real-Time Processing: Low-latency image enhancement using a Raspberry Pi.

Advanced Filtering: Implements Frangi Vesselness Filters and CLAHE for superior vessel extraction.

Web-Based Dashboard: A Flask-powered interface to view the live processed stream on any device within the network.

Hardware Optimized: Specifically tuned for the Raspberry Pi NoIR camera and ARM-based architectures.

**Tech Stack**

Hardware: Raspberry Pi, Pi NoIR Camera V2, 850nm IR LED Array.

Language: Python 3.

Libraries: * OpenCV: Image acquisition and basic transformations.

Scikit-Image: Advanced morphology and Frangi filtering.

Flask: Real-time video streaming server.

NumPy/SciPy: High-performance mathematical operations.

**Image Processing Pipeline**

The project uses a multi-stage pipeline to ensure veins are visible even under challenging lighting:

Grayscale Conversion: Simplifies the data for faster processing.

CLAHE (Contrast Limited Adaptive Histogram Equalization): Balances local contrast to prevent over-exposure.

Frangi Filter: A multiscale filter used to detect tubular structures (veins) based on the Hessian matrix.

Normalization: Scales the output for clear visualization.
