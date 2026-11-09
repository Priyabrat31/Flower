# Flower Lab — Interactive Flower Dissection Model

A GitHub Pages-ready, two-screen classroom teaching website for a Class 9 flower dissection lesson.

## What's included

- **Smart Board display:** Interactive flower illustration. Select a part directly or receive selections from the phone remote.
- **Mobile remote:** Dedicated buttons for Stamen, Anther, Filament, Stigma, Style, Ovary, Petal, Sepal and Pollen grain.
- **Home / Whole Flower:** Returns the Smart Board to the complete flower and closes the information card.
- **Information cards:** Each selected part shows its name, a short description and a simple illustration.
- **Wireless control:** Uses PeerJS for browser-to-browser connection. No Firebase or database configuration is required.
- **Class 9 scope:** The labels and cards are restricted to the parts requested for this model.

## Publish on GitHub Pages

1. Create a new repository on GitHub (for example, `flower-dissection-model`).
2. Upload `index.html` and `README.md` to the **root** of the repository.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then select **Save**.
6. After GitHub Pages publishes the site, open the provided website address.

## How to use it in class

1. Open the website on the laptop connected to the Smart Board.
2. Select **Start main display**.
3. Select **Connect phone**. The display creates a six-character room code and QR code.
4. Scan the QR code with the phone, or open the remote link on the phone. The phone must have internet access.
5. Tap a flower-part button on the phone. Its information card appears on the Smart Board.
6. Tap **Home / Whole Flower** on the phone to return to the complete flower view.

You can also select the flower parts directly on the Smart Board as a backup.

## Connection notes

- Both devices need an internet connection and should keep the website open during the lesson.
- The remote connection uses the public PeerJS cloud signaling service and public JavaScript CDNs (PeerJS and QRCode.js). These are external services, not part of GitHub Pages. Their availability and usage limits are outside this project's control.
- The random room code helps keep nearby sessions separate, but it is not an account-based security system. Use it only for classroom control and do not share it publicly.
- If the remote does not connect, check that the display page is still open, confirm the room code, and use **Reconnect to display** on the phone.
- The Smart Board display remains usable without the remote; the flower parts can be selected directly on the display.

## Files

- `index.html` — complete application (HTML, CSS, SVG illustrations and JavaScript)
- `README.md` — this guide
