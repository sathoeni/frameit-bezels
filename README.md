# frameit-bezels

This repository contains device bezels (frames) used by the [frameit](https://github.com/sathoeni/frameit) application to generate beautiful App Store screenshots with device frames.

## Repository Structure

```
.
├── bezels/            # Directory containing all device bezel images
│   ├── iphone/       # iPhone bezels
│   └── ipad/         # iPad bezels
└── device-bezels.json # Device bezel metadata and configurations
```

## Contributing Device Bezels

To add support for a new device, follow these steps:

1. **Find Device Bezels**
   - Locate high-quality device bezels for your target device

2. **Prepare the Bezel Images**
   - Remove all transparent space around the bezel
   - Keep the image dimensions as small as possible while maintaining quality
   - Save the images in PNG format with transparency
   - Place the images in the appropriate directory under `bezels/`

3. **Update device-bezels.json**
   - Add a new entry to the JSON file following this structure:

```json
{
  "devices": [
    {
      "id": "iphone-15-pro-max",
      "name": "iPhone 15 Pro Max",
      "resolution": {
        "width": 1290,
        "height": 2796
      },
      "frames": [
        {
          "color": "black-titanium",
          "orientation": "portrait",
          "path": "bezels/apple/iphone/iPhone 15 Pro Max/iPhone 15 Pro Max - Black Titanium - Portrait.png"
        },
        {
          "color": "black-titanium",
          "orientation": "landscape",
          "path": "bezels/apple/iphone/iPhone 15 Pro Max/iPhone 15 Pro Max - Black Titanium - Landscape.png"
        }
      ]
    }
  ]
}
```

### JSON Fields Explanation
- `id`: Unique identifier for the device
- `name`: Display name of the device
- `resolution`: The actual screen dimensions of the device
- `frames`: Array of available frames for the device, each with:
  - `color`: Color variant of the device
  - `orientation`: Either "portrait" or "landscape"
  - `path`: Relative path to the bezel image file

4. **Submit a Pull Request**
   - Fork this repository
   - Create a new branch for your changes
   - Add your bezel images and update the JSON
   - Submit a pull request with a clear description of the added device

## License

This project is licensed under the MIT License - see the LICENSE file for details. 