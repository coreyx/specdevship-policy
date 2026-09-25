# SpecDevShip policy documents

The Terms & Conditions (`terms.md`) and Privacy Policy (`privacy.md`) for SpecDevShip. The website pulls this repository into its own and builds these files into its terms and privacy pages at <https://specdevship.com>.

## Editing

- **Never write email addresses here.** This repository is public. Use a placeholder instead, which the website fills in when it's built:
  - `{{ POLICY_EMAIL }}`: questions about the terms
  - `{{ PRIVACY_EMAIL }}`: privacy requests
  - `{{ BILLING_EMAIL }}`: billing problems

  A new placeholder has to be set up on the website first, or its build fails; see "Policy documents" in the website's README.
- **Commit with your GitHub no-reply address,** since commit author emails are public. This repository is set up to use it: `git config user.email` should show the `users.noreply.github.com` address.
- **Update "Last updated"** at the top of a document whenever its content changes.
- **Plain Markdown only.** The website renders headings, lists, bold, italics and links.

## Publishing a change

1. Commit and push here.
2. In the website repository, pull the change in with `git subtree pull --prefix=content/policy policy main --squash` (or the VS Code task **Pull policy docs**), then push the website to deploy it.

Edits made directly in the website's copy would be overwritten or conflict on the next pull, so always edit here.
