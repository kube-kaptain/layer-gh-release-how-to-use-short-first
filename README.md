# Layer GH Release How To Use Short First

Kaptain config layer that makes the "How to Consume" section of GitHub release
notes show both reference forms, org-local first.

Projects that reference this layer inherit:

- **`consumerReferenceForms: short-first`**: the release notes lead with the
  short reference (`my-app:[1.2.3]`) and follow it with the fully qualified one
  (`ghcr.io/my-org/my/my-app:[1.2.3]`)

The short form resolves against the consuming project's own target registry and
namespace, so it only works from projects that share them. The full form carries
registry, namespace, prefix and name, and works from any org, registry or
platform.


## When to use this

Reach for this layer when a project is consumed mostly from inside your own org
but is also usable from outside, and you want the in-org reference to be the one
people copy first.
