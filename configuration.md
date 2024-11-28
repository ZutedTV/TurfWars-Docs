# TurfWars Configuration

Complete guide to configuring TurfWars.

## Configuration Files

### config.yml

```yaml
# Economy Settings
economy:
  gang-creation-cost: 1000
  territory-claim-cost: 5000
  traphouse-creation-cost: 10000

# Gang Settings
gangs:
  min-name-length: 3
  max-name-length: 16
  max-members: 10
  tag-max-length: 5

# Territory Settings
territories:
  claim-size: 16
  max-claims: 5
  war-duration: 3600

# Trap House Settings
traphouses:
  income-interval: 3600
  base-income: 100
  max-level: 3

# Chat Settings
chat:
  enable-gang-chat: true
  enable-gang-tags: true
```

## Settings Explained

### Economy Settings

| Setting | Description | Default |
|---------|-------------|---------|
| `gang-creation-cost` | Cost to create a new gang | 1000 |
| `territory-claim-cost` | Cost to claim territory | 5000 |
| `traphouse-creation-cost` | Cost to create trap house | 10000 |

### Gang Settings

| Setting | Description | Default |
|---------|-------------|---------|
| `min-name-length` | Minimum gang name length | 3 |
| `max-name-length` | Maximum gang name length | 16 |
| `max-members` | Maximum gang members | 10 |
| `tag-max-length` | Maximum gang tag length | 5 |

### Territory Settings

| Setting | Description | Default |
|---------|-------------|---------|
| `claim-size` | Size of territory claims | 16 |
| `max-claims` | Maximum territories per gang | 5 |
| `war-duration` | War duration in seconds | 3600 |

### Trap House Settings

| Setting | Description | Default |
|---------|-------------|---------|
| `income-interval` | Seconds between income | 3600 |
| `base-income` | Base income per interval | 100 |
| `max-level` | Maximum trap house level | 3 |

### Chat Settings

| Setting | Description | Default |
|---------|-------------|---------|
| `enable-gang-chat` | Enable gang chat | true |
| `enable-gang-tags` | Show gang tags in chat | true |

## Advanced Configuration

### Economy Integration

TurfWars uses Vault for economy integration. Ensure you have:
1. Vault installed
2. An economy plugin installed
3. Proper permissions set up

### Chat Integration

For best results with chat:
1. Install EssentialsX
2. Configure chat format in EssentialsX
3. Enable gang tags in config.yml

### Performance Optimization

For large servers:
1. Adjust `income-interval` for trap houses
2. Consider limiting `max-claims`
3. Optimize `war-duration`

## Troubleshooting

### Common Issues

1. **Economy Not Working**
   - Check Vault installation
   - Verify economy plugin
   - Check permissions

2. **Chat Tags Not Showing**
   - Verify `enable-gang-tags`
   - Check EssentialsX config
   - Review permissions

3. **Territory Issues**
   - Check claim costs
   - Verify territory size
   - Review max claims

## Reloading Configuration

After making changes:
1. Save the file
2. Use `/gang admin reload`
3. Verify changes in-game
