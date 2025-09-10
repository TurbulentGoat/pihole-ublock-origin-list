# Comprehensive Blocker Lists

A curated collection of DNS blocklists compiled from multiple trusted sources for maximum protection against ads, trackers, malware, and other unwanted content.

## What's Included

This repository contains a comprehensive blocklist that combines multiple protection categories:

- **Ads & Tracking** - Blocks advertising networks and tracking domains
- **Malware & Phishing** - Protects against malicious domains and phishing attacks  
- **Fake Stores & Scams** - Blocks fake shopping sites and internet scams
- **Cryptojacking** - Prevents cryptocurrency mining scripts
- **Telemetry** - Blocks software telemetry and data collection
- **Affiliate Links** - Blocks referral and affiliate tracking domains

## Available Lists

### Main Blocklist
- **File**: `multi-list.txt`
- **Entries**: ~1.1 million domains (Number of gravity domains: 1278058 (1112559 unique domains))
- **Format**: Mixed (plain domains + uBlock Origin syntax)
- **Compatibility**: Pi-hole, uBlock Origin, AdGuard, and other DNS filtering tools

## How to Use

### For Pi-hole Users

[This guide](https://www.raspberrypi.com/tutorials/running-pi-hole-on-a-raspberry-pi/) is for Raspberry Pis but will work with (most if not all) Debian based Linux distros. I've followed it on a raspberry  pi with Raspi OS and Ubuntu and works fine. 

1. Access your Pi-hole admin panel
2. Go to **Group Management** → **Lists**
3. Add this URL:
   ```
   https://raw.githubusercontent.com/TurbulentGoat/pihole-ublock-origin-list/refs/heads/main/multi-list.txt
   ```
4. Click **Add blocklist**
5. Go to **Tools** → **Update Gravity**
6. Click **Update**

### For uBlock Origin Users

1. Open uBlock Origin settings (get it here https://ublockorigin.com/)
2. Go to **Filter lists** tab
3. Scroll to **Import** section
4. Add this URL:
   ```
   https://raw.githubusercontent.com/TurbulentGoat/pihole-ublock-origin-list/refs/heads/main/multi-list.txt
   ```
5. Click **Apply changes**

## Important Notes

### Blocking Level
- **Type**: Aggressive/Comprehensive
- **Target Users**: Experienced users
- **Admin Required**: Yes (for unblocking false positives)

### Potential Issues
- May contain some false positive domains
- Could limit functionality of certain services
- Referral/affiliate domains are blocked (may affect some legitimate links)

### Recommendations
- Start with a smaller blocklist if you're new to DNS filtering
- Keep a record of any domains you need to manually whitelist
- Test thoroughly with your regular browsing habits

## Sources

This blocklist is compiled from multiple trusted sources including:

- **HaGeZi's DNS Blocklists**
  - [Multi PRO++ - Maximum protection](https://github.com/hagezi/dns-blocklists?tab=readme-ov-file#proplus)
  - [Fake - Protects against internet scams, traps & fakes!](https://github.com/hagezi/dns-blocklists?tab=readme-ov-file#fake)
  - [Threat Intelligence Feeds - Increases security significantly!](https://github.com/hagezi/dns-blocklists?tab=readme-ov-file#tif)
- **Additional curated sources** for comprehensive coverage

### Detailed Source Information

**Multi PRO++**: Sweeper - Aggressive cleans the Internet and protects your privacy! Blocks Ads, Affiliate, Tracking, Metrics, Telemetry, Phishing, Malware, Scam, Fake, Cryptojacking and other "Crap".

**Fake**: A blocklist for blocking fake stores, -streaming, rip-offs, cost traps and co.

**Threat Intelligence Feeds**: A blocklist for blocking Malware, Cryptojacking, Scam, Spam and Phishing. Blocks domains known to spread malware, launch phishing attacks and host command-and-control servers.

## Updates

The blocklist is periodically updated to include new threats and remove outdated entries. Check the commit history for update frequency.

## Contributing

If you encounter false positives or have suggestions for additional sources, please:

1. Open an issue describing the problem
2. Include the specific domain(s) affected
3. Provide context about why the domain should be whitelisted

## Licence

This project is provided as-is for educational and personal use. Please respect the original sources' licences and terms of use.

## Support

If this blocklist helps protect your network, consider:
- Go show love to the original authors of the included lists/share their lists/support them somehow!
- Starring this repository
- Contributing improvements or reporting issues

---

**Disclaimer**: Use at your own risk. This blocklist may block legitimate content. Always have a way to disable or modify filtering if needed. It is literally just the lists I use myself.
