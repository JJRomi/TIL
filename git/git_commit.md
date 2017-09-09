# git commit 관련 사용법
---

```
git commit -m 'commit message'
# git commit

git log
# git commit log

git reflog
# git commit history

git reset --hard HEAD^^
# ^ 갯수만큼 삭제

git reset --hard HEAD~38
# commit number HAED~38까지 삭제

git rebase -i HEAD~3
# commit message(number HAED~3까지) 수정

git commit --amend
# 마지막 commit message 수정
```

# Reference
---
https://backlogtool.com/git-tutorial/kr/stepup/stepup7_3.html
