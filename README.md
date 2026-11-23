# Toyota Venza XLE AWD — For Sale

A one-page listing site for a Toyota Venza XLE AWD sold by its owner in Houston, TX.

**Live page:** https://mrmontgomerymm-ai.github.io/car-for-sale/

## How it works

`index.html` holds the page, its styling, the listing details and the inquiry form. The photos are in the `photos/` folder, which keeps `index.html` small enough to edit safely in GitHub's browser editor (it only saves the first 1 MB of a file). There's nothing to build.

GitHub Pages serves `index.html` from the `main` branch. Every commit goes live on its own, usually within a minute.

## Setup (one time)

1. Upload `index.html` (and this README) to the repo.
2. Go to **Settings → Pages** and set **Source** to *Deploy from a branch*.
3. Set **Branch** to `main` and the folder to `/ (root)`, then save.

## Updating the listing

Open `index.html` on GitHub (in a browser or the mobile app) and click the pencil icon. Scroll to the `CONFIG` block near the bottom and edit:

| Setting | What it does |
|---|---|
| `year` | Model year shown in the title (leave `""` to hide it) |
| `price` / `priceNote` | Asking price, e.g. `"$11,900"` and `"OBO"`. Leave `price` blank to show "Contact for price" |
| `status` | `"Available"`, `"Pending"` or `"Sold"` |
| `phone` | Number used by the Call and Text buttons |
| `email` | Optional. On desktop, the form opens an email to this address |
| `formspreeId` | Optional. With a Formspree form ID, inquiries go straight to your email |
| `specs` / `features` / `notes` | The details, features list and seller notes |

Commit the change and the live page updates.

### Changing photos

- **Replace a photo:** in the `photos/` folder, upload a new image with the *same file name* as the one you're replacing.
- **Add or remove a photo:** upload the image to `photos/`, then add or remove its line in the `PHOTOS` list in `index.html`. Each line has the file path and the caption shown on the page.

## Admin panel (price & status from your phone)

Open the live page with `#admin` on the end:
`https://mrmontgomerymm-ai.github.io/car-for-sale/#admin`

From there you can change the **price**, the **OBO / Firm / None** note, and **Available / Pending / Sold**, then tap **Save & publish**. Each save is a commit to this repo, and the page updates for everyone in about a minute.

**One-time token setup:** the panel needs a GitHub fine-grained personal access token.
1. GitHub → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. **Repository access:** *Only select repositories* → `car-for-sale`.
3. **Permissions → Repository permissions → Contents:** *Read and write*.
4. Pick an expiration, generate, and paste the token into the admin panel the first time you save.

The token is stored only in that browser on that device, and is never added to the site. Use **Remove it** in the panel to clear it. If the token is lost or leaked, delete it on GitHub and make a new one.

## Inquiries

- **Default:** the form opens the buyer's texting app with their message filled in, addressed to the listing phone.
- **With Formspree:** create a free form at formspree.io and paste its ID into `formspreeId`. Inquiries then arrive by email and the buyer sees a confirmation on the page.

## Privacy

The photos have the license plates, registration stickers and house number blurred. This repo is public, so keep addresses and other personal details out of commits.

## When it sells

Set `status` to `"Sold"`. To take the page down, turn off Pages in **Settings → Pages**, or delete the repo.
