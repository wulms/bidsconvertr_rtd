# BIDScoin data tutorial

## The installation procedure: Getting example data and installation of R and RStudio

- Follow the [instructions](installation.md) to install the [BIDSconvertR](installation_bidsconvertr.md) on Windows or Linux and their dependencies.
- Download the [BIDScoin](https://github.com/Donders-Institute/bidscoin) example data : [Download here](https://surfdrive.surf.nl/files/index.php/s/HTxdUbykBZm2cYM/download). Please note, that the data is compressed twice with gunzip (suffix: '.gz') and tar (suffix: '.tar'). You need to unpack both.
- Create a new folder (e.g. `bidscoin\example`) and copy the `raw` subject folders into it. 

## The BIDSconvertR workflow:

- Start RStudio and use the R console from here on.
- Execute `library("bidsconvertr")`.
- Start the tool with the `convert_to_BIDS()`command.
- Create your own 'user\_settings.R' file by following the popup messages.
  - Select your input folder containing the DICOM's (e.g. 'bidscoin\_example\raw').
  - Select the `../subject/session/..` order of folders.
  - Select your output folder.
  - Skip the "subject-ID" and "pattern to remove" functionality. Your subject-ID's are fine!
- Rename your files with the sequence mapper according to BIDS, or download the `sequence_map.tsv` from here and replace the file in your output folder.

![BIDS viewer](../../../inst/figure/BIDScoin_Data_sequence_mapper.PNG)

- Now the data is automatically saved into BIDS, the BIDS validator is started and the 'Shiny BIDS viewer' starts.
