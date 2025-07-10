# 🚀 RTX Diagnostic Tool

<div align="center">

![RTX Diagnostic Tool](https://img.shields.io/badge/RTX-Diagnostic%20Tool-00BCD4?style=for-the-badge&logo=nvidia&logoColor=white) ![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white) ![PySide6](https://img.shields.io/badge/PySide6-UI%20Framework-41CD52?style=for-the-badge&logo=qt&logoColor=white) ![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**A comprehensive real-time monitoring and diagnostic tool for NVIDIA RTX graphics cards**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Screenshots](#-screenshots) • [Contributing](#-contributing)

</div>

---

## 📋 Table of Contents

- [🎯 Overview](#-overview)
- [✨ Features](#-features)
- [🎨 Status Indicators](#-status-indicators)
- [⚙️ Installation](#️-installation)
- [🚀 Usage](#-usage)
- [📊 Monitoring Panels](#-monitoring-panels)
- [🔧 GPU Feature Detection](#-gpu-feature-detection)
- [🛠️ Technical Requirements](#️-technical-requirements)
- [📸 Screenshots](#-screenshots)
- [🤝 Contributing](#-contributing)
- [🐛 Troubleshooting](#-troubleshooting)
- [📈 Roadmap](#-roadmap)
- [📄 License](#-license)
- [💝 Acknowledgments](#-acknowledgments)

---

## 🎯 Overview

RTX Diagnostic Tool is a powerful, real-time monitoring application specifically designed for NVIDIA RTX graphics cards. Built with Python and PySide6, it provides comprehensive hardware monitoring, feature detection, and diagnostic capabilities in an intuitive, modern interface.

### Why RTX Diagnostic Tool?

- **RTX-Focused**: Specifically optimized for RTX 20, 30, and 40 series GPUs
- **Real-Time Monitoring**: Live updates of all critical GPU metrics
- **Multi-Fan Support**: Individual monitoring for cards with multiple cooling fans
- **Feature Detection**: Comprehensive RTX feature and capability analysis
- **Beautiful UI**: Modern, dark-themed interface with color-coded indicators
- **No Dependencies**: Works with standard NVIDIA drivers

---

## ✨ Features

### 🌡️ **Real-Time GPU Monitoring**

- **Temperature Tracking**: Precise GPU core temperature monitoring
- **Performance Metrics**: GPU usage, memory utilization, and clock speeds
- **Power Monitoring**: Real-time power draw and power limit tracking
- **Memory Analysis**: Detailed VRAM usage in MB and GB formats

### 🌪️ **Advanced Cooling System Monitoring**

- **Multi-Fan Support**: Individual monitoring for up to 6 cooling fans
- **Fan Speed & RPM**: Real-time fan speed percentages and calculated RPM values
- **Cooling Efficiency**: Smart efficiency calculation based on temperature and fan performance
- **Fan Curve Analysis**: Model-specific fan behavior understanding

### 🎮 **RTX Feature Detection**

- **Ray Tracing**: Hardware ray tracing capability detection
- **DLSS Support**: AI super resolution feature availability
- **Resizable BAR**: Smart Access Memory detection and status
- **CUDA Cores**: Accurate core count for your specific GPU model
- **G-Sync Compatibility**: Variable refresh rate support detection

### 🔧 **Hardware Capabilities**

- **Power Management**: Adaptive power scaling analysis
- **DSR Support**: Dynamic Super Resolution capability
- **HDR Support**: High Dynamic Range display compatibility
- **Multi-Display**: Multiple monitor support detection
- **GPU Boost**: Automatic overclocking feature status

### 📊 **Advanced Diagnostics**

- **Driver Information**: Current driver version and compatibility
- **Clock Monitoring**: Base and boost clock frequencies
- **Memory Clocks**: VRAM frequency monitoring
- **V-Sync Status**: Vertical synchronization configuration
- **Low Latency Mode**: NVIDIA Reflex support detection

---

## 🎨 Status Indicators

### Color-Coded System

| Color                        | Meaning                  | Usage                             |
| ---------------------------- | ------------------------ | --------------------------------- |
| 🟢**Green (#4CAF50)**  | Active/Enabled/Supported | Features working optimally        |
| 🟡**Amber (#FFC107)**  | Inactive/Disabled        | Features available but not active |
| 🔴**Red (#F44336)**    | Error/Not Supported      | Issues or unsupported features    |
| 🔵**Cyan (#00BCD4)**   | Primary Metrics          | Main GPU indicators               |
| 🟣**Purple (#9C27B0)** | Clock Frequencies        | GPU and memory clocks             |
| 🟠**Orange (#FF9800)** | Power/Thermal            | Power and temperature metrics     |

### Fan Color Coding

| Fan   | Color        | Hex Code |
| ----- | ------------ | -------- |
| Fan 1 | 🔵 Cyan      | #00BCD4  |
| Fan 2 | 🟢 Green     | #4CAF50  |
| Fan 3 | 🟠 Orange    | #FF9800  |
| Fan 4 | 🟣 Purple    | #9C27B0  |
| Fan 5 | 🌸 Pink      | #E91E63  |
| Fan 6 | 🔘 Blue Grey | #607D8B  |

---

## ⚙️ Installation

### Prerequisites

- **Operating System**: Windows 10/11
- **Python**: 3.8 or higher
- **GPU**: NVIDIA RTX series (20xx, 30xx, 40xx)
- **Drivers**: Latest NVIDIA drivers with nvidia-smi

### Method 1: Clone Repository

```bash
# Clone the repository
git clone https://github.com/partybrasil/RTX-DIAG.git
cd RTX-DIAG

# Install required dependencies
pip install -r requirements.txt

# Run the application
python RTX-DIAG.py
```

### Method 2: Direct Download

1. Download the latest release from [Releases](https://github.com/partybrasil/RTX-DIAG/releases "go to Releases")
2. Extract the files to your desired location
3. Install dependencies: `pip install PySide6 psutil nvidia-ml-py`
4. Run: `python RTX-DIAG.py`

### Dependencies

```txt
nvidia-ml-py==12.575.51
psutil==7.0.0
PySide6==6.9.1
```

---

## 🚀 Usage

### Basic Operation

1. **Launch Application**: Run `RTX-DIAG.py`
2. **GPU Detection**: The app automatically detects your RTX GPU
3. **Real-Time Monitoring**: All metrics update every second
4. **Feature Analysis**: GPU features are analyzed and displayed

### Interface Overview

```


┌─────────────────────────────────────────────────────────────┐
│  RTX Diagnostic Dashboard              ✓ RTX 4090 Detected  │
├─────────────────────────────────┬───────────────────────────┤
│                                 │                           │
│  🌪️ Cooling System              │  🎮 GPU Features &        │
│  ├─ Fan 1: 65% (1560 RPM)       │     Capabilities          │
│  ├─ Fan 2: 67% (1608 RPM)       │  ├─ Ray Tracing: ✅       │
│  └─ Fan 3: 63% (1512 RPM)       │  ├─ DLSS: ✅              │
│                                 │  ├─ Resizable BAR: ✅     │
│  📊 GPU Metrics                 │  ├─ CUDA Cores: 16384     │
│  ├─ Temperature: 68°C           │  └─ Power Management: ⚡   │
│  ├─ GPU Usage: 76%              │                           │
│  ├─ Memory: 8.2/24.0 GB        │  🔧 Advanced Features     │
│  ├─ Power: 285W / 450W         │  ├─ G-Sync: ✅            │
│  └─ GPU Clock: 2520 MHz        │  ├─ HDR Support: ✅       │
│                                 │  └─ Low Latency: ⚡       │
└─────────────────────────────────┴───────────────────────────┘
```

### Key Controls

- **🔄 Refresh**: Manual refresh of GPU features
- **Auto-Update**: Real-time monitoring (1-second intervals)
- **Scroll**: Navigate through all monitoring data
- **Hover**: View detailed descriptions of features

---

## 📊 Monitoring Panels

### Cooling System Panel

- **Individual Fan Monitoring**: Each fan displays speed percentage and calculated RPM
- **Cooling Efficiency**: Overall system cooling performance
- **Temperature Correlation**: Fan response to thermal conditions
- **Zero RPM Detection**: Automatic detection of fan stop modes

### GPU Metrics Panel

- **Performance Indicators**: Load, clock speeds, and utilization
- **Memory Management**: VRAM usage with GB/MB precision
- **Thermal Monitoring**: Core temperature with safety thresholds
- **Power Analysis**: Real-time power consumption and limits

### Detailed Information Panel

- **Clock Frequencies**: Current and maximum GPU/Memory clocks
- **Driver Information**: Version and compatibility status
- **Hardware Specifications**: Model-specific technical data
- **Capacity Metrics**: Total memory and processing capabilities

---

## 🔧 GPU Feature Detection

### Automatic Detection Features

| Feature                    | Detection Method        | Status Types             |
| -------------------------- | ----------------------- | ------------------------ |
| **Resizable BAR**    | BAR1 Memory Analysis    | Enabled/Disabled/Unknown |
| **Ray Tracing**      | GPU Model Database      | Supported/Not Supported  |
| **DLSS**             | RTX Series Detection    | Supported/Not Supported  |
| **CUDA Cores**       | Model-Specific Database | Exact Count              |
| **Power Management** | NVML/Registry Query     | Active/Adaptive/Disabled |
| **G-Sync**           | Generation Detection    | Supported/Not Supported  |
| **HDR Support**      | Architecture Analysis   | Supported/Limited        |
| **Low Latency**      | Reflex Capability       | Available/Not Supported  |

### Manual Refresh

Click the **🔄 Refresh** button to re-analyze GPU features and update detection results.

---

## 🛠️ Technical Requirements

### Minimum System Requirements

- **OS**: Windows 10 (1903+) or Windows 11
- **RAM**: 4GB system memory
- **GPU**: NVIDIA RTX 2060 or higher
- **Drivers**: NVIDIA Game Ready 461.09+
- **Python**: 3.8+ with pip

### Recommended System Requirements

- **OS**: Windows 11 latest version
- **RAM**: 8GB+ system memory
- **GPU**: NVIDIA RTX 3070 or higher
- **Drivers**: Latest NVIDIA Studio/Game Ready drivers
- **Python**: 3.11+ with virtual environment

### Supported GPU Models

- **RTX 40 Series**: 4090, 4080, 4070 Ti, 4070, 4060 Ti, 4060
- **RTX 30 Series**: 3090 Ti, 3090, 3080 Ti, 3080, 3070 Ti, 3070, 3060 Ti, 3060
- **RTX 20 Series**: 2080 Ti, 2080 Super, 2080, 2070 Super, 2070, 2060 Super, 2060
- **Professional**: RTX A-series, Quadro RTX series

---

## 🤝 Contributing

We welcome contributions to improve RTX Diagnostic Tool! Here's how you can help:

### Ways to Contribute

- 🐛 **Bug Reports**: Found an issue? Report it!
- 💡 **Feature Requests**: Have an idea? Share it!
- 🔧 **Code Contributions**: Submit pull requests
- 📖 **Documentation**: Improve docs and tutorials
- 🧪 **Testing**: Test on different GPU models

### Development Setup

```bash
# Fork and clone the repository
git clone https://github.com/partybrasil/RTX-DIAG.git
cd RTX-DIAG

# Create virtual environment
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Linux/Mac

# Install development dependencies
pip install -r requirements-dev.txt

# Make your changes and test
python RTX-DIAG.py

# Submit a pull request
```

### Code Style

- Follow PEP 8 guidelines
- Use meaningful variable names
- Add comments for complex logic
- Include docstrings for functions
- Test on multiple GPU models when possible

### Pull Request Process

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 🐛 Troubleshooting

### Common Issues

#### "No GPU Detected"

- **Solution**: Ensure NVIDIA drivers are installed and up to date
- **Check**: Run `nvidia-smi` in command prompt
- **Verify**: GPU is RTX series (GTX not supported)

#### "NVML Not Available"

- **Solution**: Install nvidia-ml-py: `pip install nvidia-ml-py`
- **Alternative**: App will use nvidia-smi as fallback
- **Note**: Some features may be limited without NVML

#### Incorrect Fan Count

- **Cause**: Model database may not include your specific GPU variant
- **Solution**: Fan count auto-detects from hardware when possible
- **Workaround**: Manual override in future versions

#### Permission Errors

- **Solution**: Run as administrator on some systems
- **Cause**: Registry access for some NVIDIA settings
- **Alternative**: Limited functionality without admin rights

### Getting Help

1. **Check Issues**: Browse existing [GitHub Issues](https://github.com/partybrasil/RTX-DIAG/issues)
2. **Create Issue**: Report bugs with system details
3. **Community**: Join discussions and share experiences
4. **Documentation**: Review this README and inline help

---

## 📈 Roadmap

### Version 2.0 (Upcoming)

- [ ] **Multi-GPU Support**: Monitor multiple RTX cards
- [ ] **Historical Data**: Performance graphs and logging
- [ ] **Custom Alerts**: Temperature and performance warnings
- [ ] **Export Data**: CSV/JSON data export functionality

### Version 2.1 (Future)

- [ ] **Overclocking Tools**: Safe overclocking interface
- [ ] **Fan Curve Editor**: Custom fan speed profiles
- [ ] **Game Integration**: Per-game monitoring and optimization
- [ ] **Mobile App**: Remote monitoring via smartphone

### Version 3.0 (Vision)

- [ ] **AI Optimization**: Machine learning performance optimization
- [ ] **Cloud Sync**: Settings and data synchronization
- [ ] **Team Features**: Multi-user monitoring for workstations
- [ ] **Plugin System**: Third-party extensions and integrations

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/partybrasil/RTX-DIAG?tab=MIT-1-ov-file#readme "go to MIT LICENSE") file for details.

---

## 💝 Acknowledgments

<div align="center">

### Thank You for Using RTX Diagnostic Tool! ❤️

**Your support and feedback make this project possible**

</div>

We extend our heartfelt gratitude to:

- 🎮 **NVIDIA** - For creating amazing RTX technology and providing development tools
- 🐍 **Python Community** - For the incredible ecosystem of libraries and frameworks
- 🖥️ **Qt/PySide6 Team** - For the powerful UI framework that makes beautiful interfaces possible
- 👥 **Open Source Community** - For inspiration, libraries, and collaborative spirit
- 🧪 **Beta Testers** - Early adopters who help make the tool better
- 📝 **Contributors** - Everyone who submits code, reports bugs, and improves documentation
- ❤️ **Users Like You** - For choosing RTX Diagnostic Tool for your GPU monitoring needs

### Special Thanks

- **psutil** - System and process utilities
- **nvidia-ml-py** - NVIDIA Management Library Python bindings
- **PySide6** - Qt for Python UI framework
- **GitHub** - Hosting and collaboration platform

### Made with ❤️ by PartyBrasil

This tool is built with passion for PC gaming, professional workstations, and the amazing RTX ecosystem. Every line of code is written with care to provide you with the best GPU monitoring experience possible.

**If RTX Diagnostic Tool has helped you monitor your GPU, optimize your system, or simply learn more about your hardware, we'd love to hear about it!**

---

<div align="center">

**⭐ If you find this tool useful, please consider starring the repository! ⭐**

[![GitHub stars](https://img.shields.io/github/stars/partybrasil/RTX-DIAG?style=social)](https://github.com/partybrasil/RTX-DIAG/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/partybrasil/RTX-DIAG?style=social)](https://github.com/partybrasil/RTX-DIAG/network)

**Built with 💚 for the RTX community**

[🏠 Home](https://github.com/partybrasil/RTX-DIAG) • [📋 Issues](https://github.com/partybrasil/RTX-DIAG/issues) • [🚀 Releases](https://github.com/partybrasil/RTX-DIAG/releases) • [📖 Wiki](https://github.com/partybrasil/RTX-DIAG/wiki)

</div>
