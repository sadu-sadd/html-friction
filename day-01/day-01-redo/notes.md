## Exercise A
- ``` <p>Hi <strong>there</strong><br>friend<img src="a.png" alt="A cat"></p> ```
- It has 6 tags and 4 elements
- Tags are the individual markup labels used to construct code while elements are complete componenet including openeing tag, content and closing tag
- Void elements are the once with no closing tag like ``` <br> <img> <input>```

## Exercise B
- Browsers collapse sequences of whitespace (spaces, tabs, newlines) into a single space by default so that authors can freely format and indent source code for human readability without that formatting affecting the rendered output.
- The white-space: pre style will preserve the extra spaces and tabs

## Exercise C
- the mistakes in `recovery.html` was rendered by browser as below
```
<p> this is a paragraph </p>
<h2> this is a heading </h2>
<p></p>
<div>div tag inside p tag</div>
<p></p>
<strong><em>wrong syntax</em></strong>
```
- error for closing p tag was resolved 
- div tag which was inside p was moved out by creating new closing tag p and opening tag p
- strong and em tag closing order was corrected

## Exercise D
- The role for div is generic and it has name ""
- The role for button is button with name "Save"
- For keyboard user a real button is focusable by default and activates on Enter or Space. A div is not in the tab order unless you add `tabindex="0"`, and it does not respond to Enter/Space unless you write that yourself.
- For screen readers a button has an implicit `role="button"`, is announced as a button, and gets an accessible name from its content. A div is generic (or “group”), not announced as interactive, and does not automatically expose its text as a name in the same way.

## Exercise E
- URL parsing: Browser splits scheme (https), host, path, query, fragment.
- DNS resolution: Browser/OS cache -> recursive resolver -> root nameservers -> TLD nameservers -> authoritative nameserver for the domain, which returns the IP (A/AAAA record).
- TCP handshake: 3-way SYN / SYN-ACK / ACK to establish a reliable connection to the IP (port 443).
- TLS handshake: ClientHello / ServerHello, certificate verification (chain to a trusted root, hostname match, validity), key exchange, and establishment of the encrypted session. Only after this does application data flow.
- HTTP request: Browser sends GET (with headers, cookies, Accept, etc.) over the TLS tunnel.
- Server response: HTML (plus headers such as Content-Type, Cache-Control, etc.). Redirects or other status codes may intervene.
- HTML parsing -> DOM: Incremental tokenization and tree construction. Script tags block further parsing until fetched and executed (unless async/defer/type=module changes this).
- Resource discovery & fetching: CSS, JS, images, fonts, etc. are requested (often in parallel; preconnect/preload help). Each may trigger its own DNS/TCP/TLS if on a different origin.
- CSS parsing -> CSSOM: Style sheets are turned into the CSS Object Model.
- Render tree: DOM + CSSOM combined; only visible, styled elements are included.
- JavaScript: Runs on the main thread (or workers). It can mutate the DOM/CSSOM at any time after parsing, forcing further style/layout/paint work.