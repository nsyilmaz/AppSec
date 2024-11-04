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
