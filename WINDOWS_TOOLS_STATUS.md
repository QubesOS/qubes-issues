# qubes-windows-tools: Windows 10/11 support status

Tracking issue: QubesOS/qubes-issues#2843

## Current status

Windows 10/11 support is under development. Do not use on production VMs yet.

Set the `default-user` property for the qube manually as appropriate
(see QubesOS/qubes-issues#9020).

## Completed

### Core / Xen PV drivers

- Core drivers (xenbus/xeniface)
- Additional drivers (disk/network for performance)

### Integration

- Core services (qrexec agent, qubesdb)
- `qvm-run` with passthrough I/O
- AppIcon extraction
- Clipboard integration
- File receiving
- File sending
- Shell context menus for file sending and editing in other VMs
- Initializing the private disk volume
- Moving user profile to the private disk volume (QubesOS/qubes-issues#5916)

### GUI agent

- Secure attention sequence (CTRL-ALT-DEL) simulation
- Fullscreen mode
  - Basic functionality
  - Resolution change on resize (limited by the basic display driver's hardcoded list of supported resolutions)
- Seamless mode
  - Basic functionality
  - User account control (UAC) popups (desktop switch)
  - Capturing Start Menu and notifications

## Remaining

- A way to interact in seamless mode
- Seamless mode is not expected anytime soon due to the different graphics drivers framework in Windows 8+
- Non-seamless mode drivers for Windows 10 are almost complete

## References

- Development branch: https://github.com/omeg/qubes-installer-windows-tools/tree/omeg/win10
