# Making the First Semester Global Project Responsive

## Objectives

1. Replace all \<img> tags with responsive \<picture> tags.
2. Each \<picture> will have a portrait and a landscape image version available.
3. Reduce overall image file size, bandwidth usage and total energy consumption by providing files specifically tailored to how they will be displayed.

## Determining the Sizes Attribute

<blockquote>

Using the largest screen available to you (ie desktop), test to see just how big you want the image to be at **its biggest size**. This is a purely visual design decision. The technical aspects follow upon *what you want the page to look like*.

</blockquote>

The "sizes" attribute of the image is determined by testing **on desktop**.
   1. What picture size looks good to the designer.
   2. The image is **not so big that it forces the viewer to scroll vertically** to see the contents of the footer on an otherwise rather empty page.

## What This Assignment Does Not Cover

These aspects of responsive design will be covered later this semester:

- Page layout
- CSS background images
- SVG files


## Beware of Old CSS Rules

If you used CSS to resize your images last semester, please delete those rules (or delete the height and/or width properties within the rules) from your stylesheet.

The only CSS that should be affecting your images is the "golden responsive images rule":

### Bad (Delete all rules like this one)

    img.myPicture {
        width: 234px;
        height: 362px;
    }


### Bad (Delete some parts of rules like this one)

    .myimages {
        width: 234px; /* delete this property */
        height: 362px;  /* delete this property */

        margin: 2rem;  /* these two are okay to keep as is */
        border: 1px solid #444;
    }


### Good (All you really need)

    img {
        max-width: 100%;
        height: auto;
    }


## Evaluation

Each image (previously added with an \<img> tag, not as a CSS background, and not a SVG) must be converted to a \<picture> tag with both portrait and landscape options.

### Example

- 5 page web site X 2 images per page = 10 images to check X 2 orientations = 20pts
- The two orientations must load appropriately.
- The resolution switching (1x and 2x) must function properly.