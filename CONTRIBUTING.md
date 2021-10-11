# Contributing to Open Public Transport

Here you find guides how to contribute to this repo. Pushing directly to the `main` branch is disabled. Instead you can create a branch for a feature you work on and file a pull request once you are done.

- [Submission Guidelines](#submit)
- [Commit Message Format](#commit)

## <a name="submit"></a> Submission Guidelines

### <a name="submit-pr"></a> Submitting a Pull Request

1. Pick [an existing issue](https://github.com/open-public-transport/open-public-transport-frontend/issues) or [create a new one](https://github.com/open-public-transport/open-public-transport-frontend/issues/new) you can to work on
2. Clone the repo `git clone git@github.com:open-public-transport/open-public-transport-frontend.git`
3. Checkout main branch `git checkout main`
4. Create a branch for your feature and check it out `git checkout -b feature/my-fancy-feature`
5. Implement your changes and commit your changes using a descriptive commit message that follows our [commit message conventions](#commit).
6. Push your branch to GitHub `git push origin feature/my-fancy-feature`
7. In GitHub, create a pull request against the `main` branch

### <a name="review-pr"></a> Review a Pull Request (PR)

1. Pick [a pull request](https://github.com/open-public-transport/open-public-transport-frontend/pulls) you want to review
2. Review the code contained in the pull request
3. (Check out the code locally of necessary)
4. (Add comments if necessary)
5. Approve the pull request if everything looks good to you

Afterwards the requester will integrate the branch into `main` with the strategy _Rebase and Merge_.

## <a name="commit"></a> Commit Message Format

The commit messages must follow [conventional commits guidelines](https://www.conventionalcommits.org/en/v1.0.0/)

```
<type>[optional scope]: <description>
  │       │             │
  │       │             └─⫸ Summary in present tense. Not capitalized. No period at the end.
  │       │
  │       └─⫸ Commit Scope: common|data|story
  │
  └─⫸ Commit Type: feat|fix|docs|refactor
```

The `<type>` and `<summary>` fields are mandatory, the `(<scope>)` field is optional.

##### Type

Must be one of the following:

* **feat**: A new feature
* **fix**: A bug fix
* **docs**: Documentation only changes
* **refactor**: A code change that neither fixes a bug nor adds a feature

##### Scope
The scope should be the name of the npm package affected (as perceived by the person reading the changelog generated from commit messages).

The following is the list of supported scopes:

* `common`
* `data`
* `story`

##### Summary

Use the summary field to provide a succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize the first letter
* no dot (.) at the end
