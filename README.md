# pihole-lists

Domain lists for Pi-hole.

## Lists

| File | Type | Use |
|---|---|---|
| [`allow/school-chromebook.txt`](allow/school-chromebook.txt) | Allow | Domains a school-managed Chromebook needs (Google Classroom/Docs/Drive, ChromeOS, GoGuardian, Clever, IXL, Discovery Ed, etc.). Meant for a group that blocks everything else with the regex `.*`. |

## Using a list in Pi-hole (v6)

1. **Lists** → paste the raw URL, e.g. `https://raw.githubusercontent.com/jburns24/pihole-lists/main/allow/school-chromebook.txt`, and choose **Allow**.
2. Assign the list to the group the device belongs to (remove it from `Default` if it should only apply there).
3. **Tools → Update Gravity** (or `pihole -g`). Pi-hole only re-downloads lists on a gravity update (weekly by default), so run it after every edit here.

Format: one exact domain per line; `#` starts a comment.
