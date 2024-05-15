# Exercise 3 - Publish a site using GitHub Actions workflows

- Go to your `hello-world` repository > Settings > Pages > Build and deployment.

- Under Source, select GitHub Actions.

- Click Configure on the `Static HTML` starter workflow

- After the line `uses: actions/configure-pages@v5`, add the following step:
   ```yaml
      - name: Generate index.html
        run: |
          echo '<html><head><title>Built with Actions</title></head><body>' > index.html
          cat README.md >> index.html
          echo '</body></html>' >> index.html
   ```
- Commit the new `.github/workflows/static.yml` file.

- Wait a while for the actions workflow to build and deploy the new site.

- Access `https://<user>.github.io/hello-world` and it should display "Hello World"

- Update README.md and push the changes upstream. Wait a while and `https://<user>.github.io/hello-world` should display the new content.

- Additional starter workflows: `https://github.com/<OWNER>/<REPO>/actions/new?category=pages`.

- Reference: https://docs.github.com/en/enterprise-cloud@latest/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages

[Prev](Page10.md) | [Next](Page12.md)