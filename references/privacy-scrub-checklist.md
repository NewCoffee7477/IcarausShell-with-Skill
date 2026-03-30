# Privacy Scrub Checklist

Use this checklist before publishing or sharing the project.

## Remove or Replace

- Personal names that identify a specific operator
- Usernames, account handles, or email addresses
- Absolute home-directory paths such as `/Users/example/...`
- Machine names, hostnames, device labels, or local mount names
- Connector IDs, plugin instance IDs, or app-specific opaque identifiers
- Workspace-specific paths, folder names, or repo names copied from another environment
- Real customer, vendor, or organization data unless explicitly intended for publication

## Safe Replacements

- Use neutral names such as `example-user`, `example-org`, or `sample-project`
- Use repo-relative paths such as `references/policy.md`
- Use placeholders such as `<PROJECT_NAME>` or `<TARGET_PATH>`
- Use sanitized examples that describe structure instead of reproducing live content

## Verification Searches

Search for high-risk leakage patterns before delivery:

- `/Users/`
- `C:\\Users\\`
- `@`
- `token`
- `apikey`
- `secret`
- `connector`
- `plugin://`
- `app://`

Add project-specific search terms when the source material includes known internal names or system labels.

## Release Gate

The project is not ready to publish if any file still contains local-only identifiers that are unnecessary for a portable consumer.
