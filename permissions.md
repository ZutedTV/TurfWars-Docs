# TurfWars Permissions

Complete list of permissions and their functions in TurfWars.

## Permission Groups

### Basic Permissions
| Permission | Description | Default |
|------------|-------------|---------|
| `turfwars.gang.create` | Create gangs | true |
| `turfwars.gang.join` | Join gangs | true |
| `turfwars.gang.chat` | Use gang chat | true |
| `turfwars.turf.view` | View territories | true |

### Gang Management
| Permission | Description | Default |
|------------|-------------|---------|
| `turfwars.gang.invite` | Invite players | false |
| `turfwars.gang.kick` | Kick members | false |
| `turfwars.gang.color` | Set gang color | false |
| `turfwars.gang.tag` | Set gang tag | false |
| `turfwars.gang.bank` | Use gang bank | false |

### Territory Management
| Permission | Description | Default |
|------------|-------------|---------|
| `turfwars.turf.claim` | Claim territory | false |
| `turfwars.turf.unclaim` | Unclaim territory | false |
| `turfwars.turf.war` | Declare wars | false |
| `turfwars.turf.map` | View territory map | true |

### Trap House Management
| Permission | Description | Default |
|------------|-------------|---------|
| `turfwars.traphouse.create` | Create trap houses | false |
| `turfwars.traphouse.delete` | Delete trap houses | false |
| `turfwars.traphouse.upgrade` | Upgrade trap houses | false |
| `turfwars.traphouse.collect` | Collect income | true |

### Administrative
| Permission | Description | Default |
|------------|-------------|---------|
| `turfwars.admin` | All admin commands | op |
| `turfwars.reload` | Reload config | op |
| `turfwars.bypass` | Bypass protection | op |

## Permission Sets

### Default Player
```yaml
permissions:
  - turfwars.gang.create
  - turfwars.gang.join
  - turfwars.gang.chat
  - turfwars.turf.view
  - turfwars.traphouse.collect
```

### Gang Leader
```yaml
permissions:
  - turfwars.gang.*
  - turfwars.turf.claim
  - turfwars.turf.unclaim
  - turfwars.turf.war
  - turfwars.traphouse.create
  - turfwars.traphouse.upgrade
```

### Administrator
```yaml
permissions:
  - turfwars.admin
  - turfwars.reload
  - turfwars.bypass
```

## Permission Inheritance

### Gang Hierarchy
1. **Leader**
   - All gang permissions
   - Territory management
   - Bank access

2. **Officer**
   - Member invite/kick
   - Territory viewing
   - Limited bank access

3. **Member**
   - Basic gang features
   - Territory access
   - Chat access

## Implementation

### Using LuckPerms
```yaml
groups:
  gang-leader:
    permissions:
    - turfwars.gang.*
    - turfwars.turf.claim
    - turfwars.turf.war
    
  gang-officer:
    permissions:
    - turfwars.gang.invite
    - turfwars.gang.kick
    - turfwars.turf.view
    
  gang-member:
    permissions:
    - turfwars.gang.chat
    - turfwars.turf.view
```

### Using GroupManager
```yaml
groups:
  gang-leader:
    permissions:
      - turfwars.gang.*
      - turfwars.turf.*
      
  gang-officer:
    permissions:
      - turfwars.gang.invite
      - turfwars.gang.kick
      
  gang-member:
    permissions:
      - turfwars.gang.basic
```

## Troubleshooting

### Common Issues

1. **Players Can't Create Gangs**
   - Check `turfwars.gang.create`
   - Verify economy setup
   - Check console for errors

2. **Territory Protection Not Working**
   - Review `turfwars.bypass`
   - Check territory claims
   - Verify protection settings

3. **Chat Problems**
   - Check `turfwars.gang.chat`
   - Verify chat settings
   - Review format config
