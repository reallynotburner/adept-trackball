# Ploopy Adept Trackball Aluminum Upgrade

The 3D printed, open source [Ploopy Adept Trackball](https://ploopy.co/product-category/trackball/adept/) is lovely, but let's upgrade the top of it with some 1.5mm thick Aluminum plate!

## Equipment

- [Snapmaker Artisan](https://us.snapmaker.com/products/snapmaker-artisan-3-in-1-3d-printer) or other CNC Mill
- 3D Printer
- [1.5 mm Aluminum Sheet](https://www.amazon.com/Aluminum-Protective-Polished-Deburred-Crafting/dp/B0B45GLLG8)
- Cheap Masking Tape (the good stuff doesn't stick well enough)
- CA (Superglue)
- Scotch 77 spray contact cement
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
- [Ploopy-Adept-Trackball-Profiles.cnc](Ploopy-Adept-Trackball-Profiles.cnc)
- [Ploopy-Adept-Trackball-Chamfering.cnc](Ploopy-Adept-Trackball-Chamfering.cnc)
You'll also need the modified Ploopy Adept body design which supports the new aluminum deck piece.  Convert it and slice it with your software of choice.  I use Fusion 360 and Prusa Slicer.  The only object you need to convert to stl is the "Body" object
- [Adept-Trackball-Upgrade.step](Adept-Trackball-Upgrade.step)

# Mounting Work in Mill
- This procedure is described in [this NYC CNC Youtube Video](https://www.youtube.com/watch?v=r6DCvtcU8_M). 
- Cover the bed of the mill in masking tape, sticky side down, without the tape overlapping itself and minimal gaps.
- Cover the bottom of the aluminum plate in the masking tape, without overlapping the tape and minimal gaps.
- Generously apply CA (superglue) to the mill bed masking tape surface evenly for complete coverage.
- Press the aluminum, tape-side-down, into the tape covered mill bed, roughly square to the mill's X and Y axes.

# Running the CNC Code
- Install a 1/8" 2-flute endmill in the mill spindle.
- Load [Ploopy-Adept-Trackball-Profiles.cnc](Ploopy-Adept-Trackball-Profiles.cnc) and zero your mill out with Z zero the top surface of the aluminum and XY Zero about 6mm mininum from the left and bottom edges of the aluminum plate.
- Running this will create the wastage, 6 buttons, and bezel parts.  If you don't evenly glue the work down in the mounting step, parts may fly off!
- Install 1/8" Chamfering tool in the mill spindle.
- Load [Ploopy-Adept-Trackball-Chamfering.cnc](Ploopy-Adept-Trackball-Chamfering.cnc) and repeat the zero procedure in the same spot as before.  The Snapmaker doesn't need the XY re-zeroed, but you must rezero Z every time you switch tools.  The Nomad 3 will need rezeroing because it loses about a half millimeter in the X and Y after each program it runs.
- Run the code, which should make really nice edges on the bezel and the buttons.

# Printing the new Body
- Open [Adept-Trackball-Upgrade.step](Adept-Trackball-Upgrade.step) in your 3d software of choice.  If you already have the Adept parts kit, you'll only need to export and print the "Body" component.  When you slice the Body for the 3d printer, orient the shape with the buttons flat against the printer bed.  I'm still working out the supports to make this work well... [TODO] FIX SUPPPORT ISSUE.

# Assembly
- Using a spatula, carefully peel the 6 buttons and bezel free of the mill bed.  Use rubbing alcohol or acetone to strip the tape residue off.
- Spray the underside of the bezel and buttons with the Scotch 77 contact cement.
- Spray the top of the Adept body with Scotch 77.  It's a good idea to mask the sides of the body to avoid overspray.
- As soon as all the sprayed surfaces are dry to the touch, align and press the matching parts together.  It should be a permanent bond that you'll need to destroy the Adept body to remove the aluminum parts.

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)