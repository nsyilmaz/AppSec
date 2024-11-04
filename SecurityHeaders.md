# HTTP Security Headers
## X-Frame-Options
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th colspan=2>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>X-Frame-Options</td>
            <td rowspan=3>Web</td>
            <td rowspan=3>The X-Frame-Options HTTP response header can be used to indicate whether a browser should be allowed to render a page in a <frame>, <iframe>, <embed> or <object>. Sites can use this to avoid click-jacking attacks, by ensuring that their content is not embedded into other sites.</td>
            <td>X-Frame-Options: DENY</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>X-Frame-Options: SAMEORIGIN</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>X-Frame-Options: ALLOW-FROM origin</td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>

<hr>

## CSP (Content Security Policy)
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th colspan=2>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>Content-Security-Policy</td>
            <td rowspan=3>Web</td>
            <td rowspan=3>Content Security Policy (CSP) is a security feature that is used to specify the origin of content that is allowed to be loaded on a website or in a web applications. It is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross-Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement to distribution of malware.</td>
            <td>Content-Security-Policy: default-src 'self'</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Content-Security-Policy: default-src 'self' www.mydomain.com</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Content-Security-Policy: default-src 'self' www.mydomain.com; img-src *; media-src www.mydomain.com; script-src www.mydomain.com</td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>

<hr>

## CORS (Cross Origin Resource Sharing)
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th colspan=2>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=5>Access-Control-*</td>
            <td rowspan=5>Web / API / Mobile</td>
            <td rowspan=5>Cross Origin Resource Sharing (CORS) is a mechanism that enables a web browser to perform cross-domain requests using the XMLHttpRequest (XHR) Level 2 (L2) API in a controlled manner. In the past, the XHR L1 API only allowed requests to be sent within the same origin as it was restricted by the Same Origin Policy (SOP).</td>
            <td>Access-Control-Allow-Origin: https://www.mydomain.com</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Access-Control-Request-Method: POST</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Access-Control-Request-Headers: Content-Type</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Access-Control-Request-Max-Age: 86400</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Access-Control-Allow-Crerdentials: true</td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>

<hr>

## HSTS (HTTP Strict Transport Security)
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th colspan=2>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>Strict-Transport-Security</td>
            <td rowspan=3>Web / API / Mobile</td>
            <td rowspan=3>HTTP Strict Transport Security (also named HSTS) is a web security policy mechanism which helps to protect websites against protocol downgrade attacks and cookie hijacking. It allows web servers to declare that web browsers (or other complying user agents) should only interact with it using secure HTTPS connections, and never via the insecure HTTP protocol.</td>
            <td>Strict-Transport-Security: max-age=31536000</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Strict-Transport-Security: max-age=31536000 ; includeSubDomains</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Strict-Transport-Security: max-age=31536000 ; includeSubDomains ; preload</td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>
