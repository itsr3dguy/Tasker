# Tasker Morning Briefing

This repository is a simple data source for an Android Tasker automation. Tasker fetches plain text files from this repo and reads them aloud using text-to-speech, giving you a personalised morning briefing every day.

---

## How It Works

Tasker uses HTTP Get actions to download each `.txt` file directly from GitHub's raw content URL, then passes the text to a Say or Text-to-Speech action. Because the files are plain text, you can edit them from any device and Tasker will read the updated version the next time it runs.

---

## Files in This Repo

| File | Purpose |
|---|---|
| `schedule.txt` | Your daily schedule, read aloud in the morning |
| `tasks.txt` | Your to-do list for the day |
| `weather_notes.txt` | A short weather note you fill in manually (or leave as a placeholder) |

---

## Raw URLs

Use these URLs in your Tasker HTTP Get action:

```
https://raw.githubusercontent.com/itsr3dguy/Tasker/main/schedule.txt
https://raw.githubusercontent.com/itsr3dguy/Tasker/main/tasks.txt
https://raw.githubusercontent.com/itsr3dguy/Tasker/main/weather_notes.txt
```

---

## How to Edit the Files

1. Open this repository on GitHub (from your phone or PC).
2. Click the file you want to edit (for example `tasks.txt`).
3. Click the pencil icon in the top-right corner of the file view.
4. Make your changes directly in the editor.
5. Scroll down and click **Commit changes**.

That's it. The next time Tasker runs your morning briefing, it will fetch and read the updated content.

---

## Tips

- Write everything in plain sentences or one item per line. Avoid symbols, markdown, or special characters that sound odd when read aloud.
- Keep each file short so the briefing does not run too long.
- You can leave `weather_notes.txt` empty or with a placeholder if you do not update it every day.
