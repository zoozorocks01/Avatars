# Install or update Maple

For Cosmo Royal, use the [Cosmo installation guide](cosmo/README.md).

Maple is a friendly red-fox prototype. Some movements remain a little stiff.

## Before you start

You need a desktop app version that supports **local custom pets**. The instructions reflect a tested Mac app build; menus may differ. This is not a phone pet or standalone app. A public download from this repository requires no GitHub sign-in.

## Install

1. Download [Maple V2.1](https://github.com/zoozorocks01/Avatars/raw/refs/heads/main/maple/v2.1/Maple-v2.1.0-Prototype.zip) and unzip it.
2. In the host app, open **Settings → Pets → Custom pets → Open folder**, if available.
3. Copy the extracted **maple-v2-1** folder into that custom-pet folder. Copy the whole folder, not just the image.

   ```text
   pets/
     maple-v2-1/
       pet.json
       spritesheet.webp
   ```

4. Return to Pets settings and choose **Refresh**. Select **Maple V2.1 Prototype**, then **Show pet** or **Wake Pet** if hidden.

The app may cache images. If the old artwork remains, select another pet and then Maple again. Restart the app yourself if needed, after saving your work. Refreshing/restarting should not require deleting application data.

On a Mac, the default folder used during development was `~/.codex/pets/`. Finder's **Go → Go to Folder…** accepts this path. Prefer the app's **Open folder** button: your configuration may use a different location. On other operating systems, do not guess an equivalent path.

If your app lacks local Custom pets/Open folder, stop and check compatibility. This ZIP is not a verified one-click import format.

## Update an existing Maple

1. Check the [Maple page](https://github.com/zoozorocks01/Avatars/tree/main/maple) for a new version.
2. Before replacing `maple-v2-1`, copy the old folder to a safe backup location **outside** the active pets folder. Keep it until the new version works.
3. Replace only the two pet files in `maple-v2-1` with the new version's files. If you customized them, preserve your changes and ask before overwriting.
4. Refresh/reselect Maple and test her. Future versions retain the same installation folder; do not create a new pet folder for every version.

An older pet named `maple` is separate and should not be deleted. You can switch back to it at any time.

## Quick check

- Drag Maple left and right to check the trot and tail.
- Leave her at rest to check her blink/idle.
- Watch her return from an action to standing.
- Some actions are triggered by app activity and won't all run on demand.
- Reduced Motion can limit animation. Change that preference only if you want more movement and are comfortable doing so.
- Following typed text is not the same as following every physical mouse movement.

The included GIF is a preview, not an installable pet. There is no need to run a script, provide credentials, or upload your app settings anywhere.

## Roll back or remove

To roll back, restore the two files from your saved backup, then refresh/reselect Maple. To remove this version, move only `maple-v2-1` out of the active pets folder, refresh, and select another pet. Keep that folder if you may want to restore her later.

## For an agent

See [AGENT-INSTALL.md](https://github.com/zoozorocks01/Avatars/blob/main/AGENT-INSTALL.md) for exact file checks, update comparison and safe rollback guidance.
