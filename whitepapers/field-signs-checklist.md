# Field Signs of Machinery Drift

*A tour-a-plant checklist — extracted from Paper 02: The Drift Machine.*

None of these proves a plant has drifted on its own. Together they're a reliable read — no lab equipment needed.

- A Wi-Fi network name broadcasting from inside the plant that nobody in IT can account for — walk the floor with your phone's Wi-Fi list open
- A consumer Wi-Fi router zip-tied or taped inside a control panel, SSID handwritten on masking tape
- An unmanaged desktop switch (a consumer plastic box) inside an industrial enclosure, powered by a wall wart
- Ethernet cables that appear on no drawing, with hand-written or masking-tape labels — or no labels at all
- IP addresses written in marker on masking tape stuck directly to PLCs and drives
- A cellular antenna stub on a machine backplane or enclosure top that appears on no drawing — follow it to the IIoT gateway phoning home around the firewall
- A USB Wi-Fi dongle sticking out of an engineering workstation or HMI
- TeamViewer, AnyDesk, or a vendor remote-access client installed — and logged in — on the shared engineering workstation
- Firewall rules or NAT entries with "temp," "test," or a person's name in the description, dated more than a year ago
- A VPN tunnel on the perimeter firewall that's up through weekends and holidays — vendor access that was "just for commissioning"
- A PLC that answers on a public IP — check the plant's external footprint before the tour, then ask about each one on the floor
- Vendor support stickers with phone numbers and "call before changing anything" on cabinet doors — remote-access relationships nobody tracks
- Network diagrams the maintenance lead corrects from memory while you're looking at them
- "Spare" parts stashed inside dirty electrical boxes and cabinets — the physical version of undocumented infrastructure
- Staff who answer "oh, that box phones home" about equipment they've never opened a ticket on

---

*Part of the [Outlaw Engineer whitepaper series](https://github.com/TheOutlawEngineer/TheOutlawEngineer). Licensed under [CC BY-NC-SA 4.0](../LICENSE).*
