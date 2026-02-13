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

Run after Claude Code upgrades if you see "No such file or directory" errors.
