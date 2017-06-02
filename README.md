#wifite

An automated wireless attack tool.

What's New?

The biggest change from version 1 is support for "reaver", a Wifi-Protected Setup (WPS) attack tool. Reaver can compromise the PIN and PSK for many routers that have WPS enabled, usually within hours.

Other changes include a complete code re-write with bug fixes and added stability. Due to problems with the Python Tkinter suite, the GUI has been left out of this latest version.

About

Wifite is for Linux only.

Wifite was designed for use with pentesting distributions of Linux, such as Kali Linux, Pentoo, BackBox; any Linux distributions with wireless drivers patched for injection. The script appears to also operate with Ubuntu 11/10, Debian 6, and Fedora 16.

Wifite must be run as root. This is required by the suite of programs it uses. Running downloaded scripts as root is a bad idea. I recommend using the Kali Linux bootable Live CD, a bootable USB stick (for persistent), or a virtual machine. Note that Virtual Machines cannot directly access hardware so a wireless USB dongle would be required.

Wifite assumes that you have a wireless card and the appropriate drivers that are patched for injection and promiscuous/monitor mode.

Execution

To download and execute wifite, run the commands below:

wget https://raw.github.com/derv82/wifite/master/wifite.py
chmod +x wifite.py
./wifite.py

Required Programs

Please see the installation guide on the wiki for help installing any of the tools below.

Python 2.7.x. Wifite is a Python script and requires Python to run.

aircrack-ng suite. This is absolutely required. The specific programs used in the suite are:

airmon-ng,
airodump-ng,
aireplay-ng,
packetforge-ng, and
aircrack-ng.
Standard linux programs.

iwconfig, ifconfig, which, iw
Suggested Programs

* indicates program is not included in Backtrack 5 R1

*reaver, a Wifi-Protected Setup (WPS) attack tool. Reaver includes a scanner "walsh" (or "wash") for detecting WPS-enabled access points. Wifite uses Reaver to scan for and attack WPS-enabled routers.

*pyrit, a GPU cracker for WPA PSK keys. Wifite uses pyrit (if found) to detect handshakes. In the future, Wifite may include an option to crack WPA handshakes via pyrit.

tshark. Comes bundled with Wireshark, packet sniffing software.

cowpatty, a WPA PSK key cracker. Wifite uses cowpatty (if found) to detect handshakes.

Licensing

Wifite is licensed under the GNU General Public License version 2 (GNU GPL v2).

(C) 2010-2012 Derv Merkler
