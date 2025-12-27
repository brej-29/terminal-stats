# Terminal Stats

A lightweight, real-time system monitoring tool that displays CPU, memory, network, and process statistics directly in your terminal with a clean, organized interface.

## Features

- **Real-time CPU Monitoring**: Track overall CPU usage and per-core statistics
- **Memory Management**: Monitor RAM utilization, swap space, and memory breakdown
- **Network Statistics**: View network interfaces, bandwidth usage, and connection stats
- **Process Monitoring**: Display top processes by CPU and memory consumption
- **System Information**: Quick overview of system details, uptime, and load averages
- **Auto-refresh**: Continuously update statistics with configurable refresh intervals
- **Cross-platform Support**: Works on Linux, macOS, and Windows
- **Minimal Dependencies**: Lightweight with minimal external library requirements

## Installation

### Prerequisites
- Python 3.7+
- pip (Python package installer)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/brej-29/terminal-stats.git
cd terminal-stats
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

Or install directly:
```bash
pip install psutil
```

## Usage

### Basic Usage
```bash
python terminal_stats.py
```

### Options
```bash
# Display help menu
python terminal_stats.py --help

# Set refresh interval (in seconds)
python terminal_stats.py --interval 2

# Monitor specific process by name
python terminal_stats.py --process python

# Verbose mode with detailed information
python terminal_stats.py --verbose
```

## Requirements

- `psutil>=5.9.0` - System and process utilities library

## Configuration

Create a `config.json` file in the repository root to customize behavior:

```json
{
  "refresh_interval": 1.5,
  "max_processes": 10,
  "show_network": true,
  "show_memory_breakdown": true,
  "units": "GB"
}
```

## Architecture

```
terminal-stats/
├── terminal_stats.py      # Main entry point
├── system_monitor.py      # Core monitoring logic
├── utils.py              # Utility functions
├── requirements.txt      # Dependencies
├── config.json          # Configuration file
└── README.md            # This file
```

## Key Modules

- **System Monitor**: Collects and aggregates system statistics using psutil
- **Display Manager**: Formats and renders data in the terminal
- **Process Handler**: Tracks and filters process information
- **Network Monitor**: Monitors network interfaces and bandwidth

## Performance

- Minimal CPU overhead (<1% on most systems)
- Memory footprint: ~15-25 MB
- Suitable for long-running monitoring sessions

## Troubleshooting

### Permission Denied Errors
Some system metrics require elevated privileges. Run with `sudo` if needed:
```bash
sudo python terminal_stats.py
```

### Missing Modules
Ensure all dependencies are installed:
```bash
pip install --upgrade psutil
```

### High CPU Usage
Reduce the refresh interval or disable verbose mode:
```bash
python terminal_stats.py --interval 5
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

**Brejesh Balakrishnan** - [GitHub](https://github.com/brej-29)

## Acknowledgments

- Built with Python and psutil library
- Inspired by system monitoring tools like `top`, `htop`, and `glances`
- Thanks to the open-source community

## Support

For issues, questions, or suggestions, please open an [issue](https://github.com/brej-29/terminal-stats/issues) on GitHub.

---

**Last Updated**: December 2025
