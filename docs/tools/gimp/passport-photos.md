# Creating Passport Photos Using GIMP

This guide will help you create professional looking passport photos using GIMP (GNU Image Manipulation Program). The tutorial focuses on creating passport photos in the UK style format (45mm x 35mm), which is widely used in UK, Australia, New Zealand, India, and other countries.

## Prerequisites

- [GIMP](http://www.gimp.org/downloads/) installed on your computer
- A digital camera or smartphone with good quality camera
- Access to a photo printing home printer

## Photo Requirements

Before starting the editing process, ensure your original photo meets these basic requirements:

- Taken against a light, plain background
- Good lighting with no harsh shadows
- Clear, sharp and in focus
- Shows your full head and upper shoulders
- Neutral facial expression
- Eyes open and clearly visible
- No head covering (unless for religious or medical reasons)

## Step-by-Step Guide

### 1. Taking the Photo

1. Ask someone to take your photo against a light background
2. Take multiple photos to choose the best one
3. Ensure sufficient space above your head and visible shoulders
4. Keep the original high-quality image without compression

### 2. Initial Photo Editing

1. Open your photo in GIMP
2. From the Toolbox, select the "Rectangular Select" tool
3. Ensure "Fixed Aspect Ratio" is initially unticked
4. Draw a rectangle around your face
5. In the tool options (usually in the left pane):
   - Enter width = 350 px
   - Enter height = 450 px
   - Check "Fixed Aspect Ratio"
6. Adjust the selection to include:
   - Your full head (including hair)
   - Your face should fill approximately 75% of the frame
   - Proper centering of your face

### 3. Cropping and Resizing

1. Crop the image:
   - Go to Image → Crop to Selection
2. Resize the image:
   - Go to Image → Scale Image
   - Set width = 750 px
   - Height should automatically become 964 px
   - If height is not 964 px, recheck your aspect ratio and start over

### 4. Creating the Final Layout

1. Create a new GIMP window:
   - File → New
   - Set width = 814 px
   - Set height = 1092 px
   - Set background color to white
2. Copy your edited photo (Ctrl+C)
3. Paste into the new window (Ctrl+V)
4. Click on the white border to merge all layers
5. Create the photo sheet:
   - Go to Filters → Map → Tile
   - Click the chain symbol to disconnect width/height ratio
   - Set width = 3256 px
   - Set height = 2184 px
   - Ensure "Create New Image" is checked

### 5. Saving and Printing

1. Save the final image:
   - File → Export To
   - Save as JPG format
   - Set quality to 100% (no compression)
   - Use a descriptive name like "passportTile.jpg"
2. Printing options:
   - Save to USB stick for printing at a shop
   - For home printing:
     - Go to Image → Print Size
     - Set width = 6 inches
     - Set height = 4 inches
     - Print via File → Print

## Quick Reference (Measurements)

- Photo aspect ratio: 350 px × 450 px
- Scaled photo size: 750 px width (height will be 964 px)
- Initial canvas: 814 px × 1092 px
- Final tiled size: 3256 px × 2184 px
- Print size: 6 inches × 4 inches
