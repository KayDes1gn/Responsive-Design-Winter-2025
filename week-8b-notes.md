# Going from Mobile Scale to Larger Viewports

## Controlling Page Layout at Different Viewport Sizes: Media Queries

<blockquote>

1. Media: The technology used to transmit the content.
2. Query: A question.
3. "Media Query": The web browser asks the device's operating system what it is capable of, and displays the page accordingly.

</blockquote>

### Examples

- @media screen {}: Rules for computer screens
- @media print {}: Rules for formatting the page when printed
- @media screen and (orientation: portrait) {}: Rules for computer screens that are taller than they are wide
- @media screen and (min-width: 64rem) {}: Rules for computer screens that are wider than 64rem
- @media screen and (max-width: 640px) {}: Rules for computer screens that are narrower than 640px
- @media screen and (max-width: 640px) and (orientation: portrait) {}: Rules for computer screens that are narrower than 640px and taller than they are wide

### Mobile First

"Mobile first" is the simplest strategy for designing responsive web page.

1. Start with no media queries at all: Define all the styles for the mobile phone design.
2. Once the viewport is wide enough for **two columns** of content, use a media query that puts content side-by-side *starting at that width*.
3. Once the viewport is wide enough for **three columns** of content, use a media query that puts content side-by-side *starting at that width*.
4. Repeat as many times as necessary depending on how many columns you need.
5. Once you reach laptop/desktop widths, use a "wrapper" div (a fixed width box that surrounds all the content) to center the page contents.



## Setting elements side-by-side

### Using Flex Box

#### The Basic Alignment

    .flex-container {
        display: flex;
        /* put elements side-by-side */
    }

#### Switching the Items Order

    .when .flex-container {
        flex-direction: row-reverse;
        /* places elements in reverse order: second element becomes first */
    }

#### Setting Column Width

    .when p,
    .when picture,
    .why p,
    .why picture {
	    flex-basis: 50%;
    }


### Using CSS Grid

#### The Basic Alignment & Column Width

     .how .flex-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        /* two columns: each equal to one fraction of the available space */
    }

#### Switching the Items Order

    .how picture {
        order: 2;
        /* force to go to column 2 */
      }

    .how .flex-container div {
        order: 1;
        /* force to go to column 1 */
    }


## Horizontal & Vertical Centering 

### Using line-height

When you have a single line of text, you can vertically center it using a line-height equal to the height of the parent element. Then you can use regular text centering.

    footer {
        background-color: #2679d8;
        color: #fff;

        height: 5rem;
        line-height: 5rem;
        /* the line of text is the same height as the box it is in: vertical centering */

        text-align: center;
        /* horizontal centering */
    }


### Using Flex Box

    footer {
        background-color: #2679d8;
        color: #fff;
        height: 5rem;
        
        display: flex;

        align-items: center;
        /* vertical centering */

        justify-content: center;
        /* horizontal centering */
    }