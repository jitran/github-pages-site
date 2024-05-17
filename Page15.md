# Using custom domains for your GitHub Pages site

- Go to your repository > Settings > Pages > Custom domain and type in your custom domain.

- For apex domains such as example.com, configure an ALIAS, ANAME, or A record with your DNS provider.
   ```
   # A
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153

   # AAAA
   2606:50c0:8000::153
   2606:50c0:8001::153
   2606:50c0:8002::153
   2606:50c0:8003::153

   # ALIAS or ANAME
   <username>.github.io or <organisation>.github.io
   ```

- For subdomains such as www.example.com, configure a CNAME record with your DNS provider.
   ```
   # CNAME
   <username>.github.io or <organisation>.github.io or <some-thing-uuid>.pages.github.io
   ```

- Note: For EMU, `<organisation>.github.io` sites are not available. You will need to configure individual CNAME records for each GitHub Pages generated domain, i.e. `custom-domain` > `some-thing-uuid.pages.github.io`.

- Reference: https://docs.github.com/en/enterprise-cloud@latest/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

[Prev](Page14.md) | [Next](Page16.md)