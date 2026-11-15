## Day 06

1. A box with `width: 300px; padding: 20px; border: 5px solid`. What's its rendered width under content-box, and what is it under border-box?
   - Prediction: content-box = 350px (300 + 20 + 20 + 5 + 5). border-box = 300px (width already includes padding and border; content area is 250px).

2. An h2 with `margin-bottom: 30px` followed by a p with `margin-top: 20px`. How big is the gap between them?
   - Prediction: 30px. Adjacent vertical margins collapse to the larger of the two.

3. A coloured `<header>` whose first child is an h1 with `margin-top: 40px`. What happens to the header?
   - Prediction: The h1’s top margin collapses through the header (no padding-top, no border-top, overflow visible). The 40px sits outside the header, so the background does not cover it and the h1 sits flush with the top of the coloured box.
