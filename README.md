# What this does:
It is an XDF file, this is a file for an application called tuner pro, which lays out a patch to make your DME virginized (fresh from factory) as well as identify VIN locations within the hex. There is also included a Perl application that was sourced from the m3forums from user p0lar. This perl script converts your VIN number to BMW hex. This tool is needed for the process as described below.

Why would you want to "virginize" your DME? Well if you get a used DME from the junkyard for your 540/x5/740 it wont turn the car over due to the EWS security system. You would have to swap the EWS module the key ring module as well as the DME..... and then how would you ever get a replacement key from the stealership?
This system stores a special set of codes on your DME that changes on a rolling cycle. Once you "virginize" the DME. You can now align the EWS to the DME (basically the same thing BMW does when it sets the car up from the factory). This stores those rolling codes back onto your DME and syncs the cycle they rotate on to be in time with the EWS module.


## Pre Requisits:
- Tuner Pro must be installed and working
- You must understand how to load an XDF and open a Bin in tuner pro
- Galletto 1260 must be installed and working
- You must understand how to pull a dump in "boot" mode from your DME
- This is outlined TONS of places on the internet
- You must have pulled a 512kb dump of your DME in "boot" mode
- have Perl installed you can get it from here : https://www.perl.org/get.html


### Get started
1. Open up tuner pro and load the included XDF
2. then load your 512kb BIN you have already obtained before starting
3. Once loaded click the patch at the top and click apply patch then apply
4. open the 3 vin locations and the ones that show entries other than FF FF FF need to be over written with your VIN

I have included a tool written by p0lar from the m3 forums that will take your VIN number and convert it to hex

You would run this from your terminal using perl

windows:

`perl vintohex.pl --vin=PUTYOURVINNUMBERHERE`

linux/mac:

`chmod 755 vintohex.pl` <br>
`./vintohex.pl --vin=PUTYOURVINNUMBERHERE`


when it returns the hex copy it and paste it into the tuner pro boxes for your VIN
TADA! you have a virginized Me7.2 DME that you can now run an alignment on
