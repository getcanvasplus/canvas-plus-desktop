# Canvas+ for Mac (beta)

**Your Canvas deadlines, grades and workload in the menu bar and on your desktop.** The Mac companion of the [Canvas+](https://getcanvasplus.com) Chrome extension. It uses the same rules and the same grade math.

[中文说明](README.zh-CN.md)

- **Main window**: an overview (greeting, clock, what's next, workload, grades), deadlines, a full month calendar, grades with the final calculator, and settings. A short welcome guides you the first time.
- **Menu bar panel**:
  - Every deadline across your courses, with a live countdown and how much of your final grade each one is worth.
  - Tick items off. This syncs with Canvas To Do.
  - Click an item to see its details or open it in Canvas.
- **Weekly load heatmap**: how busy the next 4 weeks are.
- **Grades and final calculator**: your grade in every course, what you need on the final for each letter, and a grade-breakdown chart.
- **Reminders**: a notification before a deadline, when a deadline moves, and when a course total changes.
- **Desktop widgets**:
  - Large: overview, list, calendar and grades.
  - Also deadlines, weekly load and grades in other sizes.
  - You can tick items off and switch tabs right in the widget.

Free. Needs **macOS 14 Sonoma or later**.

---

## Install

### 1. Download

Go to [**Releases**](https://github.com/getcanvasplus/canvas-plus-desktop/releases/latest) and download `CanvasPlus-x.y.z.dmg`.

### 2. Move it to Applications

Open the `.dmg` and drag **CanvasPlus** onto **Applications**.

### 3. Open it the first time

This beta isn't notarized by Apple, which costs $99 a year. The first time you open it, macOS says *"Apple could not verify 'CanvasPlus' is free of malware"*. That only means Apple hasn't reviewed it.

To allow it once:

1. Open **Applications** and double-click **CanvasPlus**. When the warning appears, click **Done** (or **Cancel**).
2. Open  **System Settings → Privacy & Security** and scroll down to **Security**.
3. Next to *"CanvasPlus" was blocked…*, click **Open Anyway**, then enter your Mac password.
4. Click **Open Anyway** once more in the dialog that appears.

From then on it opens normally.

<details>
<summary>Prefer Terminal? One command does the same.</summary>

```bash
xattr -dr com.apple.quarantine /Applications/CanvasPlus.app && open /Applications/CanvasPlus.app
```
</details>

### 4. Connect Canvas

When you open Canvas+, a welcome window walks you through this. You can also click the Canvas+ icon **in the menu bar**, at the top right of the screen, and open **Settings**:

1. **Find your school.** Type its name, for example "Ohio State", and pick it from the list. If your school isn't listed, choose *Enter the Canvas address myself* and type the address you use for Canvas (for example `https://osu.instructure.com`).
2. **Choose how to connect.** Pick one:
   - **School sign-in** (recommended, works at every school): click **Sign in…**. Your school's own sign-in page opens (SSO, Duo). Sign in as usual and the window closes by itself.
     - You type your password on your school's page and it goes only to your school. Canvas+ never sees or stores it. The top of the window shows which site you're on, so you can check it's your school.
     - Canvas+ keeps only the Canvas sign-in, in your keychain. When your school signs you out, the panel shows a **Sign in again** button.
   - **Access token** (if your school lets students make one; it doesn't expire):
     1. Click **Open Canvas settings**.
     2. In Canvas, under **Approved Integrations**, click **+ New Access Token**.
     3. Give it any name ("Canvas+ for Mac"), click **Generate Token** and copy the token.
     4. Paste the token in Canvas+ and click **Connect**.

Allow notifications when macOS asks. Then turn on **Open at login** in Settings, so reminders and widgets stay up to date.

### 5. Add the widgets

Right-click the desktop → **Edit Widgets…** → search **Canvas+**, then drag the ones you like onto the desktop.

---

## Update

Download the new `.dmg` from Releases and drag the app onto Applications again, choosing **Replace**. Your sign-in and settings are kept. If a widget looks wrong after an update, remove it and add it again.

## Uninstall

1. Click the menu bar icon → **Settings** → **Edit** → **Sign out** (or **Remove token**). If you used a token, also delete it in Canvas, under **Approved Integrations**.
2. Click **Quit Canvas+**, then drag **CanvasPlus** from Applications to the Trash.

## Questions

**Is it safe?**
- With School sign-in, you type your password only on your school's own page. Canvas+ doesn't read or store it.
- Your token or Canvas sign-in is stored in your Mac's **Keychain** and is only ever sent to your school's Canvas address.
- Nothing goes to us or to anyone else, and there are no analytics.

**My school isn't in the search, or there's no "New Access Token" button.** Some schools don't list themselves or turn off student tokens. Enter the Canvas address yourself. If there's no token button, use **School sign-in** instead.

**The widgets are empty or say "Open Canvas+ in the menu bar".**
1. Make sure Canvas+ is running in the menu bar and is connected.
2. Click ↻ in the panel.
3. If they stay empty, remove the widget and add it again.

If that doesn't help, please [open an issue](https://github.com/getcanvasplus/canvas-plus-desktop/issues). This beta isn't notarized, and on some Macs that can stop the widgets from reading the app's data.

**Why does ↻ in a widget need the app?** Widgets can't connect to Canvas themselves, so the menu bar app fetches the data and the widgets show it.

---

## Feedback and support

- Email: [support@getcanvasplus.com](mailto:support@getcanvasplus.com?subject=Canvas%2B%20feedback)
- Website: [getcanvasplus.com](https://getcanvasplus.com/)
- Found a bug? [Open an issue](https://github.com/getcanvasplus/canvas-plus-desktop/issues)

## License

© Baowen Liu. All rights reserved. Canvas+ for Mac is free to download and use for yourself; it may not be modified, sold or redistributed. See [LICENSE](LICENSE.md). The names **Canvas+** and **Canvas Plus** and the Canvas+ logo belong to the author.

Canvas is a trademark of Instructure, Inc. This project is independent and is not affiliated with or endorsed by Instructure or any school.
