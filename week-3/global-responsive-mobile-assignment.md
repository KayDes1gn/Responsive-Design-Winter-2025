# Global Project 1 Mobile Responsive Images Assignment 

## Step by Step

### 1. Copy your first semester global project root folder.

Copy the folder from your "CPanel Backup" folder on OneDrive (which should be the latest version). Or download a copy from the GWD server.

### 2. Paste it into your second semester "Responsive Design" class folder *on OneDrive*.

As a general rule, work from OneDrive unless your project has very large file sizes like photography or video. Such large projects can be backed up on OneDrive when completed, but can be problematic when being worked on because of the constant uploading/downloading that OneDrive performs.

### 3. Rename the folder to: "Global 1 Responsive Mobile Only".

Give it an obvious name to be able to tell it apart from the original.

### 4. Take an inventory of the images you used last semester:
   #### 1. Do they have good image quality?

    In a graphic and web design portfolio, bad images make your designs look bad. Get rid of anything weak.

   #### 2. Do you still have the original (large size) image to be able to resize the image properly this semester?

    If you don't have the large size original, replace it with something else now.

### 6. Swap the img tags for picture tags.

6.1 Open index.html

6.2 Preview the page in your web browser, but in normal desktop mode.

6.3 Inspect the image.

6.4 Using the web inspector's tools, resize the image until you like its appearance on desktop. This is the value of your **sizes** attribute.

6.5 Find the \<img> tag.

            <img src="img/picture-unsplash.jpg" alt="">

6.6 Take the time to add a meaningful alt text. 

- Bad alt text: "cake"

- Good alt text: "Pink frosted birthday cake with a number 3 lit candle on it, seen in a downward angle, placed on top of a wooden kitchen table with colorful balloons and a smiling toddler in a high chair." (Imagine describing what you see in the picture to a blind person!)

6.7 Wrap the img tag with a picture tag

            <picture>

             <source srcset="
                img/picture-unsplash-900.jpg 900w,
                img/picture-unsplash-450.jpg 450w"

                sizes="450px">


            <img src="img/picture-unsplash.jpg" alt="good alt text goes here">
            </picture>

Note that the value for the sizes attribute goes in "sizes" and corresponds to the pixel dimension of the **lowest image in the srcset order**. The **top image is twice the sizes value**.

In practical terms, the human eye cannot see more than 2x of the image's resolution. Only under very specific circumstances (specific display or image characteristics) is it necessary to provide 3x and 4x images.

View the file in the browser, then open the Console (click Console at the top of the web inspector, or hit the Escape key).

Use: $0.currentSrc to see which image is being loaded from the source list.

### 7. Add orientation for art direction purposes

Repeat the steps from Step 6 but with a landscape-oriented image.

#### How to Deal with Missing Orientation Alternatives

##### Landscape to Portrait

If you have a large scale horizontal original image available, you can simply crop the image to generate the portrait version.

##### Portrait to Landscape

If you have a large scale vertical original image available, you can may be able crop the image to generate the landscape version. Sometimes, however, this is not possible. Here's a trick:

1. Open the vertical image in Photoshop.
2. Go Image > Canvas Size
3. Add extra canvas size to one side of the image. Try to keep the photo at a 3:2 ratio.
4. Select the new blank area.
5. Click the Generate button to use AI to fill the blank area.
6. Save resized copies of the image as usual.
7. Add the new orientation images as a **second source** within the \<picture> tag.
8. Add the media="(orientation: portrait)" or media="(orientation: landscape)" inside the source.

        <picture>
            <source 
            media="(orientation: portrait)"
            srcset="
                img/picture-unsplash_900x1350.jpg 900w,
                img/picture-unsplash_450x675.jpg 450w"
                sizes="450px">

            <source 
            media="(orientation: landscape)"
            srcset="
                img/picture-unsplash-landscape_1400x933.jpg 1400w,
                img/picture-unsplash-landscape_700x467.jpg 700w"
                sizes="700px">    
    

            <img src="img/picture-unsplash-landscape_700x467.jpg" alt="">
        </picture>


Test the pages to see if your images are now responsive. View the file in the browser, then open the Console (click Console at the top of the web inspector, or hit the Escape key).

Use: $0.currentSrc to see which image is being loaded from the source list.

### 8. Upload to the GWD server.

As per usual, rename the folder so that it does not contain capital letters or spaces.

### 9. Test all the pages on the site on the live server.

Make sure all the images and css load, all the links are unbroken. 

Look at the Console to see if any errors are listed. Specifically, look for 404 errors (object not found = a broken link).

### 10. Copy the URL of the page.

Ex: https://billy-poppins.graphicandwebdesign.ca/global-1-responsive-mobile-only/

### 11. Switch to a different browser, paste the link into the URL bar. 

Check to see if the link you copied is good.


### 12. Submit the known good link via MIO.
