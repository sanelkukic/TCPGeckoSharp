# TCPGeckoSharp
.NET assembly that lets you access and use TCPGecko.

> I know that you can just use the 3 files from Gecko dNet and make your program more portable but this is easier for those who are too lazy to open each of the 3 files and edit 1-2 word(s).

> Also, credits to the creator of Gecko dNet for the original source.

> This library is [now available on NuGet](https://www.nuget.org/packages/TCPGeckoSharp/)! Install it using the [Package Manager Console](https://docs.nuget.org/docs/start-here/using-the-package-manager-console):
```
PM> Install-Package TCPGeckoSharp
```

## How to use
- Download from [here](https://github.com/Hexexpeck/TCPGeckoSharp/releases/latest) or [from NuGet](https://www.nuget.org/packages/TCPGeckoSharp/)
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

## Example
```csharp
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.IO;
using System.Linq;
using System.Resources;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Net;
using System.Net.Sockets;
using System.Reflection;
using TCPGeckoSharp;

namespace YourAppHere
{
    public partial class MainForm : Form
    {
    public TCPGecko gecko;
    public MainForm()
    {
        InitializeComponent();
    }
    void connectButtonClick(object sender, EventArgs e)
    {
        try
        {
            gecko.Connect("ip here", 7331);
            // or you could do gecko.Connect(inputBox.Text, 7331);
        }
        catch (ETCPGeckoException)
        {
            MessageBox.Show("Could not find TCPGecko running on Wii U.");
        }
        catch (System.Net.Sockets.SocketException)
        {
            MessageBox.Show("Invalid IP.");
        }
    }
  }
}
```
or something like that, this was just an example for using a Windows Application instead of a commandline
