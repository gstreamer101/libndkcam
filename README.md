# libndkcam

`libndkcam` is a GObject-based C library that wraps the Android Camera NDK (Camera2 NDK) API to provide a clean, reusable interface for native Linux and Android applications.

It is designed as the core library powering the `ndkcamsrc` GStreamer plugin but can also be used independently in any GObject-based project requiring access to native Android camera streams.

## Key Features

- Native C API for accessing Android Camera via the Camera NDK (Camera2 NDK)
- GObject wrappers for seamless integration with GLib- and GStreamer-based systems
- Modular, extensible architecture with a clean abstraction layer
- Supports advanced camera features (e.g., capture sessions, multiple streams, format negotiation) without exposing low-level NDK complexity

## License

This project is licensed under the Apache License 2.0.
