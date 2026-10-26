- classic script opened via `file://` -> 'JS ran!' appeared which means JS script was triggered
- classic script opened via Live Server -> 'JS ran!' appeared which means JS script was triggered
- with `type="module"` added, opened via `file://` -> JS didn't load it gave below error
```
index.html:1 Access to script at 'file:///Users/sadath/Documents/html-friction/day-02/app.js' from origin 'null' has been blocked by CORS policy: Cross origin requests are only supported for protocol schemes: chrome, chrome-experimental-site-token-provider, chrome-extension, chrome-untrusted, data, http, https, isolated-app.
app.js:1  Failed to load resource: net::ERR_FAILED
```
- with `type="module"` added, opened via Live server -> 'JS ran!' appeared which means JS script was triggered