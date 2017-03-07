# TCPGeckoSharp
.NET assembly that lets you access and use TCPGecko.

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
