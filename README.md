# Utilities

Personal utility scripts and tools.

## Scripts

### claude-nixos-patcher

Auto-patches Claude Code binaries for NixOS compatibility after upgrades.

**Usage:**
```bash
./claude-nixos-patcher
```

**What it does:**
- Scans `~/.local/share/claude/versions/` for Claude binaries
- Patches dynamic linker paths for NixOS using patchelf
- Updates symlinks to point to the latest version
- Runs comprehensive diagnostics (interpreter validation, permissions)
- Verifies Claude Code works after patching

**Installation:**
```bash
cp claude-nixos-patcher ~/.local/bin/
chmod +x ~/.local/bin/claude-nixos-patcher
```

**When to run:**

Run after Claude Code upgrades if you see this error:
```
Could not start dynamically linked executable: claude
NixOS cannot run dynamically linked executables intended for generic
linux environments out of the box.
```
