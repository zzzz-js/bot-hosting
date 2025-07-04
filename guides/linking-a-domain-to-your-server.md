---
description: >-
  This guide is for running an HTTP server that you want to link your domain to,
  through our reverse proxy.
---

# Linking a domain to your server

To begin, you will need to get your numerical server ID (not to be confused with it's UUID). Your numerical server ID is a number. The easiest way to get this at the moment is on your server's manage server page where you can find the ID in the URL.\


<figure><img src="../.gitbook/assets/domain1.png" alt=""><figcaption><p>Get your server ID in the URL.</p></figcaption></figure>

Ok great, now you have your server ID you simply need to add a CNAME record pointing to `<your server ID>.site.bot-hosting.net`. For example with my ID, 8787, I would point it at `8787.site.bot-hosting.net`.\


<figure><img src="../.gitbook/assets/domain2.png" alt=""><figcaption><p>Example setup with Cloudflare.</p></figcaption></figure>

You can set the name to `@` to use your root domain name without any subdomain.

## Getting a TLS certificate <a href="#getting-a-tls-certificate" id="getting-a-tls-certificate"></a>

{% hint style="info" %}
If you want to be able to visit your site with HTTPS you need a TLS certificate.
{% endhint %}

We recommend you use Cloudflare for getting a TLS certificate, it's free and works great. Firstly if you have not already, you need to move your domain's name servers to Cloudflare by signing up at [https://dash.cloudflare.com](https://dash.cloudflare.com/) and setting it up.

Then you need to setup a CNAME record same as above but this time make sure the `Proxy status` option is checked.\


<figure><img src="../.gitbook/assets/domain3.png" alt=""><figcaption><p>DNS record with proxying enabled.<br></p></figcaption></figure>

But this alone won't work. Since you are now passing the connection through a proxy, we can't figure out what target you're connecting to, so you need to add a `TXT` record as well. This TXT record should contain `bh-server=<your server ID>`.\


<figure><img src="../.gitbook/assets/domain4.png" alt=""><figcaption><p>A TXT record for which server to target.</p></figcaption></figure>

Make sure you have SSL/TLS Encryption Mode set to flexible. Now you should be able to visit your domain through an HTTPS connection in your browser.\


<figure><img src="../.gitbook/assets/domain5.png" alt=""><figcaption></figcaption></figure>
