# 🎂 Birthday Dashboard

A beautiful, zero-dependency birthday dashboard you can host for free on **GitHub Pages**.

![Dashboard preview](https://img.shields.io/badge/hosted-GitHub%20Pages-brightgreen)

---

## 🚀 How to deploy

### 1. Fork or create a new repo
Upload these files to a GitHub repo:
```
birthday-dashboard/
├── index.html       ← the dashboard
├── people.csv       ← your birthday data
├── photos/          ← optional: add photos here
│   ├── alice.jpg
│   └── ...
└── README.md
```

### 2. Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under *Source*, select **Deploy from a branch**
3. Choose `main` branch, `/ (root)` folder → **Save**
4. Your dashboard will be live at:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```

---

## 📋 Editing `people.csv`

Open `people.csv` in any text editor or directly on GitHub:

```csv
Name,Birthday,Photo
Alice Smith,1990-06-15,photos/alice.jpg
Bob Jones,1985-03-22,
Carol White,1992-06-03,photos/carol.jpg
```

| Column     | Required | Notes |
|------------|----------|-------|
| `Name`     | ✅ Yes   | Full name displayed on the card |
| `Birthday` | ✅ Yes   | Formats supported: `YYYY-MM-DD`, `MM/DD/YYYY`, `DD/MM/YYYY` |
| `Photo`    | ❌ No    | Relative path to an image in your repo. Leave blank for initials avatar. |

**Adding someone:** Add a new row. Push to GitHub. Done — the live site updates automatically.

---

## 🖼 Adding photos

1. Put the image file in the `photos/` folder (JPG, PNG, WebP all work)
2. In `people.csv`, set the `Photo` column to `photos/filename.jpg`
3. Recommended size: **200×200px** or larger square crop

If a photo path is wrong or missing, the dashboard shows a colored initials avatar instead.

---

## ✨ Features

- Shows everyone celebrating in the **current month** by default
- Navigate months with **← →** buttons or click the **month pills**
- Highlights **today's birthday** with a gold badge
- Shows the **age they're turning** this year
- Spinning gold ring around each avatar
- Fully responsive — works on mobile
- No server, no database, no dependencies — pure HTML + CSV

---

## 🛠 Customisation tips

All styles are in `index.html` under `<style>`. Key variables at the top:

```css
:root {
  --bg:      #0f0e17;   /* page background */
  --gold:    #e8c97e;   /* accent color */
  --accent:  #c77dff;   /* initials color */
  --radius:  16px;      /* card corner radius */
}
```

Change `--gold` to your brand color to match your team's palette.

---

## 📄 License

MIT — free to use and modify.
