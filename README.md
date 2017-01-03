# Mint Monitor Settings
Getting setting specific monitor refresh rates. For example getting a 144hz monitor to work correctly for gaming.

# Understanding how monitor displays are handled
When using using cinnamon's display manager you are actually modifying a file located at:

~/.config/monitors.xml

This a XML file that can contain multiple configuration setups. 
For example, if this is a laptop and you use an external display and this settings file would remember your last used monitor resolutions and orientation. 

In the settings file you are going to need to find the monitors refresh rate you want to modify. In most cases the best way to accomplish this Is to find the monitor you want to modify using the  \<vendor>\</vendor> Element.

Once you find the monitor you want to modify, below the \<vendor>\</vendor> you will need to find the \<rate>\</rate> element.
in most cases this would be set to 59 or 60 but if your monitor supports 144hz change this value to 144.

It would be recommended to change this value for the specific monitor in all instances if your file has multiple \<configuration> elements.

Now next time your display manger startup cinnamon it will auto remeber your refresh rate. 
