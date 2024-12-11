# Performance

A lightweight performance monitoring library for Apple platforms that helps track various system metrics including CPU usage, memory consumption, FPS, network traffic, and system wakeups.

## Features

- 📊 CPU Usage Monitoring
- 🎯 FPS (Frames Per Second) Tracking
- 💾 Memory Usage Statistics
- 🌐 Network Traffic Analysis
- ⚡ System Wakeups Detection
- ⏱️ System Uptime Information

## Requirements

- iOS 13.0+ / tvOS 13.0+
- Swift 5.5+
- Xcode 13.0+

## Installation

### Swift Package Manager

Add the following to your `Package.swift` file:

```swift
dependencies: [
    .package(url: "https://github.com/MichaelLedger/Performance.git", from: "1.1.2")
]
```

## Usage

### Basic Setup

```swift
import Performance

let performance = Performance()
```

### FPS Usage

Monitor FPS:

```swift
if let fps = performance.fps {
    print("[Performance] FPS: \(fps)")
}
```

### CPU Usage

Monitor CPU usage percentage:

```swift
if let cpuUsage = performance.cpuUsage {
    print("[Performance] CPU Usage: \(cpuUsage)%")
}
```

### Memory Usage

Monitor memory usage:

```swift
if let memoryUsage = performance.memoryUsage {
    print("[Performance] Memory Usage: \(memoryUsage) MB")
}
```

### System Wakeups

Monitor system wakeups:

```swift
if let interruptWakeups = performance.interruptWakeups {
    print("[Performance] Interrupt Wakeups: \(interruptWakeups)")
}
```

### System Uptime (include/without sleep time)

Monitor system uptime:

```swift
if let uptime = performance.uptime {
    print("[Performance] System uptime include sleep time: \(uptime) seconds")
}
if let systemUptime = performance.systemUptime {
    print("[Performance] System uptime without sleep time: \(systemUptime) seconds")
}
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

MichaelLedger@163.com

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
