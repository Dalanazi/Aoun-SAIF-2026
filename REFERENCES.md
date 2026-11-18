# Aoun (عون): References & Evidence

Every numbered claim on the SAIF 2026 poster ([1]–[18]) is backed by one of the sources below.

## External sources

| # | Claim on the poster | Source |
|---|---|---|
| 1 | Personal locator beacons (PLBs) send the alert through satellites to a ground station, then to a Rescue Coordination Centre, not to the nearby team. | AMSA, *How distress beacons work*. https://beacons.amsa.gov.au/about/how-they-work.asp |
| 2 | Only beacons with the Galileo Return Link Service receive an automatic acknowledgement that the alert was received. | European GNSS Service Centre, *SAR/Galileo Return Link Service*. https://www.gsc-europa.eu/node/5876 |
| 3 | Lost people who keep moving enlarge the search area; search and rescue teams advise them to stay put. | KSL, *Hiking safety: what to do if you get lost* (interview with a search and rescue coordinator). https://www.ksl.com/article/36147671/hiking-safety-what-to-do-if-you-get-lost · Trail Hiking Australia, *What to do if you get lost hiking*. https://www.trailhiking.com.au/hike-safety/getting-lost/ |
| 4 | Satellite messengers need an active paid subscription; plans start at US$11.95 per month. | Garmin, *inReach satellite communication: subscription plans*. https://www.garmin.com.my/minisite/inreach/personal/ |
| 5 | Satellite SOS on phones works only in selected countries. | MacRumors, *Apple's free satellite features on iPhone: available countries* (Oct 2025). https://www.macrumors.com/2025/10/10/apple-satellite-features-which-countries/ |
| 6 | Civil GPS is free of direct user fees, and receivers only listen (receive-only). | GPS.gov, *Free access for civilian use*. https://www.gps.gov/node/34 |
| 7 | LoRa supports long-range links (Semtech cites up to 15 km in rural line of sight). Aoun's own long-range performance is **not yet field-tested**. | Semtech LoRa overview (via Richardson RFPD). https://www.richardsonrfpd.com/?p=13261 |
| 8 | In Saudi Arabia, short-range devices may use 863–870 MHz at ≤ 25 mW e.r.p. | Communications, Space & Technology Commission (CST), *RI054 Specification for Short Range Devices*. https://www.cst.gov.sa/ar/RulesandSystems/RegulatoryDocuments/EquipmentApproval/Documents/TA%20959%20E%20RI054.pdf |
| 9 | SX1262 LoRa radio: up to +22 dBm, −148 dBm sensitivity, 4.6 mA receive current. | Semtech, *SX1262 product page*. https://www.semtech.com/products/wireless-rf/lora-transceivers/sx1262 |
| 10 | NEO-6M GPS receiver specifications. | u-blox, *NEO-6 GPS Modules Data Sheet* (GPS.G6-HW-09005). https://www.u-blox.com/sites/default/files/products/documents/NEO-6_DataSheet_%28GPS.G6-HW-09005%29.pdf |
| 11 | AES-GCM authenticated encryption. | NIST SP 800-38D, *Galois/Counter Mode (GCM) and GMAC*. https://csrc.nist.gov/pubs/sp/800/38/d/final |
| 12 | The T-Beam V1.2 board (ESP32 + LoRa + GPS) costs about US$41. | LILYGO, *T-Beam* product page (US$40.98). https://lilygo.cc/products/t-beam-softrf |
| 13 | A PLB with return-link confirmation costs about US$430. | ACR ResQLink 410 RLS listing (US$429.95). https://freeportmarine.com/products/acr-resqlink-410-rls |
| 14 | 131 people went missing in Saudi deserts in 1441 AH; 20 died of hunger and thirst (Enjad Search and Rescue Association statistic). | Al-Watan, *131 مفقودا في الصحارى* (7 Apr 2021). https://www.alwatan.com.sa/article/1073200 |
| 15 | Enjad volunteers handled 902 reports in one week (≈ 128 a day), including missing persons. | Al-Watan, *128 بلاغا يوميا لمركبات عالقة* (7 Apr 2025). https://www.alwatan.com.sa/ampArticle/1163298 |
| 18 | GPS is a constellation of 31+ operational satellites in medium Earth orbit (≈ 20,200 km); a receiver needs signals from at least 4 satellites to fix a 3D position. | GPS.gov, *Space Segment*. https://www.gps.gov/systems/gps/space · GPS.gov, *Constellation arrangement*. https://www.gps.gov/node/198 |

## Our own evidence

| # | Evidence | Where |
|---|---|---|
| 16 | Security test suite: 10 test cases, run on a PC host with the same code as the firmware, compiled against Mbed TLS 2.28. | [Aoun_Security_Verification_Report.pdf](Aoun_Security_Verification_Report.pdf) |
| 17 | On-device lab tests on 2 × LILYGO T-Beam V1.2 (Oct 2026): encrypted SOS and confirmation, automatic retry, wrong-key SOS (5 attempts, 5 rejected), unregistered unit (3 attempts, 3 rejected), GPS first fix, and indoor link incl. through a concrete floor. | [README.md, "On the real boards"](README.md#on-the-real-boards-2--lilygo-t-beam-v12-7-oct-2026) |

## Scope and limits of our results

- The tests were run in the lab with 2 prototypes, indoors.
- GPS takes about 4 minutes on a cold start and about 1 minute on a warm start.
- Long-range open-field trials have not been run yet. They are the first item in our future work.

---

**Team:** Dana Mohammad Alanazi (Team Leader) · Renad Metab Aldosari · Jawaher Faisal Alsharif · Hailah Abdulrahman Alhejjei · Abrar Hassan Alqarni
**Digital Technical College for Girls, Riyadh** · SAIF 2026 · Team No. SAIF130055
