# Ploopy Adept Trackball Aluminum Upgrade

The 3D printed, open source [Ploopy Adept Trackball](https://ploopy.co/product-category/trackball/adept/) is lovely, but let's upgrade the top of it with some 1.5mm thick Aluminum plate!

## Equipment

- [Snapmaker Artisan](https://us.snapmaker.com/products/snapmaker-artisan-3-in-1-3d-printer) or other CNC Mill
- [1.5 mm Aluminum Sheet](https://www.amazon.com/Aluminum-Protective-Polished-Deburred-Crafting/dp/B0B45GLLG8)
- Cheap Masking Tape (the good stuff doesn't stick well enough)
- CA (Superglue)
- 1/8" 90° Chamfer bit
- 1/8" 2 flute endmill

## Code

The Snapmaker Artisan accepts EIA-ISO Numerical Machine Code, or "G Code" in plain text, with ".cnc" file extensions.

```eia-iso
;description: Generic Snapmaker Artisan
;spindle on clockwise at 55% of maximum speed
M3 P55

;wait 2 seconds
G4 S2

;startup in mm and absolute coordinate mode
G21
G90
...etc
```
You'll need to upload these two files to the CNC Mill via USB Stick
- [Cutting out the profiles of the bezel and buttons]()
- [Chamfering the edges of the bezel and buttons]()

# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')

```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)