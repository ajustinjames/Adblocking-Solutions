# Adblocking Solutions

Tips and tricks I have learned for blocking advertisements and trackers on the internet.

This list is for educational purposes only, and I take no responsibility for situations these tools may put you in. Feel free to submit PRs to add your own information or fork this repo.

# Background

Online advertisements have become an unfortunate necessity in today's online ecosystem. Providing services and hosting content is not free, so something needs to pay for it. It is unreasonable to expect each user to pay for each website or service they use on a daily basis. In 2021, digital advertising spending reached $521,000,000,000 and is projected to pass 876 billion dollars in 2026. In 2020, the internet was the largest medium for advertisements accounting for 51% of total media ad spend.<sup>[1](https://www.statista.com/statistics/237974/online-advertising-spending-worldwide/)</sup> With the industry only growing, online advertising will remain an important part of the internet.

## Why block ads?

While online advertisements are an important backbone of the internet, there are some reasons why one may choose to block them.

- Targeted Advertisements
- Avoiding deception
- General annoyances

# Web Browsers

Before we can discuss blocking ads on the internet we must briefly mention your choice of browser. Most browsers today are a fork of Chromium. These browsers include Google Chrome, Microsoft Edge, Opera, Brave, and many more. These browsers currently support adblocking, but the future of this support is unclear with Google introduction of Manifest v3. This change can affect how browsers support adblocking in the future. <sup>[2](https://www.xda-developers.com/google-chrome-manifest-v3-ad-blocker-extension-api/)</sup>

## Recommended Browser

### **[Firefox](https://www.mozilla.org/en-US/firefox/new/)**

For now Firefox is my recommendation. Its not perfect<sup>[3](https://support.mozilla.org/en-US/kb/sponsor-privacy)</sup>, but is an open source browser with strong community extension support and the tools to strength the privacy and adblocking properties

<details>
  <summary>Recommended settings</summary>
  
  Here are some recommendations to improve your firefox experience:

  - Turn off sponsored content
  - Disable pocket
  - Switch search to DuckDuckGo
  - Turn off search suggestions
  - Set Enhanced Tracking Protection to Strict
  - Disable passwords, address, credit cards, autofill, forms saving
  - Disable firefox data collection and studies
  - Enable HTTPS-Only Mode in all windows
</details>

## Alternative

### **[Brave](https://brave.com/)**

If you absolutely must use a Chromium browser, I recommend not using Google Chrome or Microsoft Edge. It can be argued which is worse for privacy.<sup>[4](https://www.intrust-it.com/edge-vs-chrome-what-is-the-safest-browser/)</sup> I use Brave even through the controversies<sup>[5](https://en.wikipedia.org/wiki/Brave_(web_browser)#Controversies)</sup> as the product has options to disable unnecessary features and it works better than Firefox on Android.

# Extensions

## **[uBlock Origin](https://ublockorigin.com/)**

This is the main extension I will recommend for blocking internet advertisements. It is open source, efficient, customizable, and supported on a variety of platforms. This extension even blocks ads on YouTube.

## **[ClearURLs](https://docs.clearurls.xyz/)**

This extension clears extraneous parameters from URLs. This is not necessarily beneficial to adblocking, but does help with preventing tracking. Most of the functionality can also be replicated in uBlock Origin, but this extension is more comprehensive.

## **[SponsorBlock](https://sponsor.ajay.app/)**

While uBlock Origin may take care of ads served by YouTube, many creators have added sponsored segments to their videos to supplement the income provided from YouTube's ads. This extension allows the user to highlight or even auto-skip sponsored segments, self-promotion, off topic sections, or even jump to highlights of a video. This extension does need some configuring, but the UI is simple enough to quickly set and forget.

# DNS

While installing extensions is preferred to block most internet advertisements, it may not be applicable in all use cases. For example, on iOS there is currently no option to install uBlock Origin on any browser available on the platform. To continue blocking ads, users can utilize DNS based adblocking to continue to remove internet advertisements from browsers and even in-app advertisements. DNS based adblocking basically acts as a firewall, if a request is made to a domain on your blocklist, it will be blocked, which can prevent advertisements from showing.This can potentially improve network performance since fewer assets will be loaded.

## **[NextDNS](https://nextdns.io/)***

NextDNS is a DNS service similar to CloudFlare or Google's 8.8.8.8 with an extensive amount of customization. Users can set blocklists, utilize different configurations for different devices, DNS rewrites, DNSSEC, encrypted DNS, and block pages. Since this service is hosted through the internet, you can access this DNS anywhere through any network.

## **[PiHole](https://sponsor.ajay.app/)**

PiHole is the default app for network DNS adblocking. Run this on a device like a [Raspberry Pi](https://www.raspberrypi.com/), and point your router to serve the Pi as your DNS server. Then all your devices instantly will have their requests filtered based on the configuration of the PiHole service. To use this outside of your home network, you will need to [VPN](https://pivpn.io/) into your network.

## **[AdGuard](https://sponsor.ajay.app/)**

AdGuard offers a variety of adblocking solutions. The DNS services they offer are [AdGuard DNS](https://adguard-dns.io/en/welcome.html) and [AdGuard Home](https://adguard.com/en/adguard-home/overview.html). AdGuard DNS is similar to NextDNS as its a hosted DNS solution filters ads. AdGuard Home is similar to PiHole as the user will need to deploy it to a device then point other device to use it for DNS.

## **[Blokada](https://sponsor.ajay.app/)**

Another DNS based adblocker that runs as an app on an Android device. I'll only focus on the DNS part of the app. It runs as a local DNS server on your android device and will block domains found on your blocklist. Since the service runs on the device through a VPN connection, it can potentially drain small amounts of battery.

# Mobile Apps

## **[NewPipe](https://sponsor.ajay.app/)**

NewPipe is a lightweight alternative front-end client for YouTube. This app supports background playing, audio streams, video download, and no ads.

# Site Specific Suggestions

## Twitch

Twitch has started to crack down hard on adblocking. uBlock Origin no longer blocks twitch content by default. Specialized configurations or extensions are needed to block ads here.

### **[TwitchAdSolutions](https://github.com/pixeltris/TwitchAdSolutions)**

This repo collects a number of Twitch adblocking solutions. The tools listed here may no longer work as Twitch continues to fight adblocking on their site.

# Blocklists

You should not ad as many blocklists as possible, as it will end up blocking non-ads through false positives. It can also be resource intensive causing slowdowns and increased battery usage. You should find a balance to pick the lists you need. I currently enable all of the default blocklists in uBlock Origin

## Notable Blocklists

- [AdAway](https://adaway.org/)
  - Mobile ads 
- [anudeepND Blacklist](https://github.com/anudeepND/blacklist)
  - Curated to block trackers and advertisements
- [AdGuard Filters](https://github.com/AdguardTeam/AdguardFilters)
  - Variety of filters for many situations
- [Dan Pollock's Hosts](https://someonewhocares.org/hosts/)
  - Curated list of various domains
- [EasyList](https://easylist.to/)
  - Variety of filters to block ads, tracking, cookie banners, social media widgets, and annoyances
- [oisd](https://oisd.nl/)
  - Comprehensive blocklist in a variety of categories. Run this one solo.
- [The Big BlockList Collection](https://firebog.net/)
  - Curated list of various blocklists. Maintained by WaLLy3K

# Allowlists

When using blocklists you may run into a situation where a service you may need inadvertently is blocked. Fortunately you can use allowlists to prevent these domains from being blocked.

## Notable Allowlists

- [anudeepND Whitelist](https://github.com/anudeepND/whitelist)
  - Commonly white listed websites from various sources
- [Commonly Whitelisted Domains](https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212)
  - PiHole forum discussion of domains to be whitelisted


# Conclusion

Even though advertisements are vital in today's internet, I believe it has gone too far. Reduced privacy and increased annoyances are reasons that have pushed me to research adblocking. Even though I have the option to block most ads, I still prefer to support content directly when given the option. Some examples that I subscribe to are [YouTube Premium](https://www.youtube.com/premium), [Twitch Turbo](https://www.twitch.tv/turbo), and [Hulu (No Ads)](https://help.hulu.com/s/article/hulu-no-ads#hulu). 

<br />

*Indicates that services has a recurring subscription

<br />
<br />
<br />
<br />
<br />

<sub>I hope this resource was helpful to you. If you found value in it, consider [donating](https://www.paypal.com/donate/?business=QWZF9UMPMWCCA&no_recurring=0&item_name=Donate+to+support+my+work.+Your+generosity+helps+me+continue+developing+valuable+tools+for+you.+Thank+you+for+your+support%21&currency_code=USD) as it helps me continue providing helpful resources and tools like this one. Your support is appreciated, but never expected.</sub>