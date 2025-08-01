# Sentinel and Integrated Threat Management

## Introduction

Cyber threat intelligence is a source from which Microsoft Sentinel gathers information that’s used to shore up your system’s defenses. This reading will extend your exploration of Sentinel, providing you with a clear picture of how it scans beyond the confines of your system for potential attacks. Drawing from its experience, Sentinel maintains an active vigilance over your system. Remaining active, Sentinel provides continuous updates as new attacks are discovered, drawing from global experiences.

---

## Sentinel Configuration

Sentinel is a large part of Microsoft’s Security Information Event Management (SIEM) solution. It plays a critical role in anticipating attacks before they can damage an organization. It achieves this by analyzing threat indicators to identify known threats, which are derived from tactical threat intelligence. This intelligence, in turn, originates from Cyber Threat Intelligence (CTI), a globally recognized information repository that outlines potential attacks on a system.

The CTI provides information about cyber threats, techniques used, and motivations behind executing a cyberattack. Created from executed attacks, CTI includes information such as IP addresses, domains, file hashes, and other threat indicators that are recorded in the wake of an attack. Recording this information makes repeating attacks more challenging for hackers and ensures that security measures grow with the sophistication of attacks performed. An indicator recorded in CTI is known as an Indicator of Compromise (IoC) or Indicator of Attack (IoA). Sentinel is configured to watch for these IoCs and informs cybersecurity specialists by raising an alarm.

Sentinel uses external resources when protecting a resource. To better protect your system, you can configure Sentinel as follows:

---

## Importing Intelligence

Sentinel can integrate with external platforms and APIs to provide active and actionable intelligence, expanding its awareness. There are many sources for these, including OpenDXL, an open-source threat analysis feed. Alternatively, an organization can opt for a paid service such as Recorded Future. In addition to paid services, an organization can connect with Government Agency Providers and industry-specific ones such as Information Sharing and Analysis Centers (ISACC). Other CTI sources include dark web monitors, social media and forums, and known phishing URLs and domain lists.

---

## Threat Intelligence and Imaging

You can access and manipulate the threat intelligence data you've imported within Microsoft Sentinel. You can do this both within the logs, where you can correlate this data with other security events, and in a specific section called the threat intelligence blade, designed to manage and utilize this information effectively for security monitoring and incident response.

---

## Threat Detection

Security threats are detected and responded to automatically by Threat Detection, using predefined rule templates informed by imported threat intelligence. When a potential threat aligns with the conditions specified in these templates, it triggers the creation of security alerts or incidents, helping security analysts to respond swiftly and effectively to potential security breaches or anomalies.

---

## Threat Visualization

A thorough stage that covers every facet of threat modeling is threat visualization. Extending the images created from the CTI feeds, it models system attributes like the various resources on the network, access patterns, and traffic frequencies. This step allows a cyber analyst to identify where a threat may come from and how this maps onto the activities of the current system. In this way, a strong security posture can be established.

---

## Enriched Threat Indicators

In addition to all this beneficial functionality, Microsoft Sentinel provides more enriched threat indicators, such as GeoLocation, as well as information sourced from Whois and integrated with Jupyter Notebooks.

### GeoLocation

Geolocation information empowers you to analyze potential threats with insights into where they originated from. The information derived from the IP address indicates details, including country, city, and even specific coordinates.

### Whois

Whois data provides detailed information about the owner, including registration information and contact details associated with a domain name or an IP address.

### Jupyter Notebooks

Sentinel can also be configured and queried in Jupyter Notebooks. Jupyter is powered by Python, a versatile and easy-to-use coding language that empowers a security expert to query, manipulate, present, and interpret the various data signals gathered.

---

## Conclusion

In this reading, you explored the importance of Sentinel and learned why it is considered such a crucial monitoring tool. As you discovered, Sentinel can be connected to various data sources; learning where this information is stored and how it can be connected to Sentinel offers you a wealth of insight on how to configure Sentinel