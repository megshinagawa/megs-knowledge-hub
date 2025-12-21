# Security Guide

This guide aims to clarify the security rules of this repository.

## What NOT to Commit

Note that this is not an exhaustive list.

- [ ] Passwords
- [ ] API keys
- [ ] Location information (address)
- [ ] Contact infromation (phone number, email, etc.)
- [ ] Confidential information
- [ ] Personal entries

## If You Accidentally Commit Sensitive Data

**Don't just delete it** - Git history preserves it.

```bash
# 1. Remove the commit from Git history
git filter-branch --force --index-filter \
"git rm --cached --ignore-unmatch PATH-TO-FILE" \
--prune-empty --tag-name-filter cat -- --all

# 2. Force push (if already pushed)
git push origin --force --all
```
