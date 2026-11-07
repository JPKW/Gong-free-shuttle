# Privacy Policy for Nearest Free Wollongong Bus

**Last Updated:** November 8, 2026  
**Effective Date:** November 8, 2026  

This Privacy Policy describes how the **Nearest Free Wollongong Bus** mobile application ("the App", "we", "us", or "our") handles your information. We are committed to protecting your privacy and ensuring you have a transparent, secure experience when using our app.

---

## 1. Summary — Privacy by Design

- **We do not collect, store, sell, or share your personal data.**
- **Your GPS location is processed strictly on your device** in real time to locate the closest bus stops and estimate walking distances. It is **never** sent to our servers or any third-party server.
- **No account or registration is required.**
- **No tracking or profiling analytics SDKs** (such as Firebase Analytics, Facebook SDK, or advertising trackers) are included in the app.

---

## 2. Location Information and Usage

### Permissions Requested
The App requests runtime access to:
- `android.permission.ACCESS_FINE_LOCATION` (Precise GPS Location)
- `android.permission.ACCESS_COARSE_LOCATION` (Approximate Network Location)

### Why We Need Your Location
The Wollongong Free Shuttle consists of two reciprocal loop routes:
- **Route 55C (Clockwise Loop)**
- **Route 55A (Anti-Clockwise Loop)**

Along roads like Crown Street, Burelli Street, and Northfields Avenue, 55A and 55C stops are frequently situated within 20 to 50 meters of one another on opposite sides of the street. **Precise location is necessary** to distinguish which side of the street you are on, select the closest stop for each direction, and calculate accurate walking times.

### How Location Is Processed
- **On-Device Only:** When you open the app or tap refresh, your device's operating system provides your current GPS coordinate to the app's local repository code. The app calculates the distance using the mathematical Haversine formula against a bundled catalog of Wollongong bus stop coordinates.
- **No Remote Transmission:** Your exact GPS coordinates are **never** transmitted over the network or saved to any external database.
- **No Background Tracking:** The App does **not** request `ACCESS_BACKGROUND_LOCATION`. It does not track your location when the app is closed or minimized.
- **Home Screen Widget:** When you place the home screen widget on your launcher, location is only queried when you explicitly tap the widget refresh button (`↻`) or when the widget updates while connected to a network.

You can revoke location permissions at any time via your device's **Settings > Apps > Nearest Free Wollongong Bus > Permissions > Location**. If revoked, the app will display official scheduled timetable estimates until location access is re-enabled.

---

## 3. Network Communication and Transit Data

To display real-time bus arrivals and service alerts:
1. The App queries a dedicated serverless proxy (`gong-shuttle-tfnsw-proxy.joerg-wood.workers.dev`) hosted on Cloudflare Workers, which communicates securely with the **Transport for NSW (TfNSW) Open Data Hub**.
2. **Data Sent:** Only public transit identifiers are queried (such as standard NSW transit Stop IDs like `250045` or general bounding coordinates for Wollongong stops).
3. **No PII:** Requests sent to the proxy contain **no personal identifiers**, no Advertising IDs (AAID), no IP address tracking, and no device hardware fingerprints.
4. **Encryption:** All network requests are encrypted using industry-standard HTTPS (TLS 1.2/1.3).

---

## 4. Third-Party Services and External Links

The App interacts with external services in the following limited ways:

- **Transport for NSW Open Data:** Source of real-time bus departure information. (Subject to TfNSW Open Data terms).
- **Google Maps Walking Directions:** When you tap the **"Directions"** button on a stop card, the App opens an Android system intent (`google.navigation:q=lat,lng&mode=w`) to launch the Google Maps app installed on your device for turn-by-turn walking directions. No data is shared with Google Maps other than the destination bus stop coordinates.
- **Cloudflare Workers:** Acts as a reverse proxy for transit API calls, caching public arrival timetables at the edge to protect rate limits.

---

## 5. Government Non-Affiliation Disclaimer

**Nearest Free Wollongong Bus is an independent community application developed for commuters, university students, and visitors to Wollongong.**

- The App is **not** an official government app and is **not** affiliated with, associated with, authorized by, endorsed by, or in any way officially connected with **Transport for NSW**, the **NSW Department of Transport**, or the **NSW Government**.
- Public transit arrival times, schedules, and route information are sourced from the **Transport for NSW Open Data Hub** under Creative Commons licensing.

---

## 6. Data Retention and Deletion

Because the App collects **zero personal data** and operates without user accounts:
- There is no personal data retained on any server.
- Local user preferences (such as your preferred route display order) are stored strictly on your device using Android Jetpack DataStore.
- You can erase all local app preferences at any time by clearing app data in **Settings > Apps > Nearest Free Wollongong Bus > Storage & Cache > Clear Storage**, or by uninstalling the application.

---

## 7. Children's Privacy

The App does not knowingly collect or solicit any personal information from children under the age of 13 (or under the applicable age of consent in your jurisdiction). The service provides general public transport scheduling and is compliant with the Children's Online Privacy Protection Act (COPPA) and Australian Privacy Principles.

---

## 8. Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect operational or regulatory updates. Any changes will be posted on this page with an updated "Last Updated" date. We encourage you to review this policy periodically.

---

## 9. Contact Us

If you have questions, feedback, or concerns regarding this Privacy Policy or the practices of the Nearest Free Wollongong Bus application, please contact:

- **Developer:** Joerg Wood
- **Email:** joerg.wood@gmail.com
- **Project Repository:** https://github.com/JPKW/Gong-free-shuttle
- **Location:** Wollongong, New South Wales, Australia
