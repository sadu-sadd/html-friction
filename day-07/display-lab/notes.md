## Day 07 display lab

### Results

1. Same width, padding, margin, background, and red outline on an inline span and an inline-block span.

   Prediction: `.a` stays in the line. `width: 150px` does nothing, and the top and bottom margin do nothing. The left and right margin and padding still push the words beside it. The top and bottom padding still paint, so the yellow and the red outline spill onto the lines above and below without opening a gap for themselves. `.b` honors all of it. The content box is 150px wide, padding adds 20px on each side, and the 20px margin applies above and below as well as on the sides. That tall box stretches its line. The words inside `.b` sit on the same baseline as the words next to it, so the extra padding hangs above and below that baseline.

   What happened: That split is what shows up. `.a` is inline, so the box hugs the words "span a" and the 150px width never arrives. Horizontal padding and margin separate it from the nearby words. Vertical margin adds no space. Vertical padding and the outline overlap the surrounding lines. `.b` becomes a wide yellow box with real space around it, and the line it sits on grows to hold the box. In the DevTools box model for `.a`, the content width should match the text, not 150px. Padding should be 20px on every side. Left and right margin should be 20px. Top and bottom margin should show as not applied.

2. An image in a bordered div, then the baseline gap removed.

   Prediction: The image is inline, so its bottom rests on the text baseline. The line still reserves a strip under that baseline for descenders. The strip shows inside the border, under the picture. `display: block` on the image takes it off the baseline, the strip disappears, and the border meets the image.

   What happened: The first frame leaves the image inline, so the gap under the cat is that descender strip. The second frame only adds `display: block` to the image. The gap is gone and the border sits against the picture.
