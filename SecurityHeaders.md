# HTTP Security Headers
## X-Frame-Options
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>X-Frame-Options</td>
            <td rowspan=3>Web</td>
            <td rowspan=3>The X-Frame-Options HTTP response header can be used to indicate whether a browser should be allowed to render a page in a <frame>, <iframe>, <embed> or <object>. Sites can use this to avoid click-jacking attacks, by ensuring that their content is not embedded into other sites.</td>
            <td>X-Frame-Options: DENY</td>
            <td>No rendering within a frame.</td>
        </tr>
        <tr>
            <td>X-Frame-Options: SAMEORIGIN</td>
            <td>No rendering if origin mismatch.</td>
        </tr>
        <tr>
            <td>X-Frame-Options: ALLOW-FROM origin</td>
            <td>This is an obsolete directive. Modern browsers that encounter response headers with this directive will ignore the header completely. The Content-Security-Policy HTTP header has a frame-ancestors directive which you should use instead.</td>
        </tr>
        <tr>
            <td colspan=5> 
                <li>https://owasp.org/www-project-secure-headers/#x-frame-options</li>
                <li>https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Headers_Cheat_Sheet.html#security-headers</li>
            </td>
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
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=7>Content-Security-Policy</td>
            <td rowspan=7>Web</td>
            <td rowspan=7>Content Security Policy (CSP) is a security feature that is used to specify the origin of content that is allowed to be loaded on a website or in a web applications. It is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross-Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement to distribution of malware.</td>
            <td>Content-Security-Policy: default-src 'self'</td>
            <td>Define loading policy for all resources type in case a resource type’s dedicated directive is not defined (fallback).</td>
        </tr>
        <tr>
            <td>Content-Security-Policy: default-src 'self' www.mydomain.com</td>
            <td>Define loading policy for all resources type in case a resource type’s dedicated directive is not defined (fallback).</td>
        </tr>
        <tr>
            <td>Content-Security-Policy: img-src *;</td>
            <td>Define from where the protected resource can load images.</td>
        </tr>
        <tr>
            <td>Content-Security-Policy: media-src www.mydomain.com;</td>
            <td>Define from where the protected resource can load video and audio.</td>
        </tr>
        <tr>
            <td>Content-Security-Policy: script-src www.mydomain.com;</td>
            <td>Define which scripts the protected resource can execute.</td>
        </tr>
        <tr>
            <td>Content-Security-Policy: frame-ancestors 'self' https://www.example.org;</td>
            <td>Define from where the protected resource can be embedded in frames.</td>
        </tr>
        <tr>
            <td>Content-Security-Policy: frame-ancestors 'self' https://mydomain.com https://example.com;</td>
            <td>Define from where the protected resource can be embedded in frames.</td>
        </tr>
        <tr>
            <td colspan=5>
                <li>https://owasp.org/www-project-secure-headers/#content-security-policy</li>
            </td>
        </tr>
    </tbody>
</table>

<hr>

## X-Content-Type-Options
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>X-Content-Type-Options</td>
            <td>Web</td>
            <td>Setting this header will prevent the browser from interpreting files as a different MIME type to what is specified in the Content-Type HTTP header (e.g. treating text/plain as text/css).</td>
            <td>X-Content-Type-Options: nosniff</td>
            <td>Will prevent the browser from MIME-sniffing a response away from the declared content-type.</td>
        </tr>
        <tr>
            <td colspan=5>
                <li>https://owasp.org/www-project-secure-headers/#x-content-type-options</li>
            </td>
        </tr>
    </tbody>
</table>

<hr>

## Cross-Origin-Resource-Policy
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>Cross-Origin-Resource-Policy</td>
            <td rowspan=3>Web / API / Mobile</td>
            <td rowspan=3>This response header (also named CORP) allows to define a policy that lets web sites and applications opt in to protection against certain requests from other origins (such as those issued with elements like <script> and <img>), to mitigate speculative side-channel attacks.</td>
            <td>Cross-Origin-Resource-Policy: same-site</td>
            <td>Only requests from the same Site can read the resource.</td>
        </tr>
        <tr>
            <td>Cross-Origin-Resource-Policy: same-origin</td>
            <td>Only requests from the same Origin (i.e. scheme + host + port) can read the resource.</td>
        </tr>
        <tr>
            <td>Cross-Origin-Resource-Policy: cross-origin</td>
            <td>Requests from any Origin (both same-site and cross-site) can read the resource. Browsers are using this policy when an CORP header is not specified.</td>
        </tr>
        <tr>
            <td colspan=5>
                <li>https://owasp.org/www-project-secure-headers/#cross-origin-resource-policy</li>
            </td>
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
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=5>Access-Control-*</td>
            <td rowspan=5>Web / API / Mobile</td>
            <td rowspan=5>Cross Origin Resource Sharing (CORS) is a mechanism that enables a web browser to perform cross-domain requests using the XMLHttpRequest (XHR) Level 2 (L2) API in a controlled manner. In the past, the XHR L1 API only allowed requests to be sent within the same origin as it was restricted by the Same Origin Policy (SOP).</td>
            <td>Access-Control-Allow-Origin: https://www.mydomain.com</td>
            <td>indicate which domains are allowed to read the response. Based on the CORS W3 Specification it is up to the client to determine and enforce the restriction of whether the client has access to the response data based on this header.</td>
        </tr>
        <tr>
            <td>Access-Control-Request-Method: POST</td>
            <td>Header is used when a browser performs a preflight OPTIONS request and lets the client indicate the request method of the final request.</td>
        </tr>
        <tr>
            <td>Access-Control-Allow-Method: POST</td>
            <td>Header used by the server to describe the methods the clients are allowed to use.</td>
        </tr>
        <tr>
            <td>Access-Control-Request-Max-Age: 86400</td>
            <td>Header determines the time a preflight request can be cached in the browser.</td>
        </tr>
        <tr>
            <td>Access-Control-Allow-Crerdentials: true</td>
            <td>This response header allows browsers to read the response when credentials are passed. When the header is sent, the web application must set an origin to the value of the Access-Control-Allow-Origin header.</td>
        </tr>
        <tr>
            <td colspan=5>
                <li>https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/11-Client-side_Testing/07-Testing_Cross_Origin_Resource_Sharing</li>
            </td>
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
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>Strict-Transport-Security</td>
            <td rowspan=3>Web / API / Mobile</td>
            <td rowspan=3>HTTP Strict Transport Security (also named HSTS) is a web security policy mechanism which helps to protect websites against protocol downgrade attacks and cookie hijacking. It allows web servers to declare that web browsers (or other complying user agents) should only interact with it using secure HTTPS connections, and never via the insecure HTTP protocol.</td>
            <td>Strict-Transport-Security: max-age=31536000</td>
            <td>The time, in seconds, that the browser should remember that this site is only to be accessed using HTTPS.</td>
        </tr>
        <tr>
            <td>Strict-Transport-Security: max-age=31536000 ; includeSubDomains</td>
            <td>If this optional parameter is specified, this rule applies to all of the site’s subdomains as well.</td>
        </tr>
        <tr>
            <td>Strict-Transport-Security: max-age=31536000 ; includeSubDomains ; preload</td>
            <td>If this optional parameter is specified, its instruct the browser to always access the site using HTTPS because the site is included into Strict-Transport-Security preload list.</td>
        </tr>
        <tr>
            <td colspan=5>
                <li>https://owasp.org/www-project-secure-headers/#strict-transport-security</li>
            </td>
        </tr>
    </tbody>
</table>

<hr>

## Referrer Policy
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>Referrer-Policy</td>
            <td rowspan=3>Web / API / Mobile</td>
            <td rowspan=3>The Referrer-Policy HTTP header governs which referrer information, sent in the Referer header, should be included with requests made.</td>
            <td>Referrer-Policy: no-referrer</td>
            <td>The Referer header will be omitted entirely. No referrer information is sent along with requests.</td>
        </tr>
        <tr>
            <td>Referrer-Policy: same-origin</td>
            <td>A referrer will be sent for same-site origins, but cross-origin requests will contain no referrer information.</td>
        </tr>
        <tr>
            <td>Referrer-Policy: origin-when-cross-origin</td>
            <td>Send a full URL when performing a same-origin request, but only send the origin of the document for other cases.</td>
        </tr>
        <tr>
            <td colspan=5>
                <li>https://owasp.org/www-project-secure-headers/#referrer-policy</li>
            </td>
        </tr>
    </tbody>
</table>

<hr>

## Cache-Control
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Relates</th>
            <th>Desc</th>
            <th>Usage</th>
            <th>Details</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>Cache-Control</td>
            <td rowspan=3>Web / API / Mobile</td>
            <td rowspan=3>This header holds directives (instructions) for caching in both requests and responses. If a given directive is in a request, it does not mean this directive is in the response (source Mozilla MDN). Specify the capability of a resource to be cached is important to prevent exposure of information via the cache.</td>
            <td>Cache-Control: no-store, max-age=0</td>
            <td>The response may not be stored in any cache.</td>
        </tr>
        <tr>
            <td>Cache-Control: must-revalidate</td>
            <td>Indicates that once a resource becomes stale, caches do not use their stale copy without successful validation on the origin server.</td>
        </tr>
        <tr>
            <td>Cache-Control: private</td>
            <td>The response may be stored only by a browser’s cache, even if the response is normally non-cacheable.</td>
        </tr>
        <tr>
            <td colspan=5>
                <li>https://owasp.org/www-project-secure-headers/#cache-control</li>
            </td>
        </tr>
    </tbody>
</table>

