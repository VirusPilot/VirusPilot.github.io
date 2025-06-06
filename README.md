# VirusPilot's Collision Avoidance Compilation of Information
# Basics
## Radio Protocols
- 868 MHz: **OGN**, **FLARM**, **FANET**, **ADS-L**, **PilotAware** (25 mW transmit power)
  - amongst others, the following essential data is transmitted (and encrypted in case of FLARM):
    - GNSS position and altitude
    - ground speed, sink/climb rate, track over ground
    - aircraft ID (or ICAO hex code) and type
    - predicted flight path (FLARM only)
- 869 MHz: **OGN**, **ADS-L**, **PilotAware** (500 mW transmit power)
- 1090 MHz: **Mode-S** (200 W transmit power)
  - the following data is transmitted when interrogated (selective) by ground radar (using 1030 MHz) or by other aircraft:
    - ICAO hex code and callsign
    - barometric altitude
- 1090 MHz: **Mode-S ES** (Extended Squitter, 200 W transmit power)
  - carries ADS-B (Automatic Dependent Surveillance - Broadcast): [The 1090 Megahertz Riddle](https://mode-s.org/1090mhz)
  - amongst others, the following essential data is transmitted (2 Hz update rate when airborne):
    - GNSS position, barometric and GNSS altitude
    - ground speed, sink/climb rate, track over ground
    - ICAO hex code, type and callsign
    - transponder code
  - many Mode-S Transponders can be upgraded to ADS-B out (up to SIL=3, depending on the certification)
- 978 MHz: **UAT** (Universal Access Transceiver, 10-20 W transmit power)
  - same functionality as 1090 MHz ES ADS-B
  - only approved/used in the US and only up to FL180
  - ADS-R, TIS-B and FIS-B from Ground Stations
- 978 MHz: **UAT Ground Stations** provide the following:
  - ADS-R: Rebroadcast of ADS-B information
  - TIS-B: Traffic Information Service–Broadcast
  - FIS-B: Flight Information Services-Broadcast
## Data Protocols used by Tracker Devices
- OGN: [OGN Tracking Protocol Specification](http://wiki.glidernet.org/ogn-tracking-protocol)
- FLARM-NMEA: [FLARM Data Port Interface Specification](https://www.flarm.com/wp-content/uploads/2025/05/FTD-012-Data-Port-Interface-Control-Document-ICD-7.21.pdf)
- FANET: [FANET Protocol Specification](https://github.com/3s1d/fanet-stm32/blob/master/Src/fanet/radio/protocol.txt)
- SRD 860 ADS-L: [ADS-L Specification](https://www.easa.europa.eu/en/downloads/137503/en&ved=2ahUKEwjZ7s-Dt8ONAxVGnf0HHe__GKwQFnoECBoQAQ&usg=AOvVaw2E8m3UcifYigBUuZ0SVv-x)
- GDL90: [GDL90 Specification](https://www.faa.gov/sites/faa.gov/files/air_traffic/technology/adsb/archival/GDL90_Public_ICD_RevA.PDF)
- OCAP: [Open Collision Avoidance Protocol](https://www.project-ocap.net)
## Datalink Protocols used in Ground Stations
- [AVR/RAW/BINARY](https://github.com/firestuff/adsb-tools/blob/master/protocols/raw.md)
- [BEAST](https://github.com/firestuff/adsb-tools/blob/master/protocols/beast.md)
- [JSON](https://github.com/firestuff/adsb-tools/blob/master/protocols/json.md)
- [SBS/Basestation](http://woodair.net/sbs/article/barebones42_socket_data.htm)
# Alternative Means to transport Traffic Information (using mobile phone network up to 5000 ft)
- APPs for mobile phones (1090 traffic e.g. from OpenSky or adsbhub.org, 868/1090 traffic from OGN)
  - https://www.safesky.app (provides GDL90 output to feed EFB Apps like SkyDemon or VFRnav)
  - https://ccas.aero (provides GDL90 output to feed EFB Apps like SkyDemon or VFRnav)
  - https://www.airmate.aero (displays traffic inline)
# Further Tracking Alternatives
- as definded in the [OGN APRS Specification](https://github.com/glidernet/ogn-aprs-protocol/blob/067bdeb956bf414db3674841512c8e8a6a4d6c82/aprsmsgs.txt#L55/)
# DIY Collision Avoidance Projects for General Aviation
- https://github.com/stratux/stratux
- https://github.com/VirusPilot/stratux-pi4 (with various build examples)
- https://github.com/lyusupov/SoftRF
- https://github.com/moshe-braner/SoftRF
- https://github.com/gereic/GXAirCom
## Recommended DIY Devices
- Raspberry Pi 3, 4 or 5 + SDRs + Antennas + GPS (Stratux)
- LilyGO T-Beam (SoftRF Prime Edition MkII)
- LilyGO T-Beam S3 Supreme (SoftRF Prime Edition MkIII)
- LilyGO T-Echo (SoftRF Badge Edition)
- Seeed SenseCAP T1000-E (SoftRF Card Edition)
- Elecrow ThinkNode M1 (SoftRF Handheld Edition)
## Commercial Avionics Equipment
- [Air Avionics AT-1](https://www.air-avionics.com/?page_id=653&lang=de/): ADS-B in, FLARM in/out
- [PowerFLARM Flex](https://www.flarm.com/de/allgemeine-luftfahrt/powerflarm-flex/): ADS-B in, FLARM in/out
- [Avionix ADS-L Tracker](https://www.avionix-shop.eu/product/17946648/ads-l-tracker/): ADS-B/UAT/OGN/FANET/ADS-L in, OGN/ADS-L out
- [Avionix AERO Tracker](https://www.avionix-shop.eu/product/14989526/aero-tracker/): ADS-B/OGN/FANET/ADS-L in, SafeSky over mobile network
- [uAvionix SkyEcho II](https://uavionix.com/products/skyecho/)
  - Primary receiver:  1090MHz ADS-B traffic receiver
  - Secondary receiver: selectable between 978 MHz UAT ADS-B or 868 MHz FLARM (FLARM License required)
  - 1090MHz ADS-B DO-260B Class A0 transmitter with SIL=1 (100 mW transmit power, only allowed in certain countries e.g. UK: CAP 1391)
- PilotAware FX
## Chipsets
- [ADSBee 1090](https://pantsforbirds.com/adsbee-1090/)
- [Pong](https://pongradio.com/)
- [GNS5892](https://www.gns-electronics.de/product/gns-5892r-low-power-low-cost-ads-b-modul/)
- [Aerobits TT-SC1](https://www.aerobits.pl/product/tt-sc1/)
- [FLARM](https://www.flarm.com/de/integration/)
# OGN/ADS-B Base Stations
## DIY Hardware
- SDRs:
  - https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/
  - https://www.nooelec.com/store/sdr/sdr-receivers.html
- Antennas and Cables (SK): https://vinnant.sk
- Antennas and Cables (DE): https://www.wimo.com/de/antennen/empfangsantennen/ads-b-antennen
- Antennas, Cables, Accessories (DE): https://airbatt.de/Airfield-equipment_OGN
- Antennas, Cables, Accessories (DE): https://webshop.jetvision.de/
- Filtered Preamps (UK): https://store.uputronics.com
- Cavity Filters (DE): https://shop.sysmocom.de/RF/Filters/
## DIY Software
- Ready to use Image for Raspberry Pi (Seb v0.3): http://download.glidernet.org/seb-ogn-rpi-image
- Manual Software setup (https://github.com/VirusPilot/ogn-pi34):
  - only OGN: https://github.com/VirusPilot/ogn-pi34/blob/master/install-pi34.sh
  - ADS-B/OGN: https://github.com/VirusPilot/ogn-pi34/blob/master/install-pi34-adsb.sh
  - ADS-B/OGN (in combination with ogn2dump1090): https://github.com/VirusPilot/ogn-pi34/blob/dev/install-pi34-ogn2dump1090.sh
- [Filip Chochol's nice explanation](https://chochol.io/en/hardware/ogn-receiver-installation-and-configuration-on-raspberry-pi/)
## Commercial PnP Equipment
- [Avionix openAir multitrack receiver](https://www.avionix-shop.eu/product/14982358/openair-multitrack-receiver)
- [Jetvision Air!Squitter](https://airsquitter.com)
- PilotAware ATOM Station
## Traffic Webpage (based on local OGN and/or ADSB receivers and optional OGN APRS feed)
- https://github.com/b3nn0/ogn2dump1090
