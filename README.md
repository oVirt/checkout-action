# GitHub Action: Checkout the oVirt way

Right now, it's a very thin wrapper around https://github.com/actions/checkout, passing `ref: ${{ github.event.pull_request.head.sha }}`.

The intention is for all oVirt projects to use it, so that those that build RPMs or some other artifacts and include the git hash in the artifacts' names, will get the hash of the commit they test, instead of a temporary merge commit.

Usage:
```
- uses: ovirt/checkout-action@main
```
