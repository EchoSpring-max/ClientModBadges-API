# ClientModBadges Static API

This fork provides badge data and images without requiring a continuously running server. GitHub Actions refreshes the data every hour and GitHub's raw-content CDN serves it to the matching GlobalBadges plugin.

The companion plugin is available at [EchoSpring-max/GlobalBadges](https://github.com/EchoSpring-max/GlobalBadges).

### Supported client mods:

- [Aliucord](https://github.com/Aliucord/Aliucord)
- [BetterDiscord](https://github.com/BetterDiscord/BetterDiscord)
- [BadgeVault](https://github.com/WolfPlugs/BadgeVault)
- [Enmity](https://github.com/enmity-mod/enmity)
- [Replugged](https://github.com/replugged-org/replugged)
- [Vencord](https://github.com/Vendicated/Vencord)

### Static endpoints

`https://raw.githubusercontent.com/EchoSpring-max/ClientModBadges-API/main/users/:userId.json` returns badges for a user.

`https://raw.githubusercontent.com/EchoSpring-max/ClientModBadges-API/main/badges/:clientMod/:badge.png` returns a built-in badge image.

For example:

`https://raw.githubusercontent.com/EchoSpring-max/ClientModBadges-API/main/users/354191516979429376.json`

### Response format

Example Response:

```json
{
    "BadgeVault": [
        {
            "name": "Astronaut",
            "badge": "https://gb.obamabot.me/1fdb7e114a428c3d7a063f15d7616b59447e490f.png"
        }
    ],
    "Enmity": [
        "supporter"
    ],
    "Vencord": [
        "Contributor"
    ]
}
```

## Contributing

We welcome contributions to the ClientModBadges-API! If you're looking to contribute, here's how you can help:

- **Support for New Client Mods:** If you want to add support for a new client mod, please ensure it is not a fork of an existing mod unless the original mod has reached its end-of-life (EOL). In such cases, contributions to support forks are acceptable.

- **Feature Requests:** If you have ideas on how to improve the API or add new features, we encourage you to open a feature request. This helps us understand what the community needs and prioritize accordingly.

- **Bug Reports:** If you encounter any bugs or issues, please report them by opening an issue. Provide as much detail as possible to help us understand and fix the problem quickly.

Remember, all contributions should aim to improve the API and support the wider community of client mod users. We look forward to your contributions!
