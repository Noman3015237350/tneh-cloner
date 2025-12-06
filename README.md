TNEH UID Cloner Tool

https://img.shields.io/badge/TNEH-CLONER-red
https://img.shields.io/badge/Python-3.7+-blue
https://img.shields.io/badge/License-MIT-green
https://img.shields.io/badge/Status-Active-brightgreen

A powerful UID cloning tool for Facebook accounts with old UID series support (2005-2014).

📋 Features

· Multiple Year Methods: Supports UIDs from 2005 to 2014
· Admin Authentication: Secure access with admin key protection
· High Performance: Multi-threaded processing (50 threads)
· Old UID Series Support:
  · 2005-2006 Method
  · 2007 Method
  · 2008 Method
  · 2009 Method
  · 2010 Method
  · 2011-2012 Method
· User-Agent Rotation: Random user agents for each request
· Result Saving: Automatically saves OK and CP results to files

🚀 Installation

Prerequisites

· Python 3.7 or higher
· Linux/Termux (Android) or Windows
· Internet connection

Termux Installation (Android)

```bash
# Update packages
pkg update && pkg upgrade

# Install Python and dependencies
pkg install python -y
pkg install python-pip -y
pkg install libcurl -y
pkg install openssl -y

# Install required modules
pip install requests beautifulsoup4 rich httpx
```

Linux/Windows Installation

```bash
# Clone or download the tool
git clone https://github.com/yourusername/tneh-cloner.git
cd tneh-cloner

# Install requirements
pip install -r requirements.txt

# Alternative: Install individual packages
pip install requests bs4 rich httpx pycurl
```

Install with PyCurl (if needed)

```bash
# For Termux
LDFLAGS="-L${PREFIX}/lib" CFLAGS="-I${PREFIX}/include" pip install pycurl

# For Linux
sudo apt-get install libcurl4-openssl-dev libssl-dev
pip install pycurl
```

📁 Project Structure

```
tneh-cloner/
├── tneh_cloner.py          # Main tool file
├── requirements.txt        # Python dependencies
├── README.md              # This documentation
├── TNEH-OK.txt           # Successful accounts (generated)
├── TNEH-CP.txt           # Checkpoint accounts (generated)
└── logs/                 # Logs directory (optional)
```

🎯 Usage

Starting the Tool

```bash
python tneh_cloner.py
```

Admin Authentication

When you first run the tool, you'll be prompted for the admin key:

```
╔══════════════════════════════════════════════════════════╗
║               ADMIN AUTHENTICATION REQUIRED              ║
╚══════════════════════════════════════════════════════════╝
[?] Enter Admin Key: 
```

Enter the admin key: 665577

Main Menu

After authentication, you'll see the main menu:

```
╔══════════════════════════════════════════════════════════╗
║                    ████████╗███╗   ██╗███████╗██╗  ██╗   ║
║                    ╚══██╔══╝████╗  ██║██╔════╝██║  ██║   ║
║                       ██║   ██╔██╗ ██║█████╗  ███████║   ║
║                       ██║   ██║╚██╗██║██╔══╝  ██╔══██║   ║
║                       ██║   ██║ ╚████║███████╗██║  ██║   ║
║                       ╚═╝   ╚═╝  ╚═══╝╚══════╝╚═╝  ╚═╝   ║
║                     TNEH - UID CLONER                    ║
╚══════════════════════════════════════════════════════════╝
[✓] DEVELOPER  : NOMAN
[✓] VERSION    : TNEH OLD CRACK
[✓] STATUS     : ACTIVE
[✓] TEAM       : TNEH CREW
══════════════════════════════════════════════════════════
[1] • 2011-2012 METHOD
[2] • 2010 METHOD
[3] • 2009 METHOD
[4] • 2008 METHOD
[5] • 2007 METHOD
[6] • 2005-2006 METHOD
[0] • EXIT
══════════════════════════════════════════════════════════
[?] SELECT OPTION :
```

Selecting UID Series

Choose the appropriate year method based on the UID series you want to crack:

· Option 1: 2011-2012 Method (100009XXXXX)
· Option 2: 2010 Method (100001XXXXX)
· Option 3: 2009 Method (100000XXXXX)
· Option 4: 2008 Method (1000000XXXX)
· Option 5: 2007 Method (10000000XXX)
· Option 6: 2005-2006 Method (100000000XX)

Setting Limits

After selecting a method, you'll be asked for the number of IDs to generate:

```
[!] EXAMPLE: 5000, 10000, 20000
[?] SELECT LIMIT: 
```

Enter the number of IDs you want to test.

Running the Tool

The tool will:

1. Generate UIDs based on the selected series
2. Test each UID with common passwords
3. Show real-time progress
4. Save successful accounts to /sdcard/TNEH-OK.txt
5. Save checkpoint accounts to /sdcard/TNEH-CP.txt

🔧 Technical Details

Password List

The tool uses the following default password list:

· 123456
· 1234567
· 12345678
· 123456789
· 123123
· 112233
· 1234567890
· password
· @@@###

UID Generation Patterns

· 2013-14: 100009 + 11 random digits
· 2010: 100001 + 10 random digits
· 2009: 100000 + 9 random digits
· 2008: 1000000 + 8 random digits
· 2007: 10000000 + 7 random digits
· 2005-2006: 100000000 + variable digits

Output Files

· TNEH-OK.txt: Contains working accounts in format UID|PASSWORD
· TNEH-CP.txt: Contains checkpoint accounts in format UID|PASSWORD

⚠️ Disclaimer

IMPORTANT: This tool is for educational purposes only. The developer is not responsible for any misuse of this tool. Use at your own risk and only on accounts you own or have permission to test.

Legal Notice

· This tool should only be used for ethical hacking and security testing
· Never use this tool to compromise accounts without explicit permission
· Respect privacy and follow all applicable laws and regulations
· The developer assumes no liability for any damages caused by misuse

🔒 Security Features

1. Admin Authentication: Requires admin key (None) to run
2. Encrypted Connections: Uses HTTPS for all requests
3. Random User Agents: Rotates user agents to avoid detection
4. Rate Limiting: Built-in delays to prevent server overload

🛠️ Troubleshooting

Common Issues

1. "Module not found" error
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```
2. PyCurl installation fails
   ```bash
   # For Termux
   pkg install libcurl openssl
   LDFLAGS="-L${PREFIX}/lib" CFLAGS="-I${PREFIX}/include" pip install pycurl
   ```
3. Tool not generating results
   · Check internet connection
   · Try using Flight Mode trick mentioned in tool
   · Ensure you're using correct UID series
4. Permission denied errors
   ```bash
   # For Termux
   termux-setup-storage
   ```

Error Messages and Solutions

· "Admin Key Incorrect": Contact developer for valid key
· "Connection Error": Check internet or try different network
· "No Results": Try different UID series or increase limit

📝 Notes

1. Flight Mode Trick: The tool mentions using Flight Mode if no results appear
2. UID Availability: Older UID series may have limited active accounts
3. Success Rate: Varies based on UID series and password combinations
4. File Locations: Results are saved to /sdcard/ in Android devices

🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

📞 Support

For support, issues, or questions:

· Check the 01611229803 page
· Contact the developer through appropriate channels

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments

· Developer: NOMAN
· Team: TNEH CREW
· Thanks to all contributors and testers

---

Remember: Always use ethical hacking practices and respect others' privacy and security.

Last Updated: October 2024
Version:1.0.0
