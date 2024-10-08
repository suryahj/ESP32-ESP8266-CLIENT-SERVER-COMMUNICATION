<!DOCTYPE html>
<html lang="en">
    
<h1>🌐 ESP32 Server & ESP8266 Client Network Communication 🔌</h1>

<p>This project sets up communication between an ESP32 acting as a server and multiple ESP8266 devices as clients. They communicate using the TCP/IP protocol over a local network. This is a great project for IoT, smart home automation, and wireless sensor networks.</p>

<h2 class="emoji">✨ Features</h2>
<ul>
    <li>📡 ESP32 as the server, handling multiple client connections.</li>
    <li>🔄 ESP8266 clients connect via TCP/IP and exchange data with the server.</li>
    <li>🌐 All devices operate over a local Wi-Fi network, ensuring fast, reliable communication.</li>
</ul>

<h2 class="emoji">🛠️ Technologies Used</h2>
<ul>
    <li><strong>ESP32</strong> as the server</li>
    <li><strong>ESP8266</strong> as the clients</li>
    <li><strong>TCP/IP Protocol</strong> for communication</li>
    <li><strong>Wi-Fi</strong> for network connectivity</li>
</ul>

<h2 class="emoji">📋 Circuit Setup</h2>
<ol>
    <li>⚙️ <strong>ESP32 Setup:</strong> Configure the ESP32 as a server that listens for incoming client connections.</li>
    <li>⚙️ <strong>ESP8266 Setup:</strong> Each ESP8266 connects to the same local Wi-Fi network and communicates with the ESP32 server via TCP/IP.</li>
</ol>

<h2 class="emoji">🚀 Installation</h2>
<ol>
    <li>📥 <strong>Clone the repository:</strong>
        <pre><code>git clone https://github.com/suryahj/ESP32-ESP8266-CLIENT-SERVER-COMMUNICATION.git</code></pre>
    </li>
    <li>📦 <strong>Install dependencies:</strong> Ensure you have the Arduino IDE set up with the necessary cores for ESP32 and ESP8266.</li>
    <li>💻 <strong>Upload the code:</strong> Flash the appropriate code to the ESP32 (server) and ESP8266 (clients).</li>
</ol>

<h2 class="emoji">💻 Usage</h2>
<ol>
    <li>🔌 Power on the ESP32 and ESP8266 devices.</li>
    <li>📶 Ensure all devices are connected to the same Wi-Fi network.</li>
    <li>🔄 The ESP32 will act as a server, and the ESP8266 clients will begin communicating with it.</li>
</ol>

<h2 class="emoji">📄 Example Code</h2>
<pre><code>// Example server code (ESP32)
#include <WiFi.h>
WiFiServer server(80);

void setup() {
  WiFi.begin("SSID", "PASSWORD");
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
  }
  server.begin();
}

void loop() {
  WiFiClient client = server.available();
  if (client) {
    while (client.connected()) {
      // Handle communication
    }
    client.stop();
  }
}
</code></pre>

<h2 class="emoji">📋 Serial Monitor of Server</h2>
![image](https://github.com/user-attachments/assets/8fd0ae3d-f78f-4ba1-9ad4-2031d3d5b913)



<h2 class="emoji">🙌 Contributions</h2>
<p>This project was created by <strong>Suryanath Tripathy</strong>. Contributions are welcome! Feel free to fork the repository and submit pull requests with improvements or new features.</p>

<h2 class="emoji">📜 License</h2>
<p>This project is licensed under the MIT License. See the LICENSE file for more information.</p>

<footer>
    <p>🚀 Happy Coding! 🌟</p>
</footer>

</body>
</html>
