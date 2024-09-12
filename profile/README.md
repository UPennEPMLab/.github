# UPennEPMLab

This is a space is a collection of shared code for the EPM Lab at UPenn.

The code that can be posted here must not be considered either a governmental or commercial secret.  In other words, no code should make direct use of a PDK or directly cite the objectives of a grant.

However, often projects can be thought of as subprojects.  For instance:
* Rather than mixing the code to interface with hardware with the actual collection, processing, and visualization, potentially the hardware interface code can be separated and called as a library. 
* Code for generating a delay line can be separated from the grant-driven project and called as a library.

In the short term, creating and maintaining divisions in code can cost time and energy.  However, as a lab, the reuse of code saves time.  This is particularly true if the code is well tested and maintained.

The actual use of the code, which most likely involves either PDKs or specific grant-objectives, most likely belongs in your personal notebook on the lab wiki.  In contrast to GitHub, the wiki is protected by being on a local computer, requiring both a password and TFA to access.

Below are the highlighted repositories:

Photonic Layout:
* [RiverPoint](https://github.com/UPennEPMLab/RiverPoint) - A waveguide routing engine based on Python's PHIDL project. It makes creating arrays of waveguides easier.
* [WGInstructionSet](https://github.com/UPennEPMLab/WGInstructionSet) - A Python waveguide routing engine based on PHIDL that makes use of data from [WGInterrogator](https://github.com/UPennEPMLab/WGInterrogator).  By considering a waveguide as a combination elements (straights, bends, transitions) the properties of the waveguide such as loss, group delay, dispersion, can be quickly calculated.  Once confident, the waveguide can be committed to GDS.

Simulation:
* [CustomInterconnect](https://github.com/UPennEPMLab/CustomInterconnect) - This project extends the Lumerical Interconnect Python API to make it more convenient to make simulations.
* [WGInterrogator](https://github.com/UPennEPMLab/WGInterrogator) - Python code for generating a "datasheet" of a WG profile for design and simulation using Lumerical's FDE Solver.
* [GDS_to_COMSOL](https://github.com/UPennEPMLab/GDS_to_COMSOL) - Code for importing GDS files into COMSOL and making basic selections.

Measurement:
* [HWPythonInterfaces](https://github.com/UPennEPMLab/HWPythonInterfaces) - A collection of importable files which provide a high-level interface to commonly used lab instrumentation such as power supplies and oscilloscopes.  The goal is to achieve the most common tasks without reading the programmer's manual to learn the SCPI commands.  This makes heave use of pyVISA.
* [Analytical-Devices](https://github.com/UPennEPMLab/Analytical-Devices) - A collection of analytical devices in Python with fitting routines.  An example of such a device is a heater based MZI attenuator.  Usually with a handful of measurements, when properly fitted, one can fully characterize a device.  The model can be used to accurately interpolate the behavior to set the experimental device to a desired state. 
