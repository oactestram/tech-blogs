# Clickjacking: The Sneaky "Click" Deception

***Author***: *Antsy Girl*

***Date***: *Jan 3, 2025 2:33:11 PM*

![Clickjacking with examples](https://www.imperva.com/learn/wp-content/uploads/sites/13/2019/01/Clickjacking.png)

## Summary:

Clickjacking is a malicious attack where a user is tricked into clicking something different from what they perceive.  Hidden buttons or links are overlaid on legitimate websites, leading to unintended actions. This exploits trust and can compromise accounts or data.  Prevention involves security headers and careful iframe handling.


## What is Clickjacking?

Imagine this: you're browsing your favorite social media site.  You see a cute cat video and click "Play."  But unbeknownst to you, that "Play" button is actually a cleverly disguised button on another site entirely – one that's secretly transferring all your banking details to a malicious actor! That's clickjacking in a nutshell.

Clickjacking is a type of attack where malicious code embeds a legitimate website (or part of one) within an iframe (inline frame).  This iframe is then cleverly overlaid with another seemingly innocuous layer, often with visual elements designed to trick the user into clicking something they don't intend to. The user thinks they are interacting with one site, but are actually triggering actions on a hidden, malicious website within the iframe.


## How Does it Work?

The core of clickjacking involves iframes.  These are HTML elements that allow you to embed one webpage within another. Attackers leverage this feature to create a "clickjacking frame":

* **The Malicious Layer:**  This is the top layer, what the user actually sees.  It might contain enticing visuals, a seemingly harmless button, or even be designed to look exactly like the legitimate website being hijacked.

* **The Hidden Iframe:** This sits beneath the malicious layer and contains the actual target site or a form designed to carry out the malicious action (e.g., a form transferring banking details, changing account settings).

* **The Trick:** The attacker carefully positions the malicious layer over the iframe, making the target button or link indistinguishable.  When the user clicks what they believe is a benign element, they are unwittingly triggering the action within the hidden iframe.


## Use Cases (for Attackers, unfortunately!):

* **Account Takeovers:** Tricking users into approving malicious app access or changing passwords on banking sites or social media platforms.

* **Data Theft:**  Hidden forms could be used to steal sensitive information like credit card numbers, addresses, or personal details.

* **Malware Installation:**  Users could unknowingly download and install malware by clicking a disguised button.

* **Phishing Enhancements:**  Clickjacking can be used to make phishing attacks appear more legitimate, increasing their success rate.



## Case Study:  The MySpace Clickjacking Incident

While not a massive data breach, a now-famous clickjacking attack targeted MySpace users. Attackers created deceptive pages that tricked users into clicking what appeared to be a legitimate link, but actually transferred control of the users' accounts. Though the method was relatively crude compared to later attacks, it highlighted the vulnerability of sites to such exploits.


## Protection Against Clickjacking:

Several strategies effectively protect against clickjacking attacks:

* **X-Frame-Options Header:** This is the most effective defense. Setting this HTTP header to `DENY` prevents your website from being embedded in any iframe. `SAMEORIGIN` allows embedding only from the same domain.

* **Content Security Policy (CSP):**  CSP offers more granular control over embedded content, allowing you to specify which domains are allowed to embed your site within iframes.

* **Framebusting JavaScript:** While less reliable than HTTP headers, this involves adding JavaScript to your site that detects if it's being framed and takes action (e.g., redirecting the user). However, this method can be bypassed.


Clickjacking is a subtle but powerful threat. By understanding how it works and implementing appropriate security measures, both developers and users can significantly reduce their vulnerability to this insidious attack.