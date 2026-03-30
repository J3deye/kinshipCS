# Connections
Infrastructure and tooling reference for KinshipAssist / Customer Success.

## VM
| | |
|---|---|
| Platform | Parallels Desktop (Mac host) |
| OS | Ubuntu 24.04 (ARM64) |
| User | parallels |

## Shared Folder (drag and drop)
| | |
|---|---|
| Mac path | /home/parallels/Desktop/Parallels Shared Folders/Ubuntu |
| Purpose | File transfer between Mac and VM. Primary drop zone for assets and files handed to CC. |

## GitHub
| | |
|---|---|
| Org | J3deye |
| Repo | kinshipCS |
| Clone path (VM) | ~/kinshipCS |
| Auth | GitHub CLI (gh) |

## Directory Structure
| Path | Purpose |
|---|---|
| ~/kinshipCS/pres | Presentation HTML files |
| ~/kinshipCS/pres/assets | Images, GIFs, and media for presentations |

## Tooling
| Tool | Purpose |
|---|---|
| CC (Claude Code) | Primary dev agent. Runs in VM. Handles file edits, path updates, git commits. |
| gh | GitHub CLI. Handles auth and repo operations. |
| npm (global prefix: ~/.npm-global) | Package manager. Required for CC. |
| gnome-terminal | Default terminal. Set via update-alternatives. |

## Notes
- npm global installs use `~/.npm-global` due to permissions — already configured in `~/.bashrc`
- Shared folder is the handoff point between Mac and CC — drop files there, CC picks them up
- Image paths in presentations use relative paths (`assets/filename`) for portability
