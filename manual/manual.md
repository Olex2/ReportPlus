#ReportPlus

**ReportPlus** is an extension module for Olex2. It provides extended report functionality, including the ability to create reports across a number of structures. Various output formats are supported:

- \LaTeX (for the generation of PDF files)
- RTF (for copy/paste into MS Word)
- HTML (for web content)

**ReportPlus** will eventually provide many tools that are required to prepare complete and professional reports from *.cif* files. These reports will be fully customisable.

The aim is to provide a one-button report function that will fully automatically prepare standard structure reports, either for internal archiving or to provide complete structural information for further inclusion in theses and publications.

##Installation
This module is available from the 'Extension Modules' tool in the Start tab of Olex2. You must provide your e-mail address and will be able to evaluate the module for 30 days. During the testing phase of any of our modules, you can update the module repeatedly. After the end of testing, please get in touch with us (support@olexsys.org) if you wish to continue using the module.

##GUI
Like the module itself, the GUI is currently under development. Please make sure to obtain the latest manual frequently.

![Screenshot of the GUI](/images/screenshot.png)

### Templates

If more than one template is available, you can choose the template you wish to use from the first drop-down box. A template refers to a folder of that name and the files contained within this folder will be used in the generation of the final report. If you want to modify the template, we suggest that you make a copy of the 'default' folder and modify this copy. Click on the 'Edit' link on the right to open the directory where the templates are stored. If you modify the contents of the original folder, your modifications will be lost after an update.

###Output Format

We currently support the _tex_ and _rtf_ output formats. HTML output will be supported in the near future.

#### TEX

You can use the tex output to compile the report into a PDF using a \LaTeX engine -- we recommend that you install the MikeTex system to do this, which is a straightforward process.
The report will compile into a PDF file for archival purposes -- it is not intended to be used as a source for further use. Of course, if you are originating text using \LaTeX, you can re-use any blocks of text that is generated in the .tex file.
	
### RTF

This produces a file using the rich text standard and can be opened in many word processors, including MS Word (all versions).

### Logo
You may wish to include a Logo at the top of your report. By default, this is set to the Olex2 logo -- but you may create your own logo folders and those will appear in the drop-down box automatically.

### Image
If you provide a file name here (all images present in the current structure folder are listed automatically in the drop-down box), then that image will be used.
If you leave this box empty, then ReportPlus will automatically create a screenshot of the current view from you. If you tick 'Grow Structure' and the structure will be grown first, and if you also select 'Best View' than the image will be aligned such that there is minimal overlap between atoms and bonds in the view.
For RTF files, the image will be embedded as binary data in your file. The binary data will be resized to match the resolution provided in the settings file (click 'Set' to change). For TEX files, a link to the image will be included. Currently, this is an absolute link, so your TEX document will compile from any location on your machine but not on another machine. The image included in the PDF will not be resized. So: if you include a high-resolution image here, the PDF can become rather large. _We value feedback on this aspect from our testers_.


###Tables
You can choose to include _all_ automatically produced tables of structural information (coordinates, bonds, angles etc) and in addition you can also show tables containing selected bond distances or angles. Sometimes you may want to only include the selected tables in the report.

###Crystal Images
These are the photographs of the crystal on the goniometer head. Obviously, these can only be included if these images are available. You MUST leave your manufacturer folder structure intact for this to work.

### Includes
There are various optional includes you may choose. _Diagnostics Plots_ and _Reflection Statistics_ obviously depend on the presence of HKL data in your folder.

### Paper Size
Various paper sizes will become available; currently we only support A4 and US Letter.


# References

ReportPlus will add publication references to your reports. We will interpret the information provided in the CIF file and create a meaningful reference. The reference information is stored in the standard BibTex format and can be edited by hand. However, it is advisable to make a copy of the provided citations.bib file, because updates will overwrite this file. You can set the citation source in the settings file (Click the Edit link). You may also edit the `citation normaliser' file in the same way. _Please help us making this bibliography file a valuable resource and let us have your additions so we can include them for everyone_.

In \LaTeX output, the citations will appear as fully formatted citations in the end of the file and the references in the text are denoted with square brackets.

![Citations in the \LaTeX output](/images/citations.png)
![References in the \LaTeX output](/images/references.png)

In RTF output, the short reference provided in the CIF (or possible the one generated by ReportPlus) will appear in the text and an alphabetic list of references will appear at the end of the report.


#Database

## Users
Olex2 has a database where information about authors is kept. If you set this information in `@Home|Report' then this will come through to your final report.

## Crystallisation and Crystal Mounting
ReportPlus modifies the `@Work|Report|Crystal` section in Olex2 so that the crystallisation method and crystal mounting options come from a database. You can either choose from the values already in the database, or type your own values. New values will be added to the database automatically.

![The modified `@Work|Report|Crystal` section](/images/modified_crystal_section.png)

