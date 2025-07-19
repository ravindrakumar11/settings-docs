# macOS System Monitoring Tools Guide

## Overview
This guide covers a collection of powerful command-line tools for visualizing and monitoring system resources on macOS. These tools provide interactive and user-friendly interfaces for monitoring CPU, memory, disk usage, and network activity.

## Tools

### 1. btop
A more advanced and visually appealing alternative to top.

**Installation:**
```bash
brew install btop
```

**Usage:**
```bash
btop
```

**Features:**
- Beautiful CPU, memory, and process monitoring
- Resource graphs and usage statistics
- Customizable interface
- Process management capabilities
- Keyboard shortcuts: 
  - `q` to quit
  - `h` for help
  - `m` to change view mode

### 2. glances
A cross-platform monitoring tool that shows a wide variety of system information.

**Installation:**
```bash
brew install glances
```

**Usage:**
```bash
glances
```

**Features:**
- System overview in a single screen
- CPU, memory, disk I/O, and network statistics
- Process monitoring with detailed information
- Web interface available (run with `glances -w`)
- Export capabilities to various formats
- Keyboard shortcuts:
  - `q` to quit
  - `h` for help
  - `1-5` to sort processes

### 3. ncdu (NCurses Disk Usage)
An interactive disk usage analyzer with a text-based interface.

**Installation:**
```bash
brew install ncdu
```

**Usage:**
```bash
ncdu [path]
```

**Features:**
- Interactive navigation through directories
- Size-sorted file and directory listing
- Quick identification of large files
- Keyboard shortcuts:
  - `q` to quit
  - `?` for help
  - Arrow keys for navigation
  - Return to enter directories

### 4. iftop
Network bandwidth monitoring tool with real-time graphs.

**Installation:**
```bash
brew install iftop
```

**Usage:**
```bash
sudo iftop
```

**Features:**
- Real-time network usage visualization
- Shows connections between hosts
- Bandwidth usage per connection
- Cumulative bandwidth usage statistics
- Keyboard shortcuts:
  - `q` to quit
  - `h` for help
  - `n` to toggle DNS resolution
  - `s` to toggle show/hide source ports

## Basic System Commands

Besides these specialized tools, macOS also provides built-in commands for quick system information:

```bash
# CPU and Memory snapshot
top -l 1 -n 0

# Disk space usage
df -h

# Memory statistics
vm_stat

# System hardware information
system_profiler SPHardwareDataType
```

## Tips for Usage

1. **Resource Intensive Monitoring:**
   - For continuous monitoring, `btop` or `glances` are recommended
   - They provide comprehensive system information in real-time

2. **Disk Space Analysis:**
   - Use `ncdu` for interactive exploration
   - Great for finding large files and cleaning up space

3. **Network Monitoring:**
   - `iftop` requires sudo privileges
   - Best for real-time network traffic analysis

4. **Performance Consideration:**
   - These tools themselves consume some system resources
   - For minimal impact, use built-in commands for quick checks
   - For long-term monitoring, consider using `Activity Monitor.app`

## Key Benefits

- Real-time visualization of system resources
- Interactive interfaces for better user experience
- Detailed system information in organized views
- Helpful for system troubleshooting and optimization

## Notes

- All these tools can be installed via Homebrew
- Most tools support extensive customization
- Consider system security when running tools with sudo privileges
- All tools support help screens for learning more features
