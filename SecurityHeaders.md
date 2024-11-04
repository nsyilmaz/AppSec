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

## CSP
<table>
    <thead>
        <tr>
            <th>Header</th>
            <th>Desc</th>
            <th colspan=2>Usage</th>
            <th>aaaaaaaa</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>X-Frame-Options</td>
            <td rowspan=3>Hede</td>
            <td>X-Frame-Options: DENY</td>
            <td></td>
            <td>Optimal</td>
        </tr>
        <tr>
            <td>X-Frame-Options: SAMEORIGIN</td>
            <td>&lt;2.59</td>
            <td>Optimal</td>
        </tr>
        <tr>
            <td>X-Frame-Options: ALLOW-FROM origin</td>
            <td>&lt;2.59</td>
            <td>Optimal</td>
        </tr>
    </tbody>
</table>
