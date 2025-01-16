# hass-shutter-card

A custom Lovelace card for Home Assistant to control shutters and blinds with ease and style. This project is a fork of [hass-shutter-card](https://github.com/Deejayfool/hass-shutter-card), with enhancements and improvements tailored for a better user experience.

## Features

- Intuitive and modern user interface
- Displays shutter/blind states in real-time
- Fully customizable appearance
- Compatible with various shutter and blind integrations

## Installation

### Manual Installation

1. Download the `hass-shutter-card.js` file from the [releases section](https://github.com/your-repo-link/releases).
2. Place the file in your Home Assistant configuration directory under `/www/community/hass-shutter-card/`.
3. Add the following to your `resources` in `configuration.yaml` or through the Home Assistant UI:
   ```yaml
   resources:
     - url: /local/community/hass-shutter-card/hass-shutter-card.js
       type: module
   ```

### HACS Installation

1. Open the Home Assistant Community Store (HACS).
2. Search for `hass-shutter-card` in the Frontend section.
3. Click "Install" and follow the prompts.
4. Add the resource as described above if not added automatically.

## Usage

Add the following to your Lovelace configuration:

```yaml
type: 'custom:hass-shutter-card'
entity: cover.living_room_shutter
title: Living Room Shutter
show_buttons: true
show_position: true
```

### Configuration Options

| Option         | Type    | Description                                    | Default |
|----------------|---------|------------------------------------------------|---------|
| `type`         | string  | Must be `custom:hass-shutter-card`.           | N/A     |
| `entity`       | string  | Entity ID of the shutter or blind.            | N/A     |
| `title`        | string  | Title displayed above the card.               | `null`  |
| `show_buttons` | boolean | Whether to show open/close buttons.           | `true`  |
| `show_position`| boolean | Whether to display the current position.      | `true`  |

## Screenshots

![Shutter Card Example](https://via.placeholder.com/800x400)

## Contributing

Contributions are welcome! If you have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
