# InfiniTensor

## Compilation on Lotus
``` bash
# Enter the root of InfiniTensor
source test/script/env_lotus.sh 
mkdir build && cd build
cmake .. && make -j 12
```

## Contributor Guide
InfiniTensor development is based on the pull request on Github. Before requesting for merging, a PR should satisfy the following requirements
1. Pass all tests. 
    1. Currently, CI on Github only checks code format. Script `test/script/clang_format_inplace.sh` is for formatting all code. 
    2. Contributors should run `ctest` manually and copy its output to the PR. Use fenced code blocks (triple backquotes, i.e., `` ``` ``) to avoid referencing in Github. Otherwise, `#` in the output is interpreted as a Github reference. Do not directly paste the ctest output in commit messages either for the same reason.  
2. Receive at least one approval from reviewers. 
3. PR title should be concise since it is going to be the commit message in the main branch after merging and squashing.
