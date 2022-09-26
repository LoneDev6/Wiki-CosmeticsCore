# 💾 Saving player data

## Configuration

```yaml
save:
  # Use only one at a time
  file:
    enabled: true
  mysql:
    enabled: false
    url: "jdbc:mysql://my_url_database_69.com:3306/database_name"
    username: "username"
    password: "password"
    table: "cosmeticscore_saved"

```

## File

This is the default method, it uses a wardrobe file for each player.

## MySQL

This is the method used by networks, this allows you to have multiple servers using the same wardrobe data for each player. Your players will then have the same equipped items when travelling on your network.\
(this obviously requires you to set up the plugin on each server with the same cosmetics files).
