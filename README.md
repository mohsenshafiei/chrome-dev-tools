#### chrome-dev-tools

##### Editing

- Color palette
- Scroll to the view in inspection
- Hide and show element with `H` key
- Display computed styles
- Find Event Listeners
- Change color format with `Shift`+`Click`
- Drop-Down DOM elements
- Visualize CSS Specificity
- Break on DOM changes
- Save changes to disk
- Recent selection history with `$n`
- Recent console command with `$_`

##### Debugging

- `Ctrl`+`Shift`+`P` fuzzy search in files
-  `Watch` is really useful when you want to see what is in a variable, function and etc
- With `Call Stack` you can track and find the error easily
- You can use 'Scope' to find what you actually access at the current moment
- You can use `Breakpoints` to manage breakpoints.
- Blackbox script
- Add conditional breakpoints with `Right Click`
- Add XHR breakpoints: just add the `url`

##### Networking

- In networking `Initiator` is really useful
- Color codes are really important

> `White` - Queuing:
> A  Request being queued indicates that
>  - the request was postponed by the rendering engine because it is
>   considered lower priority than critical resources. This often happens with images
>  - The request was put on hold to wait for unavailable TCP socket that's about to free up.
> - The request was put on hold because the browser only allow `six TCP Connections` per origin on HTTP1.
> - Time spent making disk cache entries.


> `Gray` - Stalled/Blocking
> - Time the request spent waiting before it could be sent. It can be waiting for any of the other reasons described for Queuing. Additionally, this time is inclusive of any time spent in proxy negotiation.


> `Light Gray` - Proxy Negotiation
> - Time spent negotiating with a proxy server connection.

> `Dark Blue` - DNS Lookup
> - Time spent performing the DNS lookup. Every new domain on a page requires a full round trip to do in the DNS lookup.

> `Orange` - Initial Connection
> - Time it took to establish a connection, including TCP handshakes/retires and negotiating SSL.

> `Brown` - SSL
> - Time spent completing a SSL handshake.

> `Green` - Request Sent / Sending
> - Time spent issuing the network request. Typically a fraction of a millisecond.

> `Green` - Waiting
> - Time spent waiting for the initial scope, also known as the Time To First Byte. This time captures the latency of a round trip to the server in addition to the time spent waiting for the server to deliver the response.

> `Blue` - Content Download / Downloading
- Time spent receiving the response data

- With getting screen shots you can see every repainting that happens in chrome.
- Using filter in chrome network is really handy (exp: larger than: 200B)


##### Auditing
  - [webpagetest.org](webpagetest.org)
  - lighthouse
  - [sonarwhal.com](sonarwhal.com)

##### Debugging Node.js
  - use `node --inspect index.js` to active node.js debugging in chrome

##### Performance API
  - put performance.mark inside the code to achieve information how much it takes to render on user monitor

##### Image performance
  - use `srcset` to querying by the size

##### Page Jank
  - you can track rendering with `paint flashing`

##### Memory Leaks
> common causes of memory leaks in JavaScript
>  - The accidental global
>  - The forgotten timer
>  - The DOM and not the DOM

- You can use `task manager` to find memory leaks
- You can also use memory snapshot to follow memory leaking
