# Image Conversion Fix: RGBA to JPEG

## Issue

The error "cannot write mode RGBA as JPEG" occurs when attempting to save an image with transparency (RGBA mode) to JPEG format, which doesn't support transparency.

## Solution

This fix properly handles images with transparency by:

1. Detecting if the image has an alpha channel (transparency)
2. Creating a white background and pasting the transparent image on top
3. Converting any non-RGB mode to RGB before saving
4. Setting JPEG quality to 90 for better results

## Implementation

The fix has been applied to the following files:
- `pages/18_Describe_1.py`
- `pages/19_Describe_2.py`

Here's the code that was added:

```python
# Convert RGBA to RGB if the image has an alpha channel
if image.mode == 'RGBA':
    # Create a white background image
    background = Image.new('RGB', image.size, (255, 255, 255))
    # Paste the image on the background using alpha as mask
    background.paste(image, mask=image.split()[3])  # 3 is the alpha channel
    image = background
elif image.mode != 'RGB':
    # Convert any other mode to RGB
    image = image.convert('RGB')
    
buffered = BytesIO()
image.save(buffered, format="JPEG", quality=90)
image_bytes = buffered.getvalue()
```

## Testing

To test the fix:
1. Upload an image with transparency (PNG with alpha channel)
2. The image should be processed without errors
3. The resulting image will have a white background where transparency was

## Additional Information

This solution maintains the visual quality of the images while ensuring compatibility with the JPEG format required by the API.