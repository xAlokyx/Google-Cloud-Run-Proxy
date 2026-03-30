# Google Cloud Run Proxy

[![Go](https://img.shields.io/badge/Go-1.21+-00ADD8?style=flat&logo=go)](https://golang.org/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?style=flat&logo=docker)](https://www.docker.com/)
[![License: GPL-3.0](https://img.shields.io/badge/License-GPLv3-yellow.svg?style=for-the-badge&logo=gplv3&logoColor=white)](https://opensource.org/license/gpl-3-0)

A lightweight, high-performance TCP proxy server written in Go. Designed for seamless deployment on Google Cloud Run, this proxy efficiently forwards traffic to a specified target server (e.g., a V2Ray server), making it an ideal solution for bypassing network restrictions or masking backend services.

## 🚀 Features

- **Lightweight & Fast**: Built with Go for minimal resource footprint and high concurrency.
- **Cloud Run Ready**: Optimized for stateless, containerized environments like Google Cloud Run.
- **Docker Support**: Includes a multi-stage Dockerfile for easy building and deployment.
- **Simple Configuration**: Configurable via environment variables.

## 📋 Prerequisites

- **Go**: Version 1.21 or higher (for local development).
- **Docker**: For containerized deployment.
- **Google Cloud SDK**: If deploying to Google Cloud Run.

## ⚙️ Configuration

The application is configured using environment variables:

| Variable | Description | Default |
| :--- | :--- | :--- |
| `PORT` | The port the server listens on. | `8080` (or provided by Cloud Run) |
| `V2RAY_SERVER_IP` | The IP address or hostname of the target server. | **Required** |

> [!NOTE]
> The target port is currently hardcoded to `:80` in the code. Ensure your target server is listening on port 80 or modify `main.go` if needed.

## 🛠️ Installation & Usage

### Local Development

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/praveenkarunarathne/Google-Cloud-Run-Proxy.git
    cd Google-Cloud-Run-Proxy
    ```

2.  **Set environment variables:**
    ```bash
    export PORT=8080
    export V2RAY_SERVER_IP=1.2.3.4  # Replace with your target IP
    ```

3.  **Run the application:**
    ```bash
    go run main.go
    ```

### 🐳 Running with Docker

You can use the pre-built public image:

```bash
docker run -p 8080:8080 \
  -e PORT=8080 \
  -e V2RAY_SERVER_IP=1.2.3.4 \
  docker.io/praveenkarunarathne/google-cloud-run-proxy
```

Alternatively, to build from source:

1.  **Build the Docker image:**
    ```bash
    docker build -t cloud-run-proxy .
    ```

2.  **Run the container:**
    ```bash
    docker run -p 8080:8080 -e PORT=8080 -e V2RAY_SERVER_IP=1.2.3.4 cloud-run-proxy
    ```

## ☁️ Deploy to Google Cloud Run

Deploy directly using the public image:

```bash
gcloud run deploy cloud-run-proxy \
  --image docker.io/praveenkarunarathne/google-cloud-run-proxy \
  --platform managed \
  --region us-central1 \
  --allow-unauthenticated \
  --set-env-vars V2RAY_SERVER_IP=1.2.3.4
```

*Replace `1.2.3.4` with your target IP.*

## 📄 License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.    </a>
    <a href="mailto:praveen.karunarathne01@gmail.com">
      <img src="https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
    </a>
    <img src="https://komarev.com/ghpvc/?username=praveenkarunarathne&label=Profile+Views&color=blue&style=for-the-badge" alt="Profile Views" />
  </div>
</div>

<br />

## ⚡ Technical Profile

I am a **Systems-focused Engineer** specializing in the intersection of **Cloud Infrastructure**, **Network Programming**, and **Automation**. My passion lies in dissecting complex workflows and scripting efficient, scalable solutions. Whether it's managing **Oracle Cloud** infrastructure with self-healing scripts, building low-level **Network Proxies** in Go, or developing sophisticated **Telegram Bots** in Python, I build tools that work harder so you don't have to.

---

## 📊 GitHub Analytics

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=praveenkarunarathne&show_icons=true&theme=gotham&hide_border=true&count_private=true&include_all_commits=true" alt="Praveen's GitHub Stats" height="180"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=praveenkarunarathne&layout=compact&theme=gotham&hide_border=true&langs_count=8" alt="Top Languages" height="180"/>
</div>

---

## 🛠️ Technology Stack

<div align="center">

| Core & Systems | Cloud & DevOps | Web & Mobile |
|:---:|:---:|:---:|
| ![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white) <br> ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) <br> ![Shell](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white) | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) <br> ![Oracle](https://img.shields.io/badge/Oracle_Cloud-F80000?style=for-the-badge&logo=oracle&logoColor=white) <br> ![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white) | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white) <br> ![JS](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) <br> ![Apps Script](https://img.shields.io/badge/Google_Apps_Script-4285F4?style=for-the-badge&logo=googleappsscript&logoColor=white) |

</div>

---

## 🏆 Flagship Projects

Additional details on my most complex and robust engineering work.

| Project | Key Features & Tech |
| :--- | :--- |
| **[Google Cloud Run Proxy](https://github.com/praveenkarunarathne/Google-Cloud-Run-Proxy)**<br>_High-Performance Cloud Run TCP Proxy_ | • **High Concurrency**: Lightweight TCP proxy built in Go for minimal resource footprint.<br>• **Stateless Deployment**: Fully optimized for containerized execution on Google Cloud Run.<br>• **Traffic Forwarding**: Seamlessly routes traffic to target servers (like V2Ray) to bypass network restrictions.<br>![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GCP](https://img.shields.io/badge/-Google_Cloud-4285F4?style=flat-square&logo=google-cloud&logoColor=white) |
| **[Marzban Subscription Dashboard](https://github.com/praveenkarunarathne/Marzban-User-Subscription-Link-Management-Dashboard)**<br>_Serverless User Management System_ | • **Serverless Backend**: Built entirely on Google Apps Script & Drive.<br>• **Seamless Sync**: Real-time Webhook integration with Marzban Server.<br>• **Security**: Password-protected UI with automated file management.<br>![GAS](https://img.shields.io/badge/-Google_Apps_Script-4285F4?style=flat-square&logo=googleappsscript&logoColor=white) ![Bash](https://img.shields.io/badge/-Bash-121011?style=flat-square&logo=gnu-bash&logoColor=white) |
| **[Oracle Cloud Auto-Provisioner](https://github.com/praveenkarunarathne/Oracle_Cloud_Out_Of_Capacity_Script)**<br>_High-Availability Infrastructure Tool_ | • **Smart Automation**: Continuously monitors and snipes "Always Free" instances.<br>• **Multi-Arch**: Supports both AMD (Micro) and Ampere (A1 Flex) shapes.<br>• **Notification System**: Instant Telegram alerts upon successful provisioning.<br>![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white) |
| **[Wi-Fi Direct Hotspot](https://github.com/praveenkarunarathne/WIFI-Direct-Hotspot-Android-App)**<br>_P2P Mesh Networking App_ | • **Offline Connectivity**: Full device-to-device communication without Internet.<br>• **Socket Layer**: Custom TCP implementation for reliable data transfer.<br>• **Modern Android**: Built for Android 13+ with strict permission handling.<br>![Kotlin](https://img.shields.io/badge/-Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white) ![Android](https://img.shields.io/badge/-Android_SDK-3DDC84?style=flat-square&logo=android&logoColor=white) |

<br/>

## 🛠️ Utilities & Tools

 Specialized scripts and proxies designed for specific engineering challenges.

| Project | Description | Stack |
| :--- | :--- | :--- |
| **[HTTP-to-TFTP Bridge](https://github.com/praveenkarunarathne/HTTP-to-TFTP-Bridge)** | UDP server bridging HTTP downloads to legacy TFTP clients. Essential for PXE boot. | ![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white) `net/packet` |
| **[Marzban TCP Proxy](https://github.com/praveenkarunarathne/Marzban-Proxy)** | Lightweight, stateless TCP tunnel optimized for Cloud Run containers. | ![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white) `Docker` |
| **[My Assistant Bot](https://github.com/praveen28624/MyAssistant)** | Multi-purpose Pyrogram bot for AI Chat (Kuki) and Music APIs. | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) `Pyrogram` |
| **[Apps Script Proxy](https://github.com/praveenkarunarathne/Google-Apps-Script-Simple-HTTP-Proxy)** | Secure HTTP proxy running on Google to bypass CORS restrictions for frontend apps. | ![GAS](https://img.shields.io/badge/-Apps_Script-4285F4?style=flat-square&logo=googleappsscript&logoColor=white) |
| **[Oracle IP Viewer](https://github.com/praveenkarunarathne/Oracle-Public-IP-Ranges-Viewer)** | Reactive web dashboard to filter and visualize Oracle Cloud public IP ranges. | ![JS](https://img.shields.io/badge/-Vanilla_JS-F7DF1E?style=flat-square&logo=javascript&logoColor=black) |

---

<div align="center">
  <p><b>Always building. Always automating.</b></p>
  <a href="https://github.com/praveenkarunarathne?tab=followers">
    <img src="https://img.shields.io/github/followers/praveenkarunarathne?label=Follow&style=social" alt="Follow" />
  </a>
</div>
