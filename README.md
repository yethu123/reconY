# reconY

**Overview:**

This script automates a comprehensive recon framework for gathering information about a target domain. It combines tools like Subfinder, Aquatone, Dirsearch, and more to discover subdomains, enumerate live hosts, identify potential vulnerabilities, and gather additional intelligence.

**Disclaimer:**

This script is provided for educational purposes only and should not be used without permission on domains you do not own. Misusing this script for malicious purposes is illegal and unethical.

**Requirements:**

**Operating System:**

- Linux-based operating system

**Tools:**

**Essential:**

- **Subfinder:** [https://github.com/projectdiscovery/subfinder](https://github.com/projectdiscovery/subfinder)
- **Assetfinder:** [https://github.com/tomnomnom/assetfinder](https://github.com/tomnomnom/assetfinder)
- **HTTPX:** [https://github.com/projectdiscovery/httpx](https://github.com/projectdiscovery/httpx)
- **Waybackurls:** [https://github.com/tomnomnom/waybackurls](https://github.com/tomnomnom/waybackurls)
- **Gau:** [https://github.com/lc/gau](https://github.com/lc/gau)
- **GF (GrepFuzz):** [https://github.com/tomnomnom/gf](https://github.com/tomnomnom/gf)
- **Dirsearch:** [https://github.com/maurosoria/dirsearch](https://github.com/maurosoria/dirsearch)
- **Unfurl:** [https://github.com/tomnomnom/unfurl](https://github.com/tomnomnom/unfurl)

**Optional:**

- **Aquatone:** [https://github.com/michenriksen/aquatone](https://github.com/michenriksen/aquatone) (Requires Chromium: [https://chromium.org/](https://chromium.org/))
- **Massdns:** [https://github.com/blechschmidt/massdns](https://github.com/blechschmidt/massdns) (For advanced subdomain discovery)

**Installation:**

Follow the installation instructions for each tool on their respective websites or repositories. Some tools may require additional dependencies, like Python and Go.

**Usage:**

```jsx
./recony.sh -d <target_domain> [options]

Options:
  -d <target_domain>     Required - Target domain to scan.
  -e <excluded_domain>   Optional - Domain to exclude from subdomain discovery.
  -r <subdomain>         Optional - Specific subdomain to recon (for recursive checks).
  -s <foldername>        Optional - Specify a custom folder name for storing results.
```

**Features:**

- Subdomain discovery with Subfinder and Assetfinder
- Live host enumeration with HTTPX and Massdns (optional)
- Wayback URL discovery with Waybackurls and Gau
- Potential vulnerability identification with GF
- Web technology discovery with Dirsearch
- Screenshot capture with Aquatone (Chromium required)
- Recursive subdomain checks on discovered subdomains
- DNS record checks with CNAME analysis for potential takeover vulnerabilities
- Extracting parameters and URLs from Wayback data for further analysis
- Wordlist-based directory bruteforcing with Dirsearch
- Parameter extraction from discovered URLs with Unfurl

**Inspiration and Credits:**

This script is heavily inspired by the lazyrecon script by nahamsec: [https://github.com/nahamsec/lazyrecon](https://github.com/nahamsec/lazyrecon). We thank nahamsec for their contribution and valuable resource.

**Additional Notes:**

- Review the script configuration options to customize your scan.
- The script will create a directory named `<target_domain>_<date>` within the current directory to store results.
- Consider the limitations of each tool and use additional techniques for a comprehensive assessment.
- Remember to use this script responsibly and ethically, respecting legal and privacy obligations.

**Further Customization:**

You can modify the script to include additional tools, adjust wordlists, and adapt it to your specific needs. Please use this tool responsibly and ethically.
