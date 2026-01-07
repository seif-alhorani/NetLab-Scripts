# NetWork

Small collection of networking practice scripts and examples.

## Contents
- `macChanger.py` - change a network interface MAC address (Linux, root required)
- `networkscanner.py` - ARP scan a local subnet using Scapy
- `portscanner.py` - simple TCP port scan (default: localhost 1-1023)

## Requirements
- Python 3
- Linux for `macChanger.py` (uses `ifconfig`)
- Python packages:
  - `pyfiglet`
  - `scapy`

Install Python deps:
```bash
pip install pyfiglet scapy
```

## Usage
### MAC changer
```bash
sudo python macChanger.py --interface eth0 --mac 00:11:22:33:44:55
```

### Network scanner
Edit the target subnet inside `networkscanner.py`:
```python
scan("192.168.1.0/24")
```
Then run:
```bash
sudo python networkscanner.py
```

### Port scanner
Scans localhost by default. Update the host in `portscanner.py` if needed.
```bash
python portscanner.py
```

## Notes
- Use these scripts only on networks and systems you own or have permission to test.
