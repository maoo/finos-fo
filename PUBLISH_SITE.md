# Publishing Docusaurus website

The [main.workflow](.github/workflows/main.workflow) file defines a GitHub Action that automatically builds the Docusaurus website after any commit.

## Configure the action
1. Create an SSH key, using `ssh-keygen -t rsa -b 4096 -C <your email address>` ; make sure to define a new file name, to avoid overriding existing local keys
2. Copy the contents of the newly created public (`.pub`) key, ie `cat ~/.ssh/docusaurus_action_rsa.pub`
3. Create a new GitHub Deploy key via `Settings > Deploy keys > Add deploy key` and paste the `.pub` key contents
4. Create a new GitHub Secret key called `DEPLOY_SSH_KEY` via `Settings > Secrets > Add a new secret` and paste the `.pub` key contents
5. Copy the `main.yml` contents, into the `.github/workflows` repo folder; make sure to update the GitHub repository name, look for `PROJECT_NAME`
6. Commit and push changes
7. Check 