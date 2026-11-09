# Flower Lab — Realistic Interactive Flower Dissection Model

A GitHub Pages-ready, two-screen classroom teaching website for a Class 9 flower dissection lesson.

## Features

- A realistic botanical flower diagram on the Smart Board display.
- Clickable label areas for Stamen, Anther, Filament, Stigma, Style, Ovary, Petal and Sepal.
- A mobile remote with picture buttons for all nine requested items, including a separate magnified Pollen grain view.
- Each selection displays the part name, a short description and a matching close-up picture.
- **Home / Whole Flower** returns the display to the complete flower.
- No PeerJS, QRCode.js, jQuery or other JavaScript library is required. The connection uses the browser's built-in WebSocket support and a small MQTT 3.1.1 implementation in the page.
- The room code is eight characters. A copyable mobile URL is created for the phone.

## Project structure

- `index.html` — complete web app (HTML, CSS and JavaScript)
- `assets/main-flower.jpg` — realistic labelled flower diagram
- `assets/stamen.jpg`, `assets/anther.jpg`, `assets/filament.jpg`, `assets/stigma.jpg`, `assets/style.jpg`, `assets/ovary.jpg`, `assets/petal.jpg`, `assets/sepal.jpg`, `assets/pollen.jpg` — detail images used in cards and mobile controls
- `README.md` — this guide

Keep the `assets` folder beside `index.html`. Do not rename the image files.

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `flower-dissection-model`.
2. Upload `index.html`, `README.md`, and the complete `assets` folder into the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. Open the published URL shown in the Pages section.

You can upload the extracted folder using GitHub Desktop, the GitHub website, or Git. Make sure the `assets` folder is uploaded with all ten JPG files.

## Use it in the classroom

1. Open the published website on the laptop connected to the Smart Board.
2. Click **Start main display**. The app creates an eight-character room code.
3. Click **Connect phone** and copy the mobile remote link. Send that link to the phone (for example, using your own messaging app), or open the same website on the phone and enter the room code.
4. On the phone, select Stamen, Anther, Filament, Stigma, Style, Ovary, Petal, Sepal or Pollen grain. The matching card appears on the Smart Board.
5. Tap **Home / Whole Flower** on the phone to return to the complete flower.

The flower labels on the Smart Board are also clickable, so the lesson can continue even when the mobile connection is unavailable.

## Wireless connection and privacy note

The mobile remote uses the public EMQX MQTT test broker at `wss://broker.emqx.io:8084/mqtt`. It is a public test service, not a private production server. The room code is random and eight characters long, but this is not account-based authentication. Only simple flower-part commands are sent; do not send names, personal information, passwords or other sensitive data through this service. The public broker can experience downtime or be blocked by a school network. If that happens, use the clickable labels on the Smart Board or retry when internet access is available.

The website does not need to load a separate PeerJS or QR-code library, so the earlier **“Remote library could not load”** error path has been removed.
