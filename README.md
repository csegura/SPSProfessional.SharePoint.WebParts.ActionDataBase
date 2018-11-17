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

This section contains various fields that will be displayed in the editor as well as the controls in which they will be displayed and the verifications that are required for each of them.

The structure is as follows (sample):  

```
<Fields\>  
<Field Name\="Freight"  
Title\="Freight"  
Type\="Money"  
Control\="TextBox"  
Required\="true"  
DefaultValue\=""  
DisplayFormat\=""  
New\="Enabled"  
Edit\="Enabled"  
View\="Enabled"\>  
<TextBox Columns\="20" RightToLeft\="true" />  
<Validators\>  
<Validator Type\="Range"  
DataType\="decimal"  
MaxValue\="10000"  
MinValue\="0"  
ErrorMessage\="Number between 0 - 10000" />  
</Validators\>  
</Field\>  
...  
</Fields\> 
```


### Fields – Section for the fields that will conform the editor

Example

```<Fields\> <Field ... /> </Fields\>```

### Field – Element for each editor’s field

**Attributes:**  
**Name** -  (string) – Field’s name  
**Title** -  (string) - Title, description   
**Type** - (string)  -  (SQL Server) Data type  
**Control** - (string)  - control type to be used to edit (TextBox, Lookup, Date, DateTime, Memo, ListBox, DropDownList)  
**Required** - (boolean) true/false   - If is a required field(implicitly adds the required verification)  

![](images/Editor_RequiredFields.gif)  
Required fields  
**  
Default** - (string)  - field by default to register. There are a number of functions that can be used as default values see: **[Functions](http://www.spsprofessional.com/page/SPSRollUp-CAML-Functions.aspx)**  
**DisplayFormat** - (string)  - mask to view the field  See: Formats  

**New** - (string)  Enabled/Disabled/Hidden - - If the field will be active when it will register a new record  
**Edit**  - (string)  Enabled/Disabled/Hidden -  - If the field will be active when it will register a new record  
**View** - (string)  Enabled/Disabled/Hidden - - If the field will be made visual

Enabled - The field is and shows itself active  
Disabled - The field shows itself but it is not enabled  
Hidden - The field doesn’t show itself  

Example; See above  

Edit controls  


### TextBox - Defines a TextBox control

**Attributes:  
Columns** -  (integer) - columns number wide  
**MaxLenght** -  (integer) -  Characters maximum number  
**RightToLeft** - (boolean)  -If you write from right to left


![](images/Editor_TextLeft.gif)  
Example RightToLeft="true"  

Example:

```<TextBox Columns\="40" MaxLenght\="60" RightToLeft\="false" />```


![](images/Editor_TextField.gif)  
Example: TextBox  


### Memo – Defines a Memo  control Memo with an enrich text editor



**Attributes:  
Columns** -  (integer) - columns number wide  
**Rows** -  (integer) - rows number  
**MaxLenght** -  (integer) - characters Maximum number  

Example:

```<Memo Columns\="40" Rows\="10" MaxLenght\="300" />```    

![](images/Editor_MemoField.gif)  
Example: Memo  


### Date y DateTime – Definition is not available

Nothing to configure here. If you select this control all parameters necessaries

![](images/Editor_DateFields.gif)

### Lookup – Defines a Memo control with a enrich text editor



**Attributes:  
TextField** -  (string) -  characters Maximum number  
**ValueField** -  (string) - Field that contains the values  
**Table** - (string) – Database field  
**DisplayFormat** - (string) - Format to view text field - See: Formats  

Example:

```<Lookup TextField\="CompanyName" ValueField\="ShipperID" Table\="Shippers" />``` 

![](images/Editor_LookupField.gif)  
Example: Lookup  


### ListItems - Define a ListBox or DropDownList control

Inside list items section you can add items. Items are Text, Value pairs. You can use it with the ListBox or DropDownList controls.

**Attributes:  
Text** -  (string) -  Text to display  
**Value** -  (string) - Value to store in the field  
**Selected** - (boolean) – If is the default selected value  

Example:

```<ListItems Multiple\="false"\> <Item Text\="00001-AAAA" Value\="00001" /> <Item Text\="00002-BBBBB" Value\="00002" /> <Item Text\="00003-CCCCC" Value\="00003" Selected\="true" /> </ListItems\>``` 



![](images/Editor_DropDownListControl.gif)  
Example: ListItems as DropDownList Control  


![](images/Editor_ListBoxControl.gif)  
Example: ListItems as ListBox Control

### DataBase – Connection


**Attributes:  
ConnectionString** - (string) -  Contains the connection chain to the SQL Server  

Example

``` <DataBase ConnectionString\="Data Source=W2K3;Initial Catalog=Northwind;  
Integrated Security=True;User ID=;Password=" \>  
<Table ....\>  
<IdentityColumn .... />  
</Table\> 
</DataBase\>
```  

Contains element: Table


### Table – Element for the configuration of the table that we are going to edit

**Attributes:**  
**Name** - (string) - table’s name that we are going to edit in the database  

Example

```<Table Name\="dbo.Customers"\>  <IdentityColumn Name\="CustomerID" Type\="NChar" /> </Table\>``` 

Contains element: IdentityColumn  

### IdentityColumn – Element for the keys to the table

We will identify each one of the columns through which we will recover a unique table register (usually the columns table entity)  

**Attributes:  
****Name** - (string) -  Column name  
**Type** - (string) – Data type (SQL Server)  
**Incremental** - (boolean) - If it is a field with auto-increase  

Example:

```<Table Name\="dbo.Customers"\> <IdentityColumn Name\="CustomerID" Type\="NChar" Incremental\="false" /> </Table\> ```


### Validations 

At the moment there are 3 types of verifications or validations:

*   by comparison (Compare)
*   by regular expressions (RegExp)
*   by ranges (Range)

We can add more than one verifier to each field so that we can combine these. We will not be able to add two compare verifiers.

### Verifier Compare

Compare a user entry with a constant value or a proprietary value from another control (not yet implemented) through a comparison operator (less than equal to,  more than, among).

The verifier by comparison requires that the attributes are completed:  

![](images/Editor_ValidatorCompare.gif)

\- **Message** - Text with the error message  
\- **DataType** - data type to be used to verify: Currency, Double, Integer, String, Date.  
\- **Value** - value to be compared to  
\- **Operator** - operation type

The possible operators are:  

\- **DataTypeCheck** - it will check if the entered  data is from the type that was specified in DataType  
\- **Equal** - Compares if the entered value is equal to the value declared in Value  
\- **GreaterThan** - Compares if the entered value  is greater than the value declared in Value   
\- **GreaterThanEqual** - Compares  if the  entered value is greater than or equal to the value declared in Value  
\- **LessThan**  - Compares  if the entered value is less than the value declared in Value  
\- **LessThanEqual**  - Compares  if the entered value is less or equal than the value declared in Value  
\- **NotEqual** - Compares if the entered value is not equal to  the value declared in Value

The result in XML configuration will be something like this.  

```
<Validators\> <Validator Type\="Compare"   
DataType\="Integer" 

ErrorMessage\="Must be greater than 100" 

Operation\="GreaterThan" 

Value\="100" /> </Validators\> 
```



### Verifier- RegExp



Verify that the entry matches a pattern defined by a regular expression. Such verification allows to check predictable character sequences, like social security numbers, email addresses, phone numbers and post codes, among others.

![](images/Editor_ValidatorRegExp.gif)

The verifier RegExp requires the completion of the following attributes:  

\- **Message** - Text with the error message  
\- **Expression** - Regular expression to be used to verify

The result in the XML configuration will be something like this.  

```
<Validators\> <Validator Type\="RegEx"   
DataType\="None"   
ErrorMessage\="Must be a valid email"   
Expression\=[.\*@.\*\\.\*](mailto:.*@.*\.*)   
Operation\="None" /> </Validators\> 
```

![](images/Editor_ValidatorRegExp1.gif)  


### Verifier - Range



Verify that a user entry is between the specified upper and lower limits. You can check the intervals between pairs of numbers, dates or alphabetic characters. The limits can be expressed as a constant.

![](images/Editor_ValidatorRange.gif)

The verifier by comparison requires the completion of the attributes:

\- **Message** - Text with the error message  
\- **DataType** - Data type to be used to verifier:  Currency, Double, Integer, String, Date.  
\- **MaxValue** - Maximum Value  
\- **MinValue** – Minimum Value  

The result in the XML configuration will be something like this.  

```
<Validators\> <Validator Type\="Range"   
DataType\="Integer"   
ErrorMessage\="Must be in range 10-40"   
Operation\="None"   
MaxValue\="40"   
MinValue\="10" /> </Validators\>
´´´
