
This can be updated as much as you want and it should be added to the path → `.git/hooks/commit_msg` or you can investigate how to add it.

```sh
#!/bin/bash

# Get the commit message
commit_msg=$(cat $1)

pattern='^(build|notes|chore|ci|docs|feat|fix|perf|refactor|revert|style|test)(\([a-z]+\))?!?: .+$'

# test if the commit message matches the pattern
# Test if the commit message matches the pattern
if ! [[ $commit_msg =~ $pattern ]]; then
  echo "ERROR: The commit message does not match the Conventional Commits format."
  echo "       Please use the format: type(scope)?: subject"
  echo "       Example: feat(users): add new user endpoint"
  echo "       Keep in mind the following pattern: build|notes|chore|ci|docs|feat|fix|perf|refactor|revert|style|test"
  echo "       See https://www.conventionalcommits.org/en/v1.0.0/#summary for more information"
  exit 1
fi

echo "SUCCESS, you commit looks good ✅"

# if the commit message matches the pattern, exit
exit 0
```