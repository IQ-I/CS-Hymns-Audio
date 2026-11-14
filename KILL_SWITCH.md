# Yorùbá voice: on/off switch (owner only)

The C&S Hymns app reads **`config/voice.json`** in this repo at launch and whenever it
comes back to the foreground. Only IQ-I org admins/maintainers can edit it.

## Turn the Yorùbá voice OFF (from your phone)
1. Open **https://github.com/IQ-I/CS-Hymns-Audio/edit/main/config/voice.json** in your phone's browser (signed in to GitHub).
2. Change `"enabled": true` to `"enabled": false` (line 4). Keep the quotes, commas and brackets exactly as they are.
3. Tap **Commit changes…** → **Commit changes**.

Turn it back ON the same way: `false` → `true`.

Optional: edit `"message"` to change the note people see while it's off.
Optional: remove `"female"` from `"voices"` to offer only the male voice (or vice-versa).

## How fast it takes effect
- Apps opened or brought to the foreground: **within about 1–2 minutes** of your commit.
- Apps already open and in use: **within about 5 minutes** (they re-check every 5 minutes).
- Turning it off **stops any Yorùbá audio that is playing** and shows your message, with a one-tap "Listen in English" where that hymn exists in English.
- No app update, no new build, no OTA is needed.

## Safety rules built into the app
- Only an explicit `"enabled": false` turns it off.
- If the file can't be read (offline, GitHub down, typo in the JSON), the app keeps the **last setting it successfully read**; if it has never read one, the voice stays **on**.
  → So after a typo, the switch simply doesn't change anything. Fix the typo and commit again.
- Check your edit: open https://raw.githubusercontent.com/IQ-I/CS-Hymns-Audio/main/config/voice.json — it should show your change (GitHub may take up to 5 min to show it there; the app bypasses that cache).
