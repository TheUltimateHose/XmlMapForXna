# XmlMapForXna

This is an Add-on for the XNA content pipeline which lets you import Xml-based maps into your C# Games.

##Usage

The Usage of this add-on is quite simple. If you have used custom pipeline tools before, you are probably familiar with the steps here:

- In the pipeline gui, click on the content root (usually "Content")
- in the menu below the tree, under settings, click on references and then on the ellipses button [...]
- You will see a window with a single text field. In there, enter the path to the "XmlMap.dll" relative to your "Content.mcgb" file (in my case  "..\XmlMap.dll")
- Now, when you add a xml map to your project, select "XML Map Importer" as Importer and "XML Map Processor" as Processor

Once you added the map to your content pipeline, you can use it in the code by adding the same dll to your c# project references and using this line of code:

    TileMap map = Content.Load<TileMap>("Map_Location/map_file");

##Notes

The Map format is my own, so it probably won't work with maps from other editors. My Editor can be found in the "Final" folder. But be aware: it's not totally finished and loading is totally broken. Apart from that, you will need a "Tileset.xml" in a "Content" subfolder containing presets for the Tiles. An example of how this is supposed to look can also be found in the "Final" folder.