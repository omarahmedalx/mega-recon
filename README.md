 __  __                       ____                        
|  \/  | ___  __ _  __ _  ___|  _ \ ___  ___ ___  _ __   
| |\/| |/ _ \/ _` |/ _` |/ _ \ |_) / _ \/ __/ _ \| '_ \  
| |  | |  __/ (_| | (_| |  __/  _ <  __/ (_| (_) | | | | 
|_|  |_|\___|\__, |\__, |\___|_| \_\___|\___\___/|_| |_| 
             |___/ |___/                                 

Description

MegaRecon – An all-in-one automated reconnaissance framework for bug bounty hunters and penetration testers. Quickly enumerate subdomains, discover directories, scan ports, extract parameters, capture screenshots, and gather historical/CT data — all in one streamlined workflow.



Features

🌐 Subdomain Enumeration – Uses Amass, Subfinder, Assetfinder, and CT logs.

📂 Directory Fuzzing – Automated directory and file discovery with FFUF/Dirsearch.

🔌 Port Scanning – Fast scanning with Naabu and detailed scanning with Nmap.

📝 Parameter Discovery – Extracts GET/POST parameters for further testing.

🖼 Screenshots – Captures target web interfaces with Gowitness/Aquatone.

🕰 Wayback Machine Scraping – Collects archived endpoints and parameters.

🔒 Certificate Transparency Lookup – Discovers hidden subdomains from CT logs.

⚡ Automation Ready – Designed for bug bounty hunters, CTFs, and red teams.


📥 Installation

git clone https://github.com/omarahmedalx/mega-recon
cd mega-recon
chmod +x mega-recon



Install dependencies

On Arch Linux: sudo pacman -S amass subfinder nmap go git jq wget curl

On Debian/Ubuntu: sudo apt update && sudo apt install -y amass nmap git jq wget curl

Install Go-based tools:

go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install -v github.com/projectdiscovery/naabu/v2/cmd/naabu@latest
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
go install -v github.com/ffuf/ffuf@latest
go install -v github.com/tomnomnom/waybackurls@latest
go install -v github.com/sensepost/gowitness@latest

Usage
Basic run against a target:

./mega-recon example.com

Run with specific modules only:
./mega-recon -d example.com --subdomains --ports --dirs



