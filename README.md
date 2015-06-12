ILI9341_due
===========

Please see http://marekburiak.github.io/ILI9341_due


Version History:
```
v1.00.000 - Breaking changes:
                - functions renamed:
                    drawArc -> fillArc
                    selectFont -> setFont
                    defineArea -> setTextArea
                    setFontColor -> setTextColor
                    setCursor -> cursorToXY
                    setTextSize -> setTextScale
                    setFontLetterSpacing -> setTextLetterSpacing
                    getFontLetterSpacing -> getTextLetterSpacing
                    drawString -> print, printAt, printAligned
                    drawStringOffseted -> printAlignedOffseted
                    drawStringPivoted -> printAlignedPivoted
                    drawStringPivotedOffseted -> printAlignedPivotedOffseted
                - setTextArea (previously defineArea) is now set by x,y,width,height 
                  (previously x1,y1,x2,y2)
                - images in .565 format must be generated again with the current BMP24toILI565 tool
                  tool
          - New functions
                - setAngleOffset (extracted from setArcParams)
                - drawLineByAngle
                - printAtOffseted
                - clearArea
                - drawImage
                - setTextLineSpacing
          - New additions
                - added support for String and FlashStringHelper*
                - supporting '\n' in strings
                - much more predefined colors like ILI9341_CHOCOLATE or ILI9341_SKYBLUE
                - BMP24toILI9341Array - a tool to convert an image to an array
                  (so you can draw small images directly from memory, no need for SD card)
          - Other changes
                - many speed improvements
                - removed ILI9341_due_gText.h, ILI_SDSpi.h, ILI_SdFatConfig.h
                - added ILI9341_due_config.h
                - gText is now embedded directly in the ILI9341_due library so you do not
                  need to create ILI9341_due_gText objects anymore. Just call tft.print
                - updated github.io page, documented all functions (with examples and 
                  pictures!)

            
ILI9341_due_gText(&tft) -> gTextArea



v0.94.000 - Added AVR compatibility, the library can now be also used on Uno, Mega and alike.
			Please check the github.io page for more information (especially if you want to
			use gText)
v0.93.000 - Breaking changes:
                - setRotation now needs iliRotation enum as a parameter (instead of an int)
                - the meaning of some gText drawString parameters have changed 
                  (event though the parameter type is the same)
          - New additions:
                - gText drawString with new parameters
                - new gText drawStringOffseted, drawStringPivoted, drawStringPivotedOffseted 
                  functions
          - gText fontLetterSpacing default value is now 2 (previously 0)
          - examples updated

v0.92.002 - Fixed drawArc
		  - Added setArcParams function to change maxArcAngle and arcAngleOffset at runtime

v0.92.001 - Added fontHeight function in gText
          - fixes for NORMAL and EXTENDED mode

v0.92.000 - Added drawArc function for drawing arcs and circles with thickness and pies
          - Added screenshotToConsole method and ILIScreenShotViewer app for taking 
            screenshots from the display
          - Added alignment options for drawString in ILI9341_due_gText
	  
v0.91.002 - Updated graphicstestWithStats example sketch so it does not use Streaming.h

v0.91.001 - Performance improvements (especially fill circle)
          - Fixed a scanline fill bug, clean up commented out code

v0.91.000 - Added functions for controlling TFT power levels (sleep, idle, setPowerLevel)

v0.90.026 - Fixed fillScreen after recent changes

v0.90.025 - Added PushColors565 function
          - Added BMP24toILI565 tool
          - Updated sdFatTftBitmap example

v0.90.010 - Initial version
```