import
TNEH UID Cloner Tool

https://img.shields.io/badge/TNEH-CLONER-red
https://img.shields.io/badge/Python-3.7+-blue
https://img.shields.io/badge/License-MIT-green
https://img.shields.io/badge/Status-Active-brightgreen
https://img.shields.io/badge/GitHub-Noman3015237350-blue

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
· Cross-Platform: Works on Termux (Android), Linux, and Windows

🚀 Installation

Prerequisites

· Python 3.7 or higher
· Linux/Termux (Android) or Windows
· Internet connection
· Git (optional)

Clone Repository

```bash
git clone https://github.com/Noman3015237350/tneh-cloner.git
cd tneh-cloner
```

Termux Installation (Android)

```bash
# Update packages
pkg update && pkg upgrade

# Install Python and dependencies
pkg install python -y
pkg install python-pip -y
pkg install git -y
pkg install libcurl -y
pkg install openssl -y

# Clone repository
git clone https://github.com/Noman3015237350/tneh-cloner.git
cd tneh-cloner

# Install required modules
pip install requests beautifulsoup4 rich httpx
```

Linux Installation

```bash
# Install system dependencies
sudo apt-get update
sudo apt-get install python3 python3-pip git libcurl4-openssl-dev libssl-dev

# Clone and install
git clone https://github.com/Noman3015237350/tneh-cloner.git
cd tneh-cloner
pip3 install -r requirements.txt
```

Windows Installation

```bash
# Install Python from python.org
# Install Git from git-scm.com

# Open Command Prompt or PowerShell
git clone https://github.com/Noman3015237350/tneh-cloner.git
cd tneh-cloner
pip install -r requirements.txt
```

Install PyCurl (if needed)

```bash
# For Termux
LDFLAGS="-L${PREFIX}/lib" CFLAGS="-I${PREFIX}/include" pip install pycurl

# For Linux
sudo apt-get install libcurl4-openssl-dev libssl-dev
pip install pycurl

# For Windows (using pre-built wheel)
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
# In Termux
python tneh_cloner.py

# In Linux
python3 tneh_cloner.py

# In Windows
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

Enter the admin key: None

Main Menu

After authentication, you'll see the TNEH banner and main menu with options for different UID series.

Selecting UID Series

Choose the appropriate year method based on the UID series you want to test:

Option Year Method UID Pattern Description
1 2011-2012 100009 + 11 digits Latest old UIDs
2 2010 100001 + 10 digits 2010 series
3 2009 100000 + 9 digits 2009 series
4 2008 1000000 + 8 digits 2008 series
5 2007 10000000 + 7 digits 2007 series
6 2005-2006 100000000 + digits Oldest UID series
0 Exit - Exit the tool

Setting Limits

After selecting a method, enter the number of IDs to generate (e.g., 5000, 10000, 20000).

Running the Tool

The tool will:

1. Generate UIDs based on the selected series
2. Test each UID with common passwords
3. Show real-time progress
4. Save successful accounts to /sdcard/TNEH-OK.txt
5. Save checkpoint accounts to /sdcard/TNEH-CP.txt

🔧 Technical Details

Password List

Default password combinations tested:

· 123456
· 1234567
· 12345678
· 123456789
· 123123
· 112233
· 1234567890
· password
· @@@###

Output Files

· TNEH-OK.txt: Contains working accounts (format: UID|PASSWORD)
· TNEH-CP.txt: Contains checkpoint accounts (format: UID|PASSWORD)

File Locations

· Android/Termux: /sdcard/TNEH-OK.txt and /sdcard/TNEH-CP.txt
· Linux/Windows: Current directory

⚠️ Disclaimer

IMPORTANT: This tool is for educational purposes only. Use only on accounts you own or have explicit permission to test.

Legal Notice

· Use only for ethical hacking and security testing
· Never compromise accounts without permission
· Respect privacy and follow all laws
· Developer assumes no liability for misuse

🔒 Security Features

1. Admin Authentication: Requires admin key (665577)
2. HTTPS Encryption: Secure connections
3. Random User Agents: Avoids detection
4. Rate Limiting: Prevents server overload

🛠️ Troubleshooting

Common Issues & Solutions

1. "Module not found" error
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```
2. PyCurl installation fails (Termux)
   ```bash
   pkg install libcurl openssl
   LDFLAGS="-L${PREFIX}/lib" CFLAGS="-I${PREFIX}/include" pip install pycurl
   ```
3. Permission errors (Termux)
   ```bash
   termux-setup-storage
   ```
4. No results appearing
   · Check internet connection
   · Try Flight Mode trick
   · Use correct UID series
   · Increase ID limit
5. Tool not starting
   · Ensure Python 3.7+ is installed
   · Check admin key is correct
   · Verify all dependencies installed

Error Messages

· "Admin Key Incorrect": Use correct key or contact developer
· "Connection Error": Check internet or try different network
· "Import Error": Install missing modules from requirements.txt

📝 Pro Tips

1. Flight Mode Trick: If no results appear, toggle Flight Mode on/off
2. UID Selection: Older series have fewer active accounts
3. Success Rate: Varies by series - newer series have higher success
4. Batch Processing: Test multiple series for better results
5. Storage: Ensure sufficient storage space for result files

📊 Performance

· Threads: 50 concurrent threads
· Speed: 100-500 IDs per minute (depends on network)
· Memory: Low memory usage
· CPU: Moderate CPU usage

🤝 Contributing

Contributions welcome! Follow these steps:

1. Fork the repository
2. Create feature branch (git checkout -b feature/AmazingFeature)
3. Commit changes (git commit -m 'Add AmazingFeature')
4. Push to branch (git push origin feature/AmazingFeature)
5. Open Pull Request

Development Setup

```bash
git clone https://github.com/Noman3015237350/tneh-cloner.git
cd tneh-cloner
# Make your changes
# Test thoroughly
# Submit PR
```

📞 Support & Issues

· GitHub Issues: Report Issues
· Developer: Noman
· Note: For security reasons, contact through GitHub only

🔄 Updates

Check for updates:

```bash
cd tneh-cloner
git pull origin main
pip install -r requirements.txt --upgrade
```

📄 License

MIT License - See LICENSE file for details.

🙏 Acknowledgments

· Developer: Noman
· Team: TNEH CREW
· Testers: All contributors and beta testers
· Community: Open source community

🌟 Star History

If you find this tool useful, please give it a star on GitHub!

---

Remember: Ethical hacking only. Respect privacy and security.

Last Updated: December 2024
Version: 1.0.0
GitHub: https://github.com/Noman3015237350/tneh-cloner.git

---

Quick Start Commands

```bash
# Clone and run
git clone https://github.com/Noman3015237350/tneh-cloner.git
cd tneh-cloner
python tneh_cloner.py
# Admin Key: 665577
```

Happy ethical hacking! 🚀
