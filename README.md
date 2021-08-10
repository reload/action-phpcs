# action-phpcs
A GitHub action that runs a phpcs and reports the result to reviewdog

# Prerequisites
* Composer install has been executed
* Phpcs is install by composer and available in the composer config bin-dir
* The code styles used by phpcs are installed and confgured in phpcs.xml

# Usage
Add a workflow step with the action:

```yaml
steps:
  - name: Run phpcs
    uses: reload/poc-phpcs-reviewdog-action@<VERSION>
    with:
      reviewdog_token: ${{ secrets.GITHUB_TOKEN }}`
```

A sub path can be given to the action if the composer.json file is not in the root of the working directory.

Example:

```yaml
steps:
  - name: Run phpcs
    uses: reload/poc-phpcs-reviewdog-action@<VERSION>
    with:
      path: drupal
      reviewdog_token: ${{ secrets.GITHUB_TOKEN }}`
```