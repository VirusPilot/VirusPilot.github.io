# VirusPilot's Collision Avoidance Compilation of Information
# Basics
## HF Protocols
- 868MHz RX/TX (max. 25mW): OGN, FLARM, FANET, ADS-L, PilotAware
- 869MHz RX/TX (max. 500mW): OGN, ADS-L
- 869MHz RX/TX: PilotAware
- 978MHz UAT (Universal Access Transceiver):
  - TIS-B: Traffic Information Service–Broadcast by UAT ground stations
  - FIS-B: Flight Information Services-Broadcast by UAT ground station
- 1090MHz
  - ADS-B in
  - ADS-B out
## DATA Protocols
- OGN: http://wiki.glidernet.org/ogn-tracking-protocol
- FLARM-NMEA: https://www.flarm.com/wp-content/uploads/2025/05/FTD-012-Data-Port-Interface-Control-Document-ICD-7.21.pdf
- FANET
- ADS-L
- GDL90
# Alternative Means to transport Traffic Information
- APPs for mobile phones (1090 traffic e.g. from adsbhub.org, 868/1090 traffic from OGN)
  - https://www.safesky.app
  - https://ccas.aero
# Further Alternatives
- https://github.com/glidernet/ogn-aprs-protocol/blob/067bdeb956bf414db3674841512c8e8a6a4d6c82/aprsmsgs.txt#L55
# DIY Projects for General Aviation
- https://github.com/stratux/stratux
- https://github.com/VirusPilot/stratux-pi4 (with various build examples)
- https://github.com/lyusupov/SoftRF
- https://github.com/moshe-braner/SoftRF
- https://github.com/gereic/GXAirCom
## Recommended DIY Devices
- LilyGO T-Beam (SoftRF Prime Edition MkII)
- LilyGO T-Beam S3 Supreme (SoftRF Prime Edition MkIII)
- LilyGO T-Echo (SoftRF Badge Edition)
- Seeed SenseCAP T1000-E (SoftRF Card Edition)
- Elecrow ThinkNode M1 (SoftRF Handheld Edition)
# Commercial Avionics Equipment
- Air Avionics AT-1: https://www.air-avionics.com/?page_id=653&lang=de
- PowerFLARM Flex: https://www.flarm.com/de/allgemeine-luftfahrt/powerflarm-flex
- Avionix ADS-L Tracker: https://www.avionix-shop.eu/product/17946648/ads-l-tracker
- Avionix AERO Tracker: https://www.avionix-shop.eu/product/14989526/aero-tracker
- uAvionix SkyEcho II: https://uavionix.com/products/skyecho
- PilotAware FX
# OGN/ADSB Base Stations
## DIY Hardware
- SDRs: https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/
- SDRs: https://de.flightaware.com/adsb/prostick/
- SDRs: https://www.nooelec.com/store/sdr/sdr-receivers.html
- Antennas and Cables (SK): https://vinnant.sk
- Antennas and Cables (DE): https://www.wimo.com/de/antennen/empfangsantennen/ads-b-antennen
- Antennas, Cables, Accessories (DE): https://airbatt.de/Airfield-equipment_OGN
- Antennas, Cables, Accessories (DE): https://webshop.jetvision.de/
- Filtered Preamps (UK): https://store.uputronics.com
- Cavity Filter (DE): https://shop.sysmocom.de/RF/Filters/
## DIY Software
- Ready to use image for Raspberry Pi (Seb v0.3): http://download.glidernet.org/seb-ogn-rpi-image
- Manual Software setup: https://github.com/VirusPilot/ogn-pi34
## Commercial PnP Receiver Equipment
- Avionix openAir multitrack receiver: https://www.avionix-shop.eu/product/14982358/openair-multitrack-receiver
- Jetvision Air!Squitter: https://airsquitter.com
- PilotAware ATOM Station
## Traffic Webpage (based on local OGN and/or ADSB receivers and optional OGN APRS feed)
- https://github.com/b3nn0/ogn2dump1090
