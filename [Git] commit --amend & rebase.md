# 커밋 메시지 변경

[Git 공식 사이트](https://docs.github.com/ko/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/changing-a-commit-message)

- 커밋 메시지에 잘못된 정보나 수정을 필요로 할 때 아래 명령어를 통해 변경할 수 있습니다.


## 가장 최근 커밋 메시지 변경하기
```bash
git commit --amend
```
위 명령어를 사용하여 가장 최근의 커밋 메시지를 변경할 수 있습니다.

## 이전의 여러 커밋 메시지 변경하기
```bash
git rebase -i HEAD~n
```
마지막 n개 커밋의 목록("변경하고 싶은 커밋의 개수")을 수정하기 위해서는 위 명령어를 사용합니다.

## 커밋 메시지를 이전에 Push한 경우

위의 명령어를 통해 커밋 메시지를 수정한 후에

```bash
git push --force origin "브랜치명"
```
위 강제 push를 통해 변경이 이루어집니다.

git push --force는 강제로 push하여 git commit 내용을 변경하므로 협업하는데에 있어서 최대한 지양해야 합니다.
되도록 push를 하기 전에 커밋 메시지를 한 번 더 확인하는 것이 좋습니다.
