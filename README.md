# httpseverywhere
Go implementation of using [HTTPS Everywhere](https://github.com/EFForg/https-everywhere) rule sets to send traffic over HTTPS. Many thanks to the EFF team maintaining such an amazing project!

Example usage:

```go
import "url"
import "github.com/getlantern/httpseverywhere"

...

httpURL, _ := url.Parse("http://name.com")
rewrite := httpseverywhere.Default()
httpsURL, changed := rewrite(httpURL)
if changed {
	// Redirect to httpsURL
	...
}
```
