---

layout: post

title:  JavaScript Source Maps for Syncfusion Essential JS Widgets

description: How to use source maps in EJ controls to debug the script files 

platform: js

control:Introduction

documentation: ug

---

# Source Maps

Source maps provides the way to debug the minified files in the production environment. The source map files holds the information about the original files along with the mapped variable names. So these information are used to convert back to the original files, these will be accomplished by the browser itself.

## Source map for EJ sources

Now-a-days Essential JavaScript sources comes with the map files, which you can find from the same installed location:

`(Installed location)\Syncfusion\Essential Studio\14.1.0.41\JavaScript\assets\scripts\`

From the above location you can see, each minified file having its own source map files. 

N>  when you are going to use the map files, you need to include the below comment in the bottom of your minified file so that the minified file will refer the corresponding map file.

`//# sourceMappingURL = ej.filename.min.map `

N> It is advised to keep the original files along with the map files, so that the virtually converted code will map with the original file. However this doesn’t affects the bandwidth and performance during the production.

