Home

## About Me
As an undergraduate cybersecurity professional specializing in threat and incident response, my skill set encompasses ethical hacking, hashing, and encoding techniques such as Base64. Additionally, I possess expertise in utilizing terminal commands to address intricate cybersecurity challenges. I am well-versed in dark web intelligence, including the utilization of tools like the Tor browser. Furthermore, I have gained practical experience in OSINT threat intelligence analysis, threat hunting, and ethical hacking methodologies.

With a robust foundation in cybersecurity principles and practical applications, I am motivated to confront emerging threats and fortify digital environments through innovative and effective solutions.

## Certifications:
- ArcX Foundation Level Threat Analyst
- ISC-2 Certified in Cybersecurity
- Security Blue Team Junior Analyst


## Projects
Here are a few projects I have worked on:

1. **Threat Intelligence - Digital Forensics Investigation** 
This project involved assisting in the investigation of a criminal on the run, who posted images with the caption, "I'm roaming free. You will never catch me." The goal was to analyze these images to extract crucial information that could help track down the criminal's location.

**Steps Taken**:

**Metadata Extraction**: To begin, the images provided were analyzed for embedded metadata using ExifTool, a powerful tool for extracting and viewing metadata from various media files. After installing ExifTool on a MacBook using Homebrew and leveraging the Terminal, I extracted key pieces of information from the images, including the camera model, timestamp, and GPS coordinates.

**Geolocation Analysis**: Initially, the GPS coordinates extracted from the images pointed to a location in the Pacific Ocean. This required further investigation to pinpoint the criminal's actual whereabouts. To proceed, I used TinEye, a reverse image search tool, to search for similar images and gather context about their origin.

**Investigative Research**: The reverse image search led me to discover that the image was most likely taken in Kathmandu, Nepal. To refine this hypothesis, I reviewed the metadata further and noticed a reference to the word "temple" in one of the titles. A quick Google search for temples in Kathmandu led me to the Temple of Kathmandu, which seemed to align with the context provided by the image.

**Conclusion**: Combining the metadata extraction, reverse image search, and geographic research, I concluded that the criminal was likely in Kathmandu, Nepal, as of the time the images were posted.
Skills Demonstrated:

This project highlighted several important skills in digital forensics and threat intelligence, **including**:

   - **Metadata Extraction**: Using ExifTool to extract detailed metadata from images, such as camera model, timestamp, and GPS coordinates, which were crucial for identifying the criminal's location.

   - **Geolocation Analysis**: The ability to interpret and analyze geographic data embedded in image files and refine it through additional tools like TinEye for reverse image searching.
     
   - **Digital Forensics**: Leveraging forensic techniques to gather and analyze evidence from digital media, applying both technical knowledge and investigative skills to solve the case.
     
   - **Critical Thinking and Problem Solving**: The ability to connect seemingly disparate pieces of information to uncover the location of the criminal and further the investigation.

     
**Tools Used**:

**ExifTool**: For extracting metadata from images to gather important details like camera model, timestamp, and GPS coordinates.
**TinEye**: A reverse image search tool that helped track the origin of the images, leading to the discovery of the criminal’s location.
Conclusion:

This project showcased my proficiency in digital forensics, metadata extraction, and investigative techniques, demonstrating my ability to solve complex problems through the use of digital tools. It provided valuable hands-on experience in applying cybersecurity knowledge to real-world scenarios, ultimately contributing to the resolution of a criminal investigation.

   - **Key Skills**: Metadata Extraction · Command Line Proficiency · Geolocation Analysis
  
   --------------------------------------


     

**Dark Web Operations – Intelligence Gathering & Drug Trafficking Case**
I successfully completed the final challenge of the Dark Web Operations course by Security Blue. In this simulated law enforcement scenario, I was tasked with investigating a dark web marketplace used by drug traffickers. Using tools such as Tor and inspecting website elements, I gained access to a protected site to gather intelligence related to an ongoing criminal operation.

## Challenge Breakdown:

**Objective**: The criminal, having evaded law enforcement after their main dark web marketplace was dismantled, continued to operate in the UK using the Tor network. My task was to:
Gain access to the secured site.
Identify evidence connecting the individual to drug trafficking.
Find details about an upcoming illegal shipment for interception.
Steps Taken:

**Accessing the Dark Web Site**: The first step involved using Tor, a privacy-focused browser, to access the provided .onion link. After installing the Tor Browser and pasting the link (5xdv6dqxv2bsbmlgttsq3ma3nw6ffa2zhqbl7o4w46p32wsqulzrtsqd.onion) into the address bar, I accessed a dark web site with protected content.
Generating Valid Credentials: The site required valid user credentials for deeper access. Since a clear username and password were not available, I employed the "Inspect Element" feature on the browser's developer tools to access the site’s console. Using the console, I executed the command generateusercredentials, which provided an encoded string. This string was then decoded using Base64 encoding to reveal the username and password, allowing me to gain authenticated access.

**Site Analysis**: With access granted, I navigated through the site and analyzed the content, which included posts and images. Key investigative tasks included:
Identifying the User's Information: Through careful review of the site’s posts, I identified the suspect’s username, first and last name, and other relevant personal details. I also identified the suspect’s country of residence based on contextual clues from posts.

**Decoding Site Content**: One significant post included an image of a computer screen with a yellow sticky note that had blurry GPS coordinates. I extracted these coordinates and used Google Earth to pinpoint their location, which revealed them to be in the Port of Felixstowe, England, a crucial clue for locating the shipment’s destination.

**Key Evidence for Law Enforcement**: Throughout my investigation, I uncovered several key pieces of evidence:
A first post related to drug trafficking was found, providing context about the criminal’s activities.
The latest post was identified, revealing that the criminal was still active and continuing operations.

**Encoded Information**: I discovered that the site was using Base64 encoding to obscure certain information, which I decoded to gather valuable details.
The date and location of the next shipment were identified, as well as a GPS coordinate from a blurry sticky note that pointed to Port of Felixstowe.
Additionally, a plane ticket was found in one of the posts, with a destination to London, further confirming the suspect’s link to the UK.

**Investigative Details**: My investigation led to several important findings:
The suspect’s username, real name, and current country of residence were identified.
The date of the first post related to drug trafficking was established.
The date of the latest post confirmed ongoing activity.
The GPS coordinates from the sticky note were cross-referenced with Google Earth, revealing a seaport in England.
Based on the post and the coordinates, it was concluded that the suspect was involved in drug trafficking operations, and the next shipment was set to arrive at Port of **Felixstowe, England**.

**Skills Demonstrated**:

This project required proficiency in several cybersecurity and investigative areas:

   - **Dark Web Navigation**: Using the Tor browser to access hidden, secured sites on the dark web.
     
   - **Credential Generation and Decryption**: Leveraging browser developer tools and Base64 encoding to generate and decode valid credentials.
     
   - **Forensic Analysis of Digital Content**: Inspecting images, posts, and encoded data to extract and analyze critical information.
     
   - **Geolocation Analysis**: Using GPS coordinates and Google Earth to locate the physical locations associated with the criminal’s activities.
     
   - **Cyber Intelligence and Investigative Research**: Gathering evidence to tie the suspect to drug trafficking activities and uncover details related to the shipment.


## **Skills**
Here are some of the skills I have acquired:

   - **Cybersecurity**: Incident Response, Threat Analysis, Security Operations, Cybersecurity Policy Compliance, Data Decryption, Dark Web Investigations, Vulnerability Assessment, Network Security

   - **Programming**: Python, Bash scripting, Data Analytics (Python), Cybersecurity-related Automation
     
   - **Networking**: TCP/IP, DNS, VPN, Firewalls, IDS/IPS, Network Security, Cyber Threat Detection
     
   - **Tools**: Splunk, Wireshark, Nmap, Metasploit, Tor, Base64 Decoding, Inspect Element, Jekyll (for GitHub Pages), GitHub
     
   - **Operating Systems**: macOS, Linux (Ubuntu, Kali)

## Cybersecurity Tools:
Splunk, Wireshark, Nmap, Metasploit, Tor, Base64 Decoding/Encoding Tools, Inspect Element, Kali Linux, Nessus, Snort, Burp Suite, CyberChef,
## Programming and Scripting:
Python, Bash, Jekyll, Git, Docker,
## Networking and Systems Tools:
Tcpdump, OpenVPN (using Tunnelblick or OpenVPN client), WiFi Analyzer (apps or built-in macOS wireless diagnostics), Vim/Emacs, VirtualBox/VMware, Xcode
## Operating Systems and Environments:
macOS, Linux, Docker,
## Other Tools/Technologies:
GitHub
Cybersecurity Frameworks (e.g., NIST, MITRE ATT&CK)
Google Earth

## Education
**Colorado State University Global**: 06/2024-02/2026

**Cumulative GPA**: 3.70/4.00

**Bachelor of Science**: Cybersecurity

**Specializations**: Python & Data Analytics, Intelligence & Homeland Security

**Organizations**: National Social Science Association, The Association of Certified Fraud Examiners, Emergency Management & Homeland Security, International Leadership Association

## Contact Information
**TEYMARR.PAGE@PROTON.ME**

**[LinkedIn](https://www.linkedin.com/in/teymarrpage/)**
