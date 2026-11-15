## Day 06

1. A box with `width: 300px; padding: 20px; border: 5px solid`. What's its rendered width under content-box, and what is it under border-box?
   - Prediction: content-box = 350px (300 + 20 + 20 + 5 + 5). border-box = 300px (width already includes padding and border; content area is 250px).
   - Actual result: Matches. In the playground the content-box card is clearly wider. DevTools on the border-box card showed a 250px content area with 20px padding and 5px border on each side, so the whole box is 300px. content-box treats 300px as content only, so padding and border add on and it lands at 350px.

2. An h2 with `margin-bottom: 30px` followed by a p with `margin-top: 20px`. How big is the gap between them?
   - Prediction: 30px. Adjacent vertical margins collapse to the larger of the two.
   - Actual result: Matches. The 30px and 20px do not add. They collapse into one 30px gap, which is the bigger of the two.

3. A coloured `<header>` whose first child is an h1 with `margin-top: 40px`. What happens to the header?
   - Prediction: The h1’s top margin collapses through the header (no padding-top, no border-top, overflow visible). The 40px sits outside the header, so the background does not cover it and the h1 sits flush with the top of the coloured box.
   - Actual result: Matches. On the leaking header the orange background starts at the h1 — the 40px gap is above the coloured box, not inside it. Adding padding on the second header stops the collapse, so the heading sits inside the orange.
