# Going from Mobile Scale to Larger Viewports

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
    .when picture {
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


## Vertical Centering 

### Using line-height

When you have a single line of text, you can vertically center it using a line-height equal to the height of the parent element.

    footer {
        background-color: #2679d8;
        color: #fff;

        height: 5rem;
        line-height: 5rem;
        text-align: center;
    }


### Using Flex Box

    footer {
        background-color: #2679d8;
        color: #fff;
        height: 5rem;
        
        display: flex;
        align-items: center;
        justify-content: center;
    }