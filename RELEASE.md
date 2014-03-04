ADmarCCD Releases
==================

The latest untagged master branch can be obtained at
https://github.com/areaDetector/ADmarCCD.

Tagged source code and pre-built binary releases prior to R2-0 are included
in the areaDetector releases available via links at
http://cars.uchicago.edu/software/epics/areaDetector.html.

Tagged source code releases from R2-0 onward can be obtained at 
https://github.com/areaDetector/ADmarCCD/releases.

Tagged prebuilt binaries from R2-0 onward can be obtained at
http://cars.uchicago.edu/software/pub/ADmarCCD.

The versions of EPICS base, asyn, and other synApps modules used for each release can be obtained from 
the EXAMPLE_RELEASE_PATHS.local, EXAMPLE_RELEASE_LIBS.local, and EXAMPLE_RELEASE_PRODS.local
files respectively, in the appropriate release of the 
[top-level areaDetector](https://github.com/areaDetector/areaDetector) repository.


Release Notes
=============

R2-0
----
* Moved the repository to [Github](https://github.com/areaDetector/ADmarCCD).
* Re-organized the directory structure to separate the driver library from the example IOC application.
* Added support for the triggered acquisition modes available on the new high-speed (-HS series) 
  detectors from Rayonix.  
  This includes the following new records:
    - GateMode
    - ReadoutMode
    - ServerMode_RBV
    - ReadoutMode
    - SeriesFileTemplate
    - SeriesFileDigits
    - SeriesFileFirst
    - MarSeriesStatus_RBV


R1-9-1 and earlier
------------------
Release notes are part of the
[areaDetector Release Notes](http://cars.uchicago.edu/software/epics/areaDetectorReleaseNotes.html).
