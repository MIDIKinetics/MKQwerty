# MKQwerty

A Lemur implementation of an ASCII keyboard.

## Installation

1. Click the green "Code" button at the top of this page and download the zip files.
2. Drag and drop **MKQwerty.jzlib** into one of your Lemur projects to start using it right away.
3. You can also double-click the **MKQwerty Demo.jzml** file to see a demo of how it works.

## Retrieving the Keyboard's Output

Retrieve the keyboard's output via its `getOutput()` script. 

If want to monitor the output in realtime, you can monitor this script for changes:
 
1. Create a new script on one of your controls.
2. Set the Execution Mode to "On Expression", and set the expression to `MKQwerty.getOutput()`. The script will be called whenever the output changes.

## Configuring the Keyboard's Settings

MKQwerty supports 2 modes, Alphanumeric and Numeric. 

You can can configure this by setting the `isAlphanumeric` property to 1 for Alphanumeric, and 0 for Numeric.

### Alphanumeric Mode

The keyboard will output strings. Use this when you need to work with text, for example when updating a label's content.

### Numeric Mode

The keyboard will output numbers. Use this when you need to work with raw numbers, for example when setting a MIDI value to send.

- Set `allowsNegativeNumbers` to 0 if you want to prevent the keyboard from representing negative numbers.
- Set `allowsFloatingPointNumbers` to 0 if you want only to work with integers.

## Addtional configuration Options

- `showsDismissKey`: shows or hides the dismiss key
- `showsReturnKey`: shows or hides the return key

The keyboard also has various properties for setting the keyboard's color. Enter the color in one of the following formats:

- {color} : a grayscale color. Use a value between 0 and 1 
- {alpha, red, green, blue}: a RGB color with alpha channel. Use values between 0 and 1.


## Setting the Keyboard's Output Externally

You can load a value into the keyboard via `setOutput(value)`, passing in the value to want to display. The keyboard will only accept the value if its current settings allows it. For example, if you try to pass a string but the keyboard has `isAlphanumeric` set to 0 (Numeric Mode), nothing will happen. 

## Monitoring Key Strokes

In addition to monitoring the keyboard's output via `getOutput()` you can also react to each individual key stroke in the same way via `getLastTypedKey()`. 

## Feedback and Support

We welcome your suggestions for improvements and reports of any bugs you encounter. Here's how you can get in touch:

### Suggest Improvements or Report Bugs

1. **Go to the Issues Tab**: Click on the "Issues" tab at the top of this page.
2. **New Issue**: Click the "New Issue" button.
3. **Provide Details**: Describe your suggestion or the problem you encountered. Please include as much detail as possible to help us understand and address your feedback.
