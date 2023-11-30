# reconY

ReconY is an automated reconnaissance script written in Bash designed to streamline the initial phase of security assessments. It integrates various tools and techniques to discover subdomains, find open ports, capture screenshots, and perform content discovery on target domains. The script is highly customizable, allowing users to configure parameters based on their preferences.

## **Features**

- **Subdomain Enumeration:** Uses tools like Subfinder, Assetfinder, and others to discover subdomains associated with the target domain.
- **Wayback Machine Analysis:** Scrapes the Wayback Machine for historical URLs and extracts potential vulnerabilities using GF (Grep Find).
- **Host Alive Detection:** Probes for live hosts using httprobe and httpx, removing non-responsive hosts.
- **Directory and File Discovery:** Utilizes Dirsearch to discover common directories and files on live subdomains.
- **Screenshots:** Captures screenshots of the target's HTTP and HTTPS ports using Aquatone.
- **Content Discovery:** Identifies potential vulnerabilities by analyzing Wayback Machine data and looking for specific patterns like SSRF, IDOR, LFI, etc.
- **WAF Detection:** Identifies potential Web Application Firewalls (WAFs) in use.
- **CNAME Analysis:** Identifies CNAME records and checks for potential NS takeover vulnerabilities.
- **Reports Generation:** Generates detailed HTML reports for each subdomain, providing an overview of the reconnaissance findings.

## **Prerequisites**

- Bash shell
- Various reconnaissance tools such as Subfinder, Assetfinder, httprobe, httpx, Dirsearch, Aquatone, GF, and others (Make sure they are installed and available in your PATH).

## **Installation**

1. Clone the repository:
    
    ```bash
    bashCopy code
    git clone https://github.com/yourusername/ReconY.git
    cd ReconY
    
    ```
    
2. Edit the configuration section in the script (**`recony.sh`**) to set the desired parameters.

## **Usage**

Run the script with the target domain as an argument:

```bash
bashCopy code
./recony.sh -d target.com

```

Additional options include specifying excluded subdomains (**`-e`**) and providing custom subdomain reports (**`-r`**).

```bash
bashCopy code
./recony.sh -d target.com -e excluded.domain.com,other.domain.com -r subdomain1.domain.com -r subdomain2.domain.com

```

## **Customization**

- Configure the script parameters in the configuration section of **`recony.sh`** based on your preferences.
- Customize the tools and their options as needed.

## **Disclaimer**

This script is provided for educational and ethical testing purposes only. The author is not responsible for any misuse or damage caused by this script.

## **Acknowledgments**

- Special thanks to the developers of the tools integrated into this script.
- Inspired by various reconnaissance methodologies and community contributions
