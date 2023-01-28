
## Ian Stocker Sound Data Format
The Ian Stocker sound data format (SOUNDDATA.ROM) is a highly packaged format, used in games such as Sims 2 and Urbz on the DS.

This document aims to outline, in some form, how the format is stored.
### Header
The file header takes up at least what appears to be the first chunk. It contains a series of pointers, which then leads to another series of pointers (probably samples, in a signed format (XX0000000 X being the last bytes)).

### Sample Data
Sample data appears to be 16-Bit PCM mixed with 8-Bit PCM, and is all held within one largescale chunk, broken up by a series of noise (potential instrument bank). Assuming it somewhat follows ITI (Impulse Tracker Instrument) or S3M PCM sample format (unlikely, considering some samples are 16 Bit PCM), then following [the ITTECH.txt documentation](https://github.com/schismtracker/schismtracker/wiki/ITTECH.TXT), we can concur that it is likely a single bit decides whether the sample is 8-Bit or 16-Bit, and whether it loops.
