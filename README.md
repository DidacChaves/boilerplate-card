# Boilerplate Card by [@DidacChaves](https://www.github.com/DidacChaves)

A community boilerplate of best practices for Home Assistant Lovelace custom cards

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE.md)
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg?style=for-the-badge)](https://github.com/custom-components/hacs)

![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

[![Community Forum][forum-shield]][forum]

## Options

| Name              | Type    | Requirement  | Description                                 | Default             |
| ----------------- | ------- | ------------ | ------------------------------------------- | ------------------- |
| type              | string  | **Required** | `custom:boilerplate-card`                   |
| name              | string  | **Optional** | Card name                                   | `Boilerplate`       |
| show_error        | boolean | **Optional** | Show what an error looks like for the card  | `false`             |
| show_warning      | boolean | **Optional** | Show what a warning looks like for the card | `false`             |
| entity            | string  | **Optional** | Home Assistant entity ID.                   | `none`              |
| tap_action        | object  | **Optional** | Action to take on tap                       | `action: more-info` |
| hold_action       | object  | **Optional** | Action to take on hold                      | `none`              |
| double_tap_action | object  | **Optional** | Action to take on double tap                | `none`              |

## Action Options

| Name            | Type   | Requirement  | Description                                                                                                                            | Default     |
| --------------- | ------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| action          | string | **Required** | Action to perform (more-info, toggle, call-service, navigate url, none)                                                                | `more-info` |
| navigation_path | string | **Optional** | Path to navigate to (e.g. /lovelace/0/) when action defined as navigate                                                                | `none`      |
| url             | string | **Optional** | URL to open on click when action is url. The URL will open in a new tab                                                                | `none`      |
| service         | string | **Optional** | Service to call (e.g. media_player.media_play_pause) when action defined as call-service                                               | `none`      |
| service_data    | object | **Optional** | Service data to include (e.g. entity_id: media_player.bedroom) when action defined as call-service                                     | `none`      |
| haptic          | string | **Optional** | Haptic feedback _success, warning, failure, light, medium, heavy, selection_ | `none`      |
| repeat          | number | **Optional** | How often to repeat the `hold_action` in milliseconds.                                                                                 | `none`       |

## Starting a new card from boilerplate-card

### Step 1

Click the "Use this template" button on the main page and clone the new repository to your machine

### Step 2

Install necessary modules (verified to work in node 18.x)

`yarn install` or `npm install`

### Step 3

Do a test lint & build on the project. You can see available scripts in the package.json

`yarn build` or `npm run build`

### Step 4

Search the repository for all instances of `TODO` and handle the changes/suggestions

### Step 5

Customize to suit your needs and contribute it back to the community

## Starting a new card from boilerplate-card with [devcontainer][devcontainer]

Note: this is available only in vscode ensure you have the [Remote Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension installed.

1. Fork and clone the repository.
2. Open a [devcontainer][devcontainer] terminal and run `npm start` when it's ready.
3. The compiled `.js` file will be accessible on
   `http://127.0.0.1:5000/boilerplate-card.js`.
4. On a running Home Assistant installation add this to your resources on your configuation -> panels:

```yaml
- url: 'http://127.0.0.1:5000/rainfall-tracker-card.js'
  type: module javascript
```

_Change "127.0.0.1" to the IP of your development machine._

## Credits

This project is based on the template provided by [@iantrich](https://www.github.com/iantrich).

Special thanks for their valuable contributions to the Home Assistant community and for sharing tools and resources that help others build amazing projects.

[commits-shield]: https://img.shields.io/github/commit-activity/y/DidacChaves/boilerplate-card.svg?style=for-the-badge
[commits]: https://github.com/DidacChaves/boilerplate-card/commits/master
[devcontainer]: https://code.visualstudio.com/docs/remote/containers
[discord-shield]: https://img.shields.io/discord/330944238910963714.svg?style=for-the-badge
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg?style=for-the-badge
[forum]: https://community.home-assistant.io/c/projects/frontend
[license-shield]: https://img.shields.io/github/license/DidacChaves/boilerplate-card.svg?style=for-the-badge
[maintenance-shield]: https://img.shields.io/maintenance/yes/2025.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/release/DidacChaves/boilerplate-card.svg?style=for-the-badge
[releases]: https://github.com/DidacChaves/boilerplate-card/releases
