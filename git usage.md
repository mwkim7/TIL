### local file을 github repository에 새로운 branch로 올리기
```shell
git init
git add .
git commit -m "created a new branch"
git remote origin ~
git remote update

# github 사이트에서 issue 생성

git checkout -b issue-x
git push origin issue-x
```

### 새로운 branch를 dev branch로 merge하기
```shell
git pull origin --rebase dev

# conflict 해결 (모두 accept coming in 선택)

git add .
git rebase --continue

# github 사이트에서 issue-x branch 삭제
# (git push origin issue-x)

# dev <- issue-x 로 pull request
# merge 하면 완료
```
