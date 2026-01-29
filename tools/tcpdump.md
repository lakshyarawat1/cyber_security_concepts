# TCPDump

Tcpdump uses `libpcap` library which is written in C/C++

- They were released for Unix-like systems in 1990s.
- `libpcap` was ported to `winpcap` for windows.
- All networking tools use these libraries.

## Usage

- `-i` flag specifies the interface on which packets will be captured, use value `any` to listen to all available interfaces.