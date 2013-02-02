# wireshark2latex

Generate TikZ graphics from tcpdump/Wireshark captures for usage in LaTeX documents.

# Instructions

1. Install tshark
2. Put your captured pcap file under ``script`` and name it ``capture.pcap``
3. Configure IP addresses in ``script/capture.cfg``
4. Run ``script/generate``
5. Look at ``example/example.tex`` how to include generated tex file

# Infos

Forked to fix some issues with the original script.

Original script by Vladimir V. Lavrov

From http://www.wireshark.org/lists/wireshark-users/201007/msg00258.html

# Example of generated TikZ graphic

![Screenshot](https://github.com/dschuermann/wireshark2latex/raw/master/screenshot.png "Screenshot")