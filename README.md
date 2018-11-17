# SPSProfessional.SharePoint.WebParts.ActionDataBase
**ActionDatabase WebParts** is a set of webparts to connect quickly and effortlessly with your Back-End DataBase, as alternative to Business Data Catalog.

Click to show video

[![Show Video](https://img.youtube.com/vi/3sn8vO3GhNA/0.jpg)](https://www.youtube.com/watch?v=3sn8vO3GhNA)


ActionGrid
----------

The **ActionGrid** WebPart displays data from a DataBase: with a simple "select command", the configuration of columns, headers and formats as presented on screen

![](images/ADGrid1.gif)

The **ActionGrid** also connects with other WebParts to create Master-Detail grids or connect with a form WebPart to filter data

![](images/ADGrid2.gif)

ActionDataBaseEditor
--------------------

Connect the **ActionGrid** WebPart with the **ActionEditor** WebPart and take full control to create, edit, update and delete data

![](images/ADEditor1.gif)

Full editing control

*   Fully customizable Tool Bar
*   Lookup fields, DropDownList and AJAX Picker Dialog
*   Date and DateTime fields controls
*   Fields validations (Required, Range, Regular Expression, Comparison)
*   Rich Text format fields
*   MOSS and WSS support !!!

Video

[![Edit video](https://img.youtube.com/vi/GO7oKl4hx4s/0.jpg)](https://www.youtube.com/watch?v=GO7oKl4hx4s)


*ActionDataBaseGrid**

![](images/Generator_GenerateGridButton.gif)

\- Click on the "Generate Grid" icon, the file configuration of the grid will be generated and you will be guided to the "XML Grid" results tab

![](images/Generator_GridXMLTab.gif)

\- If you wish you can edit this part directly in the XML configuration file or if you prefer you can use the advanced editor on the "XML Grid Editor" tab

\- You can use the "Validate XML" icon to validate the XML configuration file if you have chosen to modify it by hand, in this case, if there are any errors these errors will be displayed on the"Errors" tab.

\- There is an icon "Copy" to copy the configuration file content to the clipboard.

\- We will use this icon.

\- We will go to SharePoint and we will create a new webparts page.

\- We will Add the el webpart **_ActionDataBaseGrid_**

![](images/WebParts_ActionDataBaseGrid.gif)

\-Once the web part is added to our site we have to configure it.

![](images/WebParts_ActionDataBaseGrid1.gif)

\- For which we can use the link **"Check webpart properties in tool panel"**

\- showing the properties panel

![](images/WebParts_ActionDataBaseGridProperties.gif)

\- Click the icon to the right of the configuration box to paste the XML contents that we have previously generated with the generator.

![](images/WebParts_XMLConfiguration.gif)

\- Once the XML configuration is pasted, press Ok and then accept the changes.

\- We will have our first **ActionDataBaseGrid** running.

![](images/ActionDataBaseGrid_First.gif)

Next we will configure an **ActionDataBaseEditor** to edit data from the"Customers" table.

\- Returning to the generator from the "Command" tab

![](images/Generator_SelectCommand.gif)

\- Click on "Generate Form" icon

![](images/Generator_GenerateFormButton.gif)

\- The **ActionDataBase Generator** will generate the necessary and basic XML configuration file to edit the table that we are using, in this case "Customers". You can modify the XML configuration file using the 'Form XML "tab or using the "XML Form Editor " advanced editor.

![](images/Generator_FormXMLTab.gif)

\- If you decide to use the advanced editor you need to remember that after publishing you should click the "Generate XML" icon to update the XML configuration.

![](images/Generator_ValidateXMLButton.gif)

\-Once we have the code we only have to paste it into the **_ActionDataBaseEditor_** configuration like we did with the **_ActionDataBaseGrid_**

![](images/WebParts_ActionDataBaseEditor.gif)

\- By default the **ActionDataBaseEditor** will not display any data it will only show a blank form.

![](images/ActionDataBaseEditor_First.gif)

\- This is a normal behavior, as to be able to show a record, the **_ActionDataBaseEditor_** must be connected to another webpart to obtain identifying data from the register that you want to view or edit.
