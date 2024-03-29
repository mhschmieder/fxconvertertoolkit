# FxConverterToolkit
FxConverterToolkit is a toolkit for converting JavaFX based graphics and GUI elements to various vector graphics output formats such as EPS, SVG and PDF, via intermediary transcoding to AWT using the excellent JFXConverter library by Hervé Girod, which allows one to connect legacy AWT-based Java libraries to JavaFX application elements.

ALERT: Please note that there seem to have been some recent changes to the artifact labeling of several of the legacy Java 8 versions of JFreeOrg's libraries, but I won't have time to update my POM's and/or API calls in this library for at least a few days (as of early October 20201, when I discovered the new discrepancy).

Although the JFXConverter library has its own drivers and extensions for the supported file formats, I needed to switch to better libraries for each vector graphics target and to have this code all available in a coordinated release with my other libraries. It is possible that this library may go away later on if Hervé likewise switches his source libraries for EPS and SVG (the latter currently uses Batik, which is very old and hard to maintain integration compatibility) and adds PDF support (this is my most important output format overall, and is meant to eventually supplant the need for EPS).

Eclipse and NetBeans related support files are included as they are generic and are agnostic to the OS or to the user's system details and file system structure, so it seems helpful to post them in order to accelerate the integration of this library into a user's normal IDE project workflow and build cycle.

The Javadocs are 100% compliant and complete, but I am still learning how to publish those at the hosting site that I think is part of Maven Central, as it is a bad idea to bloat a GitHub project with such files and to complicate repository changes (just as with binary files and archices). Hopefully later tonight!

This projects depends on my GraphicsToolkit and EpsToolkit libraries, as well as depending on Object Refinery's JFreeSVG and JFreePDF libraries, along with the JFXConverter library, and is marked as such in the Maven POM file.

Please note that for now my forks must be used for both external dependencies, as I had to modify the POM in order to specify Java 1.8 vs. Java 11.

This is a placeholder note: this library does not build yet, due to JFXConverter not being found. It is not yet a GitHub project or available as an artifact at Maven Central, so I think I will migrate it to Maven myself and bump its rev to 0.24 to avoid confusion. It has a run-time dependency though as well, and that one isn't open source, so it's another learningt curve for me, to see how to package pre-built resources that aren't yet using the GitHub + Maven paradigm.
