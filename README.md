
# Keyboard Layout Setup for i3wm (Temporary)

## Method 1: setxkbmap (Session-only)

Add this line to your i3 config file at `~/.config/i3/config`:

```bash
exec --no-startup-id setxkbmap -layout us,ua,ru -variant ,winkeys, -option grp:alt_shift_toggle
```

### Layouts:
- `us`: English (default)
- `ua`: Ukrainian (with Windows key variant)
- `ru`: Russian (default variant)

### Key Features:
- Switch between layouts using `Alt+Shift`
- Ukrainian layout uses Windows-style key positions
- Changes apply immediately but won't persist after reboot

### Verification:
Check active layout with:
```bash
setxkbmap -query
```

### Manual Switching:
```bash
setxkbmap -layout ua  # Ukrainian
setxkbmap -layout ru  # Russian
setxkbmap -layout us  # English
```

+ Note: For permanent setup, use Xorg configuration or localectl methods.
