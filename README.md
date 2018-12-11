SET Toolkit V0.4.0
Copyright © 2014, Ryan Porter
All rights reserved.

Author:	 Ryan Porter
LAVA Name: Porter
Contact Info:	Contact via PM on lavag.org

LabVIEW Versions:
-----------------
- LV 2013 (Windows)

Dependencies:
------------
- Unicode support enabled in the LabVIEW.ini file

Description:
------------
The SET Toolkit has been developed to provide more convenient edit-time language switching support for LabVIEW projects.

UI strings are extracted from an existing project and stored in a localization file. Additional languages can be added then applied to the source code of the project using the apply language wizard.

The idea is to be able to quickly apply a language to a project before compiling to executable. Applying the language at edit-time allows you to fix up the UI in the target language. Change fonts and resize controls so that it looks right before compiling it.

- No modification of project's source code required. No additional dependencies.
- Support for switching code pages.
- Ability to definition shared resources.
- Resources referenced via UID. Changing labels of control does not break linkage.
- Resources can be exported to CSV file for external translation.
- Resources stored as UTF-16LE text.
- Ability to translate RTM files.

Installation:
------------------------------
- Install using VI Package Manager
- Enable Unicode support by adding "UseUnicode=True" to the LabVIEW.ini file.

Usage:
------
- From within any LabVIEW window, select "Tools->LAVA->SET Project Editor"

Known Issues:
-------------
- Excel doesn't properly import multi-line CSV records when the character encoding is UTF-16LE. Suggest using OpenOffice or LibreOffice instead.

Acknowledgments:
-----------------
- LabVIEW Unicode Programming Tools by Christian_L (https://decibel.ni.com/content/docs/DOC-10153): Modified version of some of the tools posted there have been included “Unicode Tools.lvlib”
- Passa Mak by ShaunR (http://lavag.org/files/file/98-passa-mak/): Provided inspiration for some of the VI string export and import functions.

Version History:
----------------
- v0.3: Alpha Release.
- v0.3.1: Added Tip Strip support and removed label checking.
- v0.3.2: Removed timer from RTM preview window to prevent labview from crashing when the window closes and the menu is open.
          Moved Launcher.vi to root directory & runs on open.
          Added "X" in front of all resource IDs to prevent excel from interpreting as number.
- v0.3.3: Fixed support for front panel static text.
          Added User Manual PDF to Documentation folder.
- v0.3.4: Modified CSV file format to work better with Excel CSV import.
- v0.3.5: Added support for labeled block diagram string array constants.
          Added support for WaveformChart, IntensityChart, IntensityGraph, MixedSignalGraph, WaveformGraph, DigitalGraph, XYGraph.
          Merged RemoveItem, RemoveGObject, RemoveFile messages into one RemoveObject message for Controller actor.
- v0.3.6: Added support for Tab Control page captions.
          Re-worked "tool_Unicode_Convert ASCII to Unicode.vi" and "tool_Unicode_Convert Unicode to ASCII.vi". Verified with Korean and Vietnamese text.
          Improved project editor launcher "SET Project Editor.vi".
          Removed OpenG dependencies.
- v0.3.7: Compiled to VI package.
          Added check for "UseUnicode=True" in "labview.ini"
- v0.3.8: Fixed bug in Unicode to ANSI conversion
          Fixed bug in tool_Unicode_Resize String Control.vi
- v0.3.9.1: Moved language list to "<VI Lib>\addons\_LAVA\SET_Toolkit\SET Project Data\LanguageList.csv"
- v0.3.9.2: Fixed runtime menus on VI selectors of project wizards
- v0.4.0: Added support for Array Control (1D) of type String and Array Constant of type String.

License:
--------
Distributed under the BSD 2-Clause (http://opensource.org/licenses/BSD-2-Clause)
See link for a full description of the license.

Support:
--------
If you have any problems with this code or want to suggest features:
Contact Porter via PM on lavag.org


