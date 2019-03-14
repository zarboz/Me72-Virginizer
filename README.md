# Pre Requisits:
- Tuner Pro must be installed and working
- You must understand how to load an XDF and open a Bin in tuner pro
- Galletto 1260 must be installed and working
- You must understand how to pull a dump in "boot" mode from your DME
- This is outlined TONS of places on the internet
- You must have pulled a 512kb dump of your DME in "boot" mode


## Get started
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
