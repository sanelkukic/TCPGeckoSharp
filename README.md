# TCPGeckoSharp
.NET assembly that lets you access and use TCPGecko.

> I know that you can just use the 3 files from Gecko dNet and make your program more portable but this is easier for those who are too lazy to open each of the 3 files and edit 1-2 word(s).

> Also, credits to the creator of Gecko dNet for the original source.

## How to use
- Download from [here](https://github.com/ASHTeam/TCPGeckoSharp/releases/latest)
- Add the reference to your project
- Add `using TCPGeckoSharp;` to the list of assembly(s) used by your project
- Declare it by using `public TCPGecko gecko;` and `gecko = new TCPGecko("ip here", 7331);`
- Connect to the console using `gecko.Connect();` and disconnect using `gecko.Disconnect();`

## Compiling
- Get VS
- Download this source
- Open this in VS
- Go to Build tab
- Click Build Solution
