# ControlsStack
This is a stack to demonstrate the new controls available in Stacks 3.

### Button
Button is a new control type. It displays the content of a single boolean value.  Functionally it is identical to a checkbox. However in some cases it makes more sense to provide visual information rather than textual.

### Date
There is now a date type control.  The value entered is a date/time.

### Icons
Stacks 3 the Font Awesome icons throughout its interface.  They're used in the Stacks default toolbars and default controls and you can use them for your stacks too.  Font Awesome has hundreds of icons to choose from and is particularly well suited for web design.  Using a single icon-set throughout Stacks allows all stacks to feel like an integral part of Stacks rather than something separate.

To add icons to your controls you add the "icons" key.  This should be an Array of Numbers (integers).  The number entered should be the Font Awesome icon code-number.

Example: To add a link icon to your button you find the [chain-link](http://fortawesome.github.io/Font-Awesome/icon/link/) icon on the [Font Awesome site](http://fortawesome.github.io/Font-Awesome/).  That page shows that the Unicode for this icon is: f0c1.  You can enter that value as a hexidecimal in most editors as 0xF0C1 or in decimal if you prefer 61633.

At this time Icons are only supported for Button controls.

### Subtitles
Many controls now provide a way to add a small bit of descriptive text under the control itself.  This can help in showing a user the format of the value you expect, or in labeling groups of controls.

### Control Arrays
Some controls can now be ganged together into a small group. The controls are visually denser and more terse. This provides a way of displaying groups of related items, like 4 border widths, or left/center/right alignment. Control arrays are defined much like their single counterparts, but have a few key differences:

 * `title`: There is only one title for the entire group, so there is no change to this key.
 * `subtitles`: An array of strings. One for each control. Keep them short and pay attention to the available space.
 * `icons`: An array of Numbers (integers). One for each control. They should correspond to the icon code from Font Awesome.
 * `toolTip`: There is only one tooltip for the entire group. so there is no change to this key.
 * `type`: Grouped controls have the same type as their single counterparts, but with `-2`, `-3`, or `-4` appended.  For example: `checkbox-2`, `button-3`, or `color-4`.
 * `id`: There is only one id for the entire group. So there is no change in the way this key is defined. However how it is used is new. When using the id in a template, you must append the array index using standard array notation. For example: `%id=button_4_array[0]%, %id=button_4_array[1]%, %id=button_4_array[2]%, %id=button_4_array[3]%`
 * `radio`: For checkbox and buttons the items support a one-at-a-time (radio-button) mode. Setting `radio` to boolean YES enables this mode.

Supported Types:  `button`, `checkbox`, `color`, `number`, and `input`
Buttons support 1, 2, 3, and 4 across.
All other types support 1, 2, and 4 (not 3).

