# Branches Names

| Name    | Description             | Merge                                        | Trigger                               | Release                                                      |
| ------- | ----------------------- | -------------------------------------------- | ------------------------------------- | ------------------------------------------------------------ |
| Main    | Stable branch           | From `beta`, `feature` or `patch` branches   | `major`, `minor` and `patch`  updates | Include no suffix (`v1.0.0`)                                 |
| Beta    | Unstable/testing branch | From `alpha`, `feature` or `patch` branches. | `minor` and `patch` updates           | Include beta suffix (`v1.3.0-beta`)                          |
| Alpha   | Prototype branch        | From `feature` and `patch` branches          | `minor` and `patch` updates           | Include alpha suffix (`v0.4.9-alpha`)                        |
| Feature | Feature branches        | Into `alpha`, `beta` or `main` branches      | `minor` updates                       | Include alpha, beta, or no suffix (`v0.5.0-alpha`, `v0.4.0-beta`, `v1.3.0`) |
| Patch   | Patch branches          | into `alpha`, `beta` or `main` branches      | `patch` updates                       | Include alpha, beta, or no suffix (`v0.5.5-alpha`, `v0.4.9-beta`, `v1.2.3`) |

## Branch naming convention

### Releases are automatically created based on your branch naming convention in pull requests

- **Source Branch:** Any branch where you are developing features

- **Target Branch:** The branch against which you are merging

> Note: You'll find compiled binaries in the Releases section of the repository after a successful build

## How releases are created based on source and target branch names

### When you merge a pull request, depending on the name of the branch you are working on and the branch you are pulling against, a different release will be created

| Source Branch | Target Branch | Description                                                  | Example                          |
| ------------- | ------------- | ------------------------------------------------------------ | -------------------------------- |
| `patch/*`     | `alpha`       | Triggers a **patch** update and adds or keeps the **alpha** suffix | `v0.2.3-alpha` -> `v0.2.4-alpha` |
| `feat/*`      | `alpha`       | Triggers a **minor** update and adds or keeps the **alpha** suffix | `v0.2.3-alpha` -> `v0.3.0-alpha` |
| `alpha`       | `beta`        | Does **not** trigger a version update. Changes suffix from **alpha** to **beta** | `v0.8.2-alpha` -> `v0.8.2-beta`  |
| `patch/*`     | `beta`        | Triggers a **patch** update and adds or keeps the **beta** suffix | `v0.3.4-beta` -> `v0.4.0-beta`   |
| `feat/*`      | `beta`        | Triggers a **minor** update and adds or keeps the **beta** suffix | `v0.7.7-beta` -> `v0.8.0-beta`   |
| `beta`        | `main`        | Triggers a **major** update and removes **beta** suffix      | `v1.2.3-beta` -> `v2.0.0`        |
| `patch/*`     | `main`        | Triggers a **patch** update, does **not** modify the suffix  | `v1.2.3` -> `v1.2.4`             |
| `feat/*`      | `main`        | Triggers a **minor** update, does **not** modify the suffix  | `v1.2.3` -> `v1.3.0`             |

> **Note:** If the latest version is a stable version (without a suffix) and a feat/ or patch/ branch is merged to alpha or beta branch, the update will append said suffix to the version. Eg: merging `feat/feature1` into  `beta` when the latest version is `v1.0.0` will create the tag `v1.1.0-beta`
