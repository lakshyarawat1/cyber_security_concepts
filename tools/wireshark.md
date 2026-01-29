# Wireshark

- Wireshark is an open-source cross-platform network packet analyser tool capable of sniffing and investigating network traffic.

## Use cases

- Detecting and troubleshooting network problems, such as network load failure points and congestion.
- Detecting security anomalies, such as rogue hosts, abnormal port usage, and suspicious traffic.
- Investigating and learning protocol details, such as response codes and payload data.

## GUI

Wireshark GUI has five sections with a single all-in-one page.

- Toolbar : Contains multiple menus and shortcuts for packet sniffing and processing, including filterning, sorting, summarizing, exporting and merging.
- Display filter bar : Main query and filtering section.
- Recent Files : List of recently investigated files. Recall with a double-click.
- Capture filter and interfaces : Capture filters and available sniffing points (network interfaces).
- Status bar : Tool status, and numeric packet information.

### Loading PCAP Files

- Go to File menu, drag and drop the file to be loaded.

### Coloring packets

- Coloring packets can help better categorize large amount of packets visible in the screen.
- You can create custom coloring rules to spot events of interest by using display filters.
- There can be temporary rules, available for only one session or permanent rules.
- Coloring rules are inside the view menu.

## Packet Dissection

- Packet dissection also known as protocol dissection, investigates packet details by decoding available protocols and fields.
- There are seven different layers to the packet as per OSI model.