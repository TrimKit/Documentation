# Installation

## Blender

Download the TrimKit `.zip` file. Leave it zipped — Blender installs it directly, there's nothing to extract first.

1. In Blender, go to **Edit > Preferences > Add-ons** (on some versions this tab is labeled **Get Extensions**).
2. Click the dropdown arrow in the top-right corner of that window and choose **Install from Disk**, then browse to and select the TrimKit `.zip` file.
3. Blender unpacks the `.zip` itself, into its own extensions/add-ons folder — you don't need to know or manage that location.
4. Find TrimKit in the resulting list (search the box at the top if it doesn't jump into view) and tick the checkbox next to its name to enable it.
5. With TrimKit enabled, open it in the 3D Viewport with the keyboard shortcut **Shift + Alt + T** (the default binding).

### Changing the Blender Shortcut

To change that shortcut, go to **Edit > Preferences > Keymap**, search for **TrimKit**, expand the entry under the **Window** category, and click the key combination field to record a new one.

## 3ds Max

Download the TrimKit `.mzp` file (a self-installing 3ds Max script package — don't unzip or open it, it installs itself).

1. With 3ds Max open, drag the `.mzp` file from Explorer straight into the viewport and drop it there.
2. Max unpacks it automatically, copying the TrimKit script into its Max scripts/startup folder and registering it as a macroscript — there's no install dialog to click through.
3. Open **Customize > Customize User Interface**.
4. In any of its tabs (**Toolbars, Menus, Quads, or Keyboard**), set the **Category** dropdown to **TrimKit** to find the installed script there.
5. From there, drag TrimKit onto a toolbar (Toolbars tab) or a menu (Menus tab) to give it a clickable button, or select it on the Keyboard tab and type a key combination into the Hotkey field, then click **Assign**.
6. 3ds Max doesn't ship TrimKit with a default hotkey — you're choosing one for the first time here.

Once set up this way, TrimKit can be launched from whichever of those you added — its keyboard shortcut, a toolbar button, or a menu entry.
