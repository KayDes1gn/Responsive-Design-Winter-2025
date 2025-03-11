# Week 7 Notes

## Art Review

- Content vs Presentation 
- Not enough content in mocks

Images for the 5 Ws:

- Who: JAC students 
- What: BioBlitz (what is a bioblitz?)
- Where: JAC/Ste-Anne
- When: Date
- Why: Engage students in crowdsourced scientific data collection

Get images from Unsplash that illustrate this. 

Which images can be background (CSS background image) vs content (HTML picture tag)?



## Technical Review

- Q: What is the image size?
- Q: What is the text measure width? 

### Notes on Typography

#### The Ideal Line Length
- [https://baymard.com/blog/line-length-readability](https://baymard.com/blog/line-length-readability)

#### Line Length in Web vs Print
- [https://www.viget.com/articles/the-line-length-misconception/](https://www.viget.com/articles/the-line-length-misconception/)

#### Examples of CSS for Limiting Line Length

    p { /* paragraph only */
        max-width: 85ch; 
    } 

    h1,
    h2,
    h3,
    h4,
    h5,
    h6,
    legend,
    label,
    p,
    li { /* most on-screen text */
        max-width: 100ch; 
    }  

## Assignment

1. Create a standard html page
2. Add style tag inside head
3. Add multiple images using orientation media query and 1x + 2x resolutions. Image width is defined by column width in Figma. 
4. Remember that 2x images must be saved from same size or bigger images. **Not scaled up from smaller sizes.** 
5. Wrap elements (picture + picture, picture + text, etc) that will be side by side on larger screens inside a div. Use a "flex-container" class. 