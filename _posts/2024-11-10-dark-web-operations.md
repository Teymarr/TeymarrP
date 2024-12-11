---
title: "Dark Web Operations - Ethical Hacking"
date: 2024-11-10
layout: post
---
Dark Web Operations – Intelligence Gathering & Drug Trafficking Case I successfully completed the final challenge of the Dark Web Operations course by Security Blue. In this simulated law enforcement scenario, I was tasked with investigating a dark web marketplace used by drug traffickers. Using tools such as Tor and inspecting website elements, I gained access to a protected site to gather intelligence related to an ongoing criminal operation.

Challenge Breakdown:

Objective: The criminal, having evaded law enforcement after their main dark web marketplace was dismantled, continued to operate in the UK using the Tor network. My task was to: Gain access to the secured site. Identify evidence connecting the individual to drug trafficking. Find details about an upcoming illegal shipment for interception. Steps Taken:

Accessing the Dark Web Site: The first step involved using Tor, a privacy-focused browser, to access the provided .onion link. After installing the Tor Browser and pasting the link (5xdv6dqxv2bsbmlgttsq3ma3nw6ffa2zhqbl7o4w46p32wsqulzrtsqd.onion) into the address bar, I accessed a dark web site with protected content. Generating Valid Credentials: The site required valid user credentials for deeper access. Since a clear username and password were not available, I employed the "Inspect Element" feature on the browser's developer tools to access the site’s console. Using the console, I executed the command generateusercredentials, which provided an encoded string. This string was then decoded using Base64 encoding to reveal the username and password, allowing me to gain authenticated access.

Site Analysis: With access granted, I navigated through the site and analyzed the content, which included posts and images. Key investigative tasks included: Identifying the User's Information: Through careful review of the site’s posts, I identified the suspect’s username, first and last name, and other relevant personal details. I also identified the suspect’s country of residence based on contextual clues from posts.

Decoding Site Content: One significant post included an image of a computer screen with a yellow sticky note that had blurry GPS coordinates. I extracted these coordinates and used Google Earth to pinpoint their location, which revealed them to be in the Port of Felixstowe, England, a crucial clue for locating the shipment’s destination.

Key Evidence for Law Enforcement: Throughout my investigation, I uncovered several key pieces of evidence: A first post related to drug trafficking was found, providing context about the criminal’s activities. The latest post was identified, revealing that the criminal was still active and continuing operations.

Encoded Information: I discovered that the site was using Base64 encoding to obscure certain information, which I decoded to gather valuable details. The date and location of the next shipment were identified, as well as a GPS coordinate from a blurry sticky note that pointed to Port of Felixstowe. Additionally, a plane ticket was found in one of the posts, with a destination to London, further confirming the suspect’s link to the UK.

Investigative Details: My investigation led to several important findings: The suspect’s username, real name, and current country of residence were identified. The date of the first post related to drug trafficking was established. The date of the latest post confirmed ongoing activity. The GPS coordinates from the sticky note were cross-referenced with Google Earth, revealing a seaport in England. Based on the post and the coordinates, it was concluded that the suspect was involved in drug trafficking operations, and the next shipment was set to arrive at Port of Felixstowe, England.

Skills Demonstrated:

This project required proficiency in several cybersecurity and investigative areas:

Dark Web Navigation: Using the Tor browser to access hidden, secured sites on the dark web.

Credential Generation and Decryption: Leveraging browser developer tools and Base64 encoding to generate and decode valid credentials.

Forensic Analysis of Digital Content: Inspecting images, posts, and encoded data to extract and analyze critical information.

Geolocation Analysis: Using GPS coordinates and Google Earth to locate the physical locations associated with the criminal’s activities.

Cyber Intelligence and Investigative Research: Gathering evidence to tie the suspect to drug trafficking activities and uncover details related to the shipment.
