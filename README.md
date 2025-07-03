# Minimalist Network & Security Test

A single-file, zero-dependency tool for analyzing your internet connection's performance, reachability, and security posture.


## 🚀 Features

*   ✅ **Single File:** The entire application (HTML, CSS, and JavaScript) is contained in a single `.html` file.
*   💨 **Zero Dependencies:** No external libraries, frameworks, or setup required. It runs directly in the browser.
*   🎨 **Modern UI:** A clean, responsive, and dark-themed interface that is easy to read and use.
*   🌐 **Comprehensive Tests:** Includes performance metrics, international connectivity checks, and critical security/privacy validations.
*   🔒 **Privacy-Focused:** The tool is entirely client-side. No data is ever stored or sent to a server owned by the developer.

---

## 🛠️ How to Use

1.  **Download:** Save the code as an HTML file (e.g., `net-test.html`).
2.  **Open:** Open the file in a modern web browser like Chrome, Firefox, or Edge.
3.  **Test:** Click the buttons for the tests you wish to perform. Results appear instantly.

---

## 📊 Understanding the Tests

The tests are grouped into three main categories: Performance, Service Connectivity, and Security.

### 1. Performance & Geolocation

These tests measure the core characteristics of your connection.

#### Check My IP
*   **What it does:** Fetches your public IP address and its associated country using reliable public APIs. It includes a fallback mechanism for better reliability.
*   **Public IP / Country:** Your public-facing address and the country where the IP is registered.

#### Test Ping
*   **What it does:** Measures network latency—the time it takes for a small packet of data to travel to a server and back.
*   **Result (ms):** Measured in milliseconds (ms). **Lower is better.** Crucial for gaming and video calls.

#### Test Download / Test Upload
*   **What it does:** Measures your connection's bandwidth by downloading or uploading a temporary file.
*   **Result (Mbps):** Measured in Megabits per second (Mbps). **Higher is better.** Determines how quickly you can stream, download, or upload content.

### 2. Service Connectivity

These tests verify whether your connection can reach specific popular international services.

#### Test Services
*   **What it does:** Attempts a quick connection to Google, YouTube, Gemini, and ChatGPT to check for regional or firewall blocks.
*   **Results:**
    *   `✓ Reachable`: Your connection successfully reached the service.
    *   `✗ Blocked`: Your connection was blocked, likely by a firewall or network restriction.

### 3. Security Checks

These tests validate important privacy and security aspects of your connection.

#### Run Security Checks
*   **WebRTC Leak:**
    *   **What it does:** Checks if your browser's WebRTC functionality is revealing your *real* IP address, which can happen even when using a VPN.
    *   **Note:** This test requires running "Check My IP" first for an accurate baseline comparison.
    *   **Results:**
        *   `✓ No Leak Detected`: Your WebRTC IP matches your public IP. This is secure.
        *   `✗ Leak Detected`: A different IP was found, potentially exposing your real location.

*   **Detected DNS Servers:**
    *   **What it does:** Identifies the DNS (Domain Name System) resolvers your system is using. Exposing this can reveal your browsing habits to your ISP.
    *   **"No DNS servers detected":** This is **not an error**. It is often a **positive sign** that your browser's Secure DNS (DoH) or a strong VPN is working correctly, effectively hiding your DNS activity from external probes.

*   **Encrypted DNS:**
    *   **What it does:** Analyzes the list of detected DNS servers to see if they belong to a known provider of encrypted DNS (like DNS-over-HTTPS).
    *   **Results:**
        *   `✓ Likely Enabled`: Your DNS is handled by a known secure provider (e.g., Cloudflare, Google, Quad9). This is excellent for privacy.
        *   `○ Uncertain`: Your DNS servers are not from a known secure provider, or no servers were detected.

---

## 💻 Technology Stack

*   **HTML**
*   **CSS** 
*   **Vanilla JavaScript**

---

## ⚠️ Disclaimer

This tool is provided for informational purposes only. Network test results can vary based on many factors, including browser extensions, network congestion, server load of the test APIs, and your physical location.
