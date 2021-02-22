# Working with XML Files

_By Blair Wang_
<br /><br />


## 1. What are XML files?

XMLstands for "eXtensible Markable Language" (I know, it's cheesy, it is what it is). You can recognise XML files with the file extension .xml. This is really just a plain text file (.txt) with a particular structure. This is a structure composed of "tags" each with "contents" and "attributes".

```xml
<tag attribute1="hello world" attribute2="bonjour monde">
	contents
</tag>
```

You will notice that this code snippet is marked as "HTML", the language of websites. This is because HTML is the most common usage of XML - to store the contents of a webpage.


## 2. Where are XML files used in Java?

XML files form the basis of FXML layouts. Even though these open in Scene Builder, their contents are actually text:

```xml
<VBox alignment="CENTER" spacing="20.0" xmlns="http://javafx.com/javafx/8.0.171" xmlns:fx="http://javafx.com/fxml/1" fx:controller="au.edu.unsw.business.infs2605.fxstarterkit.PrimaryController">
	<children>
		<Label text="Primary View" />
		<Button fx:id="primaryButton" text="Switch to Secondary View" onAction="#switchToSecondary"/>
	</children>
	<padding>
		<Insets bottom="20.0" left="20.0" right="20.0" top="20.0" />
	</padding>
</VBox>
```

This is actually a snippet from the file primary.xml in the infs2605fxstarterkit, which is machine-generated. Because it is machine-generated, it doesn't care about human readability, which is why you need to scroll horizontally to see the full line.

Technically, you can rewrite it to be a bit more readable, and it is still valid XML:

```xml
<VBox alignment="CENTER" spacing="20.0"
	xmlns="http://javafx.com/javafx/8.0.171"
	xmlns:fx="http://javafx.com/fxml/1"
	fx:controller="au.edu.unsw.business.infs2605.fxstarterkit.PrimaryController"
>
	<children>
		<Label text="Primary View" />
		<Button
			fx:id="primaryButton"
			text="Switch to Secondary View"
			onAction="#switchToSecondary"
		/>
	</children>
	<padding>
		<Insets bottom="20.0" left="20.0" right="20.0" top="20.0" />
	</padding>
</VBox>
```

Now you can easily see on line 4:

```
fx:controller="au.edu.unsw.business.infs2605.fxstarterkit.PrimaryController"
```

This specifies that the Controller for this View is the Java class called PrimaryController.