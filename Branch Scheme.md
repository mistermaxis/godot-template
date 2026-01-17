# Branches

| Name    | Description             | Merge                                        | Trigger                               | Release                                                      |
| ------- | ----------------------- | -------------------------------------------- | ------------------------------------- | ------------------------------------------------------------ |
| Main    | Stable branch           | From `beta`, `feature` or `patch` branches   | `major`, `minor` and `patch`  updates | Include no suffix (`v1.0.0`)                                 |
| Beta    | Unstable/testing branch | From `alpha`, `feature` or `patch` branches. | `minor` and `patch` updates           | Include beta suffix (`v1.3.0-beta`)                          |
| Alpha   | Prototype branch        | From `feature` and `patch` branches          | `minor` and `patch` updates           | Include alpha suffix (`v0.4.9-alpha`)                        |
| Feature | Feature branches        | Into `alpha`, `beta` or `main` branches      | `minor` updates                       | Include alpha, beta, or no suffix (`v0.5.0-alpha`, `v0.4.0-beta`, `v1.3.0`) |
| Patch   | Patch branches          | into `alpha`, `beta` or `main` branches      | `patch` updates                       | Include alpha, beta, or no suffix (`v0.5.5-alpha`, `v0.4.9-beta`, `v1.2.3`) |