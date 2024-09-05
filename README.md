```markdown
# OpenCV Repository

This repository contains various OpenCV examples and presentations for both Windows and Linux platforms. It includes a collection of C++ and Python examples as well as Docker-based setups for basic image processing tasks.

## What is OpenCV?

[OpenCV](https://opencv.org/) (Open Source Computer Vision Library) is an open-source computer vision and machine learning software library. OpenCV was built to provide a common infrastructure for computer vision applications and to accelerate the use of machine perception in commercial products. Being open-source, it supports a wide variety of programming languages like C++, Python, Java, and MATLAB and runs on multiple platforms such as Windows, Linux, and macOS.

### Official Website:
- [OpenCV Official Website](https://opencv.org/)

## Installation

Instalación en Linux

En Linux, la instalación de OpenCV generalmente se realiza compilando desde el código fuente o utilizando el gestor de paquetes del sistema.

    Instala dependencias:

   ```bash
sudo apt-get install build-essential cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
   ```
Clona el repositorio de OpenCV y opencv_contrib:

   ```bash
git clone https://github.com/opencv/opencv.git
git clone https://github.com/opencv/opencv_contrib.git
   ```
Crea una carpeta de compilación y configura CMake:

   ```bash
cd opencv
mkdir build
cd build
cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules ..
   ```

Compila OpenCV:

   ```bash
    make -j$(nproc)
    sudo make install
   ```

### Linux

1. Install OpenCV via the package manager:
   ```bash
   sudo apt update
   sudo apt install libopencv-dev python3-opencv
   ```

2. For examples using **Qt Creator**, refer to the `QTOpenCV-Linux` folder in this repository.

## Project Structure

- **Presentaciones**: This folder contains presentations, including an internal summary of OpenCV. The presentation `NerdTalk - OpenCV` provides an overview of OpenCV's functionalities and use cases.
  
- **Ejemplos**: This folder includes a variety of OpenCV examples for different platforms and languages:
  
  - **TestOpenCV-Windows**: A Qt Creator project that captures images from the camera and applies a few filters, like edge detection. This example is built for Windows.
  
  - **QTOpenCV-Linux**: Similar to the previous project, but developed for Linux environments using Qt Creator.
  
  - **Prueba_OpenCV_Docker**: A simple example that runs inside a Docker container, where an image is read and processed with edge detection.
  
  - **opencv1.cpp, opencv2.cpp, opencv3.cpp**: Basic OpenCV examples written in C++.
  
  - **opencv_harry.py**: A fun Python example that uses a preloaded image instead of a solid color background, mimicking an invisibility cloak effect (similar to the magic from *Harry Potter*).

## Usage

### Running Examples in Qt Creator
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/opencv.git
   ```

2. Open the Qt Creator project files in either the `TestOpenCV-Windows` or `QTOpenCV-Linux` folders.

3. Build and run the project to see the camera capture and image filters in action.

### Running the Docker Example
1. Navigate to the `Prueba_OpenCV_Docker` directory:
   ```bash
   cd Ejemplos/Prueba_OpenCV_Docker
   ```

2. Build the Docker image:
   ```bash
   docker build -t opencv-example .
   ```

3. Run the Docker container:
   ```bash
   docker run -it opencv-example
   ```

4. The image will be read, and edge detection will be applied.

## Presentations

The `Presentaciones` folder includes a presentation titled **"NerdTalk - OpenCV"**, which provides a brief summary of OpenCV's capabilities and use cases. You can open it using any software that supports PowerPoint files.

