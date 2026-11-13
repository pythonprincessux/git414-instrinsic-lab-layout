## Container Query Practice
Kiara McRae | GIT 414

### Component and Query Container
This week, I decided to adapt the reusable feature card and placed it in two parent
containers with maximum widths of 22rem and 60rem.

Each `.feature-shell` uses `container-type: inline-size` and the
container name `feature`. The card starts with a single-column layout.
At a container width of 36rem or greater, a container query changes
the card to two columns, placing the decorative gradient beside
the text.

### Why a Container Query
I chose this honestly because i thought it would be cool to show a side by side display. The same component appears in different-width parents within the
same viewport. A viewport-only media query would not distinguish
between those available widths. The container query lets each card
adapt to the space its own parent provides.

### Fallback
Without container-query support, the query is ignored and both cards
retain the usable single-column layout. The heading, description,
and action link remain available.

### Testing
I checked both parent widths in Chrome within the same browser window.
The narrow card stacked its gradient above the text. The wide card
displayed the gradient beside the text.

### AI Disclosure
I used ChatGPT to help troubleshoot syntax I applied the changes and checked
both component layouts in Chrome. I verified all broswer behavior through the live server launched through VS Code.