# Aditya
Program Sent for the programming round by Mutunus

System Requirement Specification

1)Eclipse IdE
Version: Mars release(4.5.0)
2) JDK 1.8
3) Itextpdf- 5.5.8
4) Windows 7 X86.

Steps to run the application
 1) Open the project in Eclipse IDE.
 2)Imprt itext pdf- 5.5.8
	a) right "click on project".
	b) choose "build path".
	c) choose "Add external archives".
	d) Select itextpdf-5.5.8 from the folder.
 3) Click run. Feed the desired inputs.
 4) Check the output in project(Multunus) folder.


---------------------------------------------------------------------------------------------------------------------
				||Working--  ||
----------------------------------------------------------------------------------------------------------------------

This application take the input in console and convert it into plain text or pdf.
Even external plugin can be also used to convert the console input in other format like ".doc" or "html".
When you run the application in console it will sk for the desired input. After feeding input, it will show 3 options
1.PlainText Conversion.
2.PDF Conversion.
3.Transform using Plugin.

If 1 is opted, whole details will convert into Movie_name.txt, if 2 is opted , whole details will convert into Movie_name.pdf
and if 3 is opted, it will ask for the plugin name.Plugin name is the name which is kept in "adi.Multunus.Plugin" in.java format.
After entering the name of plugin(only write plugin and exclude .java ), it will convert the details into another format for which plugin is written.


An interface "Multunus" is created with a public method "Moie_Detail()" in package "adi.Multunus.intfc".
For plain text, PlainText.java is used. PlainText.Java implements Multunus and override Movie_Details().
Similrly PDFConv.java is used for pdf conversion.







1


For plain text
---------------

FileWriter,BufferedWriter and PrintWriter class is used.


Using FileWriter class object, we create an output stream using the default encoding scheme.
BufferedWriter object creates a buffer for the stream created with fileWriter.
PrintWriter object is responsible for writting on the text file linke with the object of FileWriter.
-------------------------------------------------------------------------------------------------------------------------

2

For PDF
--------------------------------------------------------------------------------------------------------------------------


Itext API is used. It is an open source API. It supports the generation of pdf, html, rtf and xml documents.
Using Document class document object is created and using newParagraph() method details were added in pdf document.
-------------------------------------------------------------------------------------------------------------------------
3
 Creating and running Plugins
--------------------------------------------------------------------------------------------------------------------------
For creating plugins reflection is used. The Class.forNmae() metod is used. It returns the class object associated with the class
with the given name. The fornmae method causes the class with the name to be initialized.
Method class is used to create method object. Using getClass.getMethod("Movie_Details", new Class<?>[0]), Movie_Details method 
is searched is the dynamically loaded classes usin reflection.
method.invoke(dynamicObject) is used to invoke Movie_Details with dynamically created object.
 To use your plugin, write a java file which implements Multunus. After writtig java file, place it in package "adi.Multunus.plugin".
Restart the application, insert the details of movies as asked, insert 3 in console to run plugin, insert the plugin name
and check the output in project folder. 
