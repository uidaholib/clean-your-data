---
layout: default
title: 3-Start
nav: true
---

# Setup Refine
    
1. **Install Java:** OpenRefine is a [Java](http://java.com/en/){:target="_blank"} application and requires Java JRE to run. Download and install Java if you do not have it (you can check by typing `java -version` into a terminal). You want a 64-bit version, which is usually the default install. It is also a good idea to uninstall any old Java versions on your machine.
    - *Windows and Mac:* Clicking "Free Java Download" on the [Java](http://java.com/){:target="_blank"} site will get you the correct installer. (When installing be sure to uncheck the "recommended" option to add any bundled spamware to your system!)
    - *Linux:* Install from your distro's repositories, for example `sudo apt install default-jre` on Ubuntu/Debian (this is usually OpenJDK rather than Oracle's version).
2. **Download Refine:** Download the most recent [OpenRefine package](http://openrefine.org/download.html){:target="_blank"} for your OS. Releases are posted on the [OpenRefine site](http://openrefine.org/download.html){:target="_blank"} or [GitHub releases page](https://github.com/OpenRefine/OpenRefine/releases/){:target="_blank"}. (this workshop used OpenRefine V3.1) 
3. **Extract Refine:** Unzip the OpenRefine package to a permanent location, for example in your User directory, Home, or Documents. 
    - *Windows:* unzip by right clicking and selecting Extract All. 
    - *Mac:* drag the `dmg` to the application folder (Mac has known [issues](https://github.com/OpenRefine/OpenRefine/wiki/Installation-Instructions#mac-osx){:target="_blank"}, try these [solutions](https://evanwill.github.io/_drafts/notes/open-refine-osx.html){:target="_blank"}). 
    - *Linux:* unpack in desired location with with `tar`, for example `tar xzf openrefine-linux-3.1.tar.gz`. 

Full documentation is available on the [official wiki](https://github.com/OpenRefine/OpenRefine/wiki/){:target="_blank"}.

# Use Refine

1. **Start the Java app:** Opening Refine differs depending on your OS, but in all cases the app will start running in a terminal window which you can ignore and minimize (but do not close!).
    - *Windows:* double click `openrefine.exe` (You may get a warning that the publisher could not be verified, ignore it, and click *Run*. Once open, pin the Refine icon to your taskbar for easy access in the future). 
    - *Mac:* click the Refine icon in the applications folder. 
    - *Linux:* in the OpenRefine directory open terminal and type `./refine`.
2. **Use the GUI:** Once Refine is running in a terminal, your default web browser should automatically open with the interface. If it does not open automatically or you close the browser tab, find the GUI by typing <http://127.0.0.1:3333> or `localhost:3333` in your address bar. 
3. **Shut down:** close any browser tabs with the GUI, then stop the host terminal window with `Ctrl+C` (or `Command-Q` on Mac). This will ensure any open projects are saved.

> The user interface is rendered by your web browser, but Refine is not a web application. 
> Although it uses the term "upload" and "download", no information is sent online and no internet connection is necessary.
> For best results, use Firefox, Chrome, or Chromium browser.

Thus, Refine has two parts, the terminal window hosting the Java and the browser tab hosting the GUI:

![OpenRefine terminal and GUI](images/openrefine.png)
