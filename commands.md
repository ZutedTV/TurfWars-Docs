# TurfWars Commands

Complete list of all available commands in TurfWars.

## Gang Commands

### Basic Gang Management
| Command | Description | Permission |
|---------|-------------|------------|
| `/gang create <name>` | Create a new gang | `turfwars.gang.create` |
| `/gang invite <player>` | Invite a player | `turfwars.gang.invite` |
| `/gang kick <player>` | Kick a member | `turfwars.gang.kick` |
| `/gang leave` | Leave your gang | - |
| `/gang info [gang]` | View gang info | - |

### Gang Customization
| Command | Description | Permission |
|---------|-------------|------------|
| `/gang color <color>` | Set gang color | `turfwars.gang.color` |
| `/gang tag <tag>` | Set gang tag | `turfwars.gang.tag` |

### Gang Management
| Command | Description | Permission |
|---------|-------------|------------|
| `/gang promote <player>` | Promote a member | `turfwars.gang.promote` |
| `/gang demote <player>` | Demote a member | `turfwars.gang.demote` |
| `/gang bank <deposit/withdraw> <amount>` | Manage gang bank | `turfwars.gang.bank` |

### Gang Communication
| Command | Description | Permission |
|---------|-------------|------------|
| `/gang chat` | Toggle gang chat | - |
| `/prefix toggle` | Toggle gang prefix | - |

## Territory Commands

### Basic Territory Management
| Command | Description | Permission |
|---------|-------------|------------|
| `/turf claim` | Claim territory | `turfwars.turf.claim` |
| `/turf unclaim` | Unclaim territory | - |
| `/turf info` | View territory info | - |
| `/turf list` | List all territories | - |

### Territory Warfare
| Command | Description | Permission |
|---------|-------------|------------|
| `/turf war <gang>` | Declare war | `turfwars.turf.war` |
| `/turf map` | View territory map | `turfwars.turf.map` |

## Trap House Commands

### Basic Trap House Management
| Command | Description | Permission |
|---------|-------------|------------|
| `/traphouse create` | Create trap house | `turfwars.traphouse.create` |
| `/traphouse delete` | Delete trap house | - |
| `/traphouse info` | View trap house info | - |

### Trap House Economy
| Command | Description | Permission |
|---------|-------------|------------|
| `/traphouse collect` | Collect earnings | - |
| `/traphouse upgrade` | Upgrade trap house | `turfwars.traphouse.upgrade` |

## Admin Commands

### Gang Administration
| Command | Description | Permission |
|---------|-------------|------------|
| `/gang admin delete <gang>` | Delete a gang | `turfwars.admin` |
| `/gang admin reload` | Reload config | `turfwars.reload` |

### Territory Administration
| Command | Description | Permission |
|---------|-------------|------------|
| `/turf admin reset` | Reset territories | `turfwars.admin` |

### Trap House Administration
| Command | Description | Permission |
|---------|-------------|------------|
| `/traphouse admin remove <location>` | Remove trap house | `turfwars.admin` |

## Command Arguments

### Colors
Available colors for `/gang color`:
- RED
- BLUE
- GREEN
- YELLOW
- PURPLE
- AQUA
- WHITE
- GRAY

### Tags
Requirements for `/gang tag`:
- Maximum 5 characters
- Alphanumeric characters only
- No offensive content

### Bank Operations
Available operations for `/gang bank`:
- `deposit <amount>`: Add money to gang bank
- `withdraw <amount>`: Take money from gang bank
