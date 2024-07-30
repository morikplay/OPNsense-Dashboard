# What's Monitored
- Active Users
- Uptime
- CPU Load total
- Disk Utilization
- ZFS utilization
- Memory Utilization
- CPU Utilization per core (Single Graph)
- RAM Utilization time graph
- Load Average
- Load Average Graph
- CPU and ACPI Temperature Sensors
- Gateway Response time - dpinger
- List of interfaces with IPv4, IPv6, Subnet, MAC, Status and pfSense labels thanks to [/u/trumee](https://www.reddit.com/r/PFSENSE/comments/fsss8r/additional_grafana_dashboard/fmal0t6/)
- WAN Statistics - Traffic & Throughput (Identified by dashboard variable)
- LAN Statistics - Traffic & Throughput (Identified by dashboard variable)
- Firewall Statistics - Blocked Ports, Protocols, Events, Blocked IP Locations, and Top Blocked IP
# Changelog

[2024]
- Modified Graylog content pack with the following:
    - included configuration for ingesting `filterlog` input
    - included lookup table, cache and data adapters
    - due to a change in `filterlog` format, the csv-to-field regex didn't work. Changed the behavior to consuming grok extractors instead. Only `IPv4` is verified (as I do not have functional IPv6 network yet)
- Updated grafana dashboard + queries
    ![Firewall Dashboard](grafana/OPNsense-Grafana-Dashboard-1.png)
    ![ZFS Dashboard](grafana/OPNsense-Grafana-Dashboard-2.png)
    ![Hardware Dashboard](grafana/OPNsense-Grafana-Dashboard-3.png)
    ![Network Dashboard](grafana/OPNsense-Grafana-Dashboard-4.png)
    ![WAN Dashboard](grafana/OPNsense-Grafana-Dashboard-5.png)
    ![Sample LAN Dashboard](grafana/OPNsense-Grafana-Dashboard-6.png)
    ![Suricata Dashboard](grafana/Grafana-OPNsense-Suricata.png)
- Updated install / configuration instructions

[<2024]
- Converted InfluxQL queries to Flux.
- Converted pfSense functions to OPNsense.
- Added Firewall panels.
- Added subnet info to Interface Summary panels
- Added Suricata dashboard, see instructions [here](./configure.md#configuration-for-the-suricata-dashboard-optional)
- Added RFC5424 support thanks to [subract](https://github.com/IRQ10/Graylog-OPNsense_Extractors/pull/11)


# Running on

    Grafana >11.1.3
    InfluxDB >2.7.6
    Graylog >5.2.3


# Configuration
Configuration instructions can be found [here](./configure.md).
