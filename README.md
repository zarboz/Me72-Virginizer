Load your 512kb file into tuner pro and open up the xdf that is included
run the patch function

open the 3 vin locations and the ones that show entries other than FF FF FF need to be over written with your VIN

I have included a tool written by p0lar from the m3 forums that will take your VIN number and convert it to hex

You would run this from your terminal using perl

windows:
perl vintohex.pl --vin=PUTYOURVINNUMBERHERE

when it returns the hex copy it and paste it into the tuner pro boxes for your VIN
TADA! you have a virginized Me7.2 DME that you can now run an alignment on