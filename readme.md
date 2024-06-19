## Rider is creating files with BOM markers when it shouldn't.

This repository is set up to demonstrate certain bugs in Jetbrains Rider. The .editorconfig indicates that UTF-8 should be used without a BOM marker. But typical operations will add a BOM marker.


## Adding a new file

### Steps to Reproduce

Right-click on the ClassLibrary folder and add a new class file. Name it Whatever.

### Actual Result

The file is created as UTF-8 but with a BOM marker.

### Expected Result

The file is created as UTF-8 WITHOUT a BOM marker.


## Creating a new file indirectly

### Steps to reproduce:

Open the existing "Foo" class in "Foo.cs". Select the word "Bar" which is there for a class named Bar. Do the refactoring to move it to its own file "Bar.cs"

### Actual Result

A file Bar.cs is created using UTF-8 with a BOM marker.

### Expected Result
A file Bar.cs is created using UTF-8 WITHOUT a BOM marker.
