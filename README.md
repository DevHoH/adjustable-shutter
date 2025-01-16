<script type="text/javascript" src="https://cdnjs.buymeacoffee.com/1.0.0/button.prod.min.js" data-name="bmc-button" data-slug="DevHoH" data-color="#FFDD00" data-emoji=""  data-font="Arial" data-text="Buy me a coffee" data-outline-color="#000000" data-font-color="#000000" data-coffee-color="#ffffff" ></script>


# hass-shutter-card

A custom Lovelace card for Home Assistant to control shutters and blinds with ease and style. This project is a fork of [hass-shutter-card](https://github.com/Deejayfool/hass-shutter-card), with enhancements and improvements tailored for a better user experience.

## Features

- Intuitive and modern user interface
- Displays shutter/blind states in real-time
- Fully customizable appearance
- Compatible with various shutter and blind integrations

## Installation

### Manual Installation

1. Download the `hass-shutter-card.js` file from the [releases section](https://github.com/DevHoH/adjustable-shutter/releases).
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
type: custom:shutter-card
title: Küche
entities:
  - entity: cover.rollo_kuche1_vorhang
    name: rechts
    buttons_position: left
    title_position: bottom
    invert_buttonlogic: false
    invert_percentage: true

```

### Configuration Options

#### General
| Name              | Type    | Required | Default | Description                                   |
|-------------------|---------|----------|---------|-----------------------------------------------|
| `type`            | string  | True     | -       | Must be `custom:shutter-card`.               |
| `title`           | string  | False    | -       | Title of the card.                           |

#### Entities
| Name                      | Type    | Required | Default                 | Description                                                                         |
|---------------------------|---------|----------|-------------------------|-------------------------------------------------------------------------------------|
| `entity`                  | string  | True     | -                       | The shutter entity ID.                                                              |
| `name`                    | string  | False    | Friendly name of entity | Name to display for the shutter.                                                   |
| `buttons_position`        | string  | False    | left                    | Set buttons on left, right, top, or bottom of the shutter.                          |
| `title_position`          | string  | False    | top                     | Set title on top or bottom of the shutter.                                          |
| `invert_percentage`       | boolean | False    | false                   | Set to true if your shutter is 100% when closed and 0% when opened.                 |
| `can_tilt`                | boolean | False    | false                   | Set to true if your shutters support tilting.                                       |
| `partial_close_percentage`| int     | False    | 0                       | Percentage (0-100) for a quick "partially closed" state.                            |
| `offset_closed_percentage`| int     | False    | 0                       | Percentage (0-100) of travel considered "closed" in the visualization.              |
| `always_percentage`       | boolean | False    | false                   | If true, end states (open/closed) will also be displayed as numbers (0/100%).       |
| `shutter_width_px`        | int     | False    | 153                     | Shutter visualization width in px, adjustable to fit your layout.                  |
| `disable_end_buttons`     | boolean | False    | false                   | If true, deactivates direction buttons (e.g., "up" when fully open).                |
| `invert_buttonlogic`     | boolean | False    | false                   | If true, up and down are swapped, necessary for certain curtain modules.             |

## Screenshots

![Shutter Card Example](https://raw.githubusercontent.com/DevHoH/adjustable-shutter/master/images/shutter-card.gif)

## Contributing

Contributions are welcome! If you have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
