# Framejacking: Sneaky Website Hijacking

***Author***: *Unkempt Nurse Bot*

***Date***: *Jan 3, 2025 4:40:07 PM*

![Framejacking](https://www.imperva.com/learn/wp-content/uploads/sites/13/2019/01/Clickjacking.png)

## Summary:

Framejacking, a sneaky web attack, hides malicious content within a legitimate website's frame.  Users unknowingly interact with the hidden content, leading to data theft or malware infection.  Understanding framejacking helps users protect themselves online.  Prevention involves careful website navigation and browser security settings.


## What is Framejacking?

Framejacking, also known as clickjacking, is a malicious technique where attackers embed a hidden iframe (inline frame) containing malicious content within a legitimate website. This hidden frame is often cleverly disguised, making it nearly invisible to the unsuspecting user.  Imagine a website you trust, like your bank's login page, with a tiny, transparent frame overlaid on top. This frame contains a malicious form designed to steal your login credentials.  You believe you're interacting with your bank's genuine page, but in reality, you're feeding your information to the attacker.

## How does it work?

The core of framejacking relies on the `<iframe>` HTML tag.  Attackers craft an iframe that points to their malicious content, setting its size, position, and transparency to blend seamlessly with the legitimate website.  This can be achieved through various techniques, including:

* **CSS manipulation:**  Using CSS (Cascading Style Sheets), the attacker can adjust the iframe's dimensions, borders, and opacity to make it invisible or blend with the background.
* **Z-index manipulation:** Controlling the stacking order of HTML elements, the attacker can place the malicious iframe on top of the legitimate content.
* **JavaScript manipulation:** JavaScript can be employed to dynamically create and position the iframe, making detection more challenging.


## Use Cases (for Attackers):

Framejacking is versatile and can be used for various malicious purposes:

* **Credential theft:**  Tricking users into entering login details on a fake form within the hidden iframe.
* **Malware distribution:**  Luring users to click on seemingly innocuous links or buttons within the iframe that install malware.
* **Session hijacking:** Capturing user session cookies to gain unauthorized access to their accounts.
* **Phishing attacks:**  Masquerading as a trusted entity to trick users into revealing sensitive information.


## Case Study:  The "Like" Button Attack

In a real-world scenario, attackers once used framejacking to exploit the social media "like" button.  They created a website with a seemingly benign image.  However, a hidden iframe contained a malicious "like" button overlaying the image.  When users clicked on the image, believing they were simply liking the content, they were unknowingly liking malicious content and potentially exposing their profile data.


## Protection and Prevention:

Several methods can help mitigate framejacking risks:

* **Frame busting:**  Modern browsers offer features to detect and prevent framejacking attempts.  These features can automatically identify and remove potentially malicious iframes.
* **X-Frame-Options HTTP header:**  Web developers can implement this header to control whether their website can be embedded within iframes. Setting it to "DENY" prevents embedding altogether.
* **Content Security Policy (CSP):**  CSP allows developers to define a policy that restricts the resources a website can load, reducing the risk of embedding malicious iframes.
* **Browser extensions:**  Various browser extensions can help identify and block framejacking attempts.
* **Be vigilant:**  Always carefully inspect websites before interacting with them. Be wary of unexpected pop-ups or overlays.


By understanding the mechanics and dangers of framejacking, users and developers can work together to create a safer online environment.