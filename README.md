[!IMPORTANT]
**Notice:**
Starting from Kubewarden release 1.32.0, all code from this repository has been merged into [github.com/kubewarden/policies](https://github.com/kubewarden/policies), which is now a monorepo containing policies.
Please refer to that repository for future updates and development.
**This repository is now archived. Development continues in the new location.**


[![Kubewarden Policy Repository](https://github.com/kubewarden/community/blob/main/badges/kubewarden-policies.svg)](https://github.com/kubewarden/community/blob/main/REPOSITORIES.md#policy-scope)
[![Stable](https://img.shields.io/badge/status-stable-brightgreen?style=for-the-badge)](https://github.com/kubewarden/community/blob/main/REPOSITORIES.md#stable)

# Kubewarden policy raw-validation-policy

## Description

This is a waPC test policy that validates raw requests.

The policy accepts requests in the following format:

```json
{
  "request": {
    "user": "tonio"
    "action": "eats",
    "resource": "hay",
  }
}
```

and validates that:

- `user` is in the list of valid users
- `action` is in the list of valid actions
- `resource` is in the list of valid resources

## Settings

This policy has configurable settings:

- `validUsers`: a list of valid users. Cannot be empty.
- `validActions`: a list of valid actions.Cannot be empty.
- `validResources`: a list of valid resources. Cannot be empty.
