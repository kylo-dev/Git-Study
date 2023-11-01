## Branch

소프트웨어를 개발할 때, 개발자들간에 동일한 소스 코드를 함께 공유하고 서로 다른 작업을 할 때 사용합니다.

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/eccd4ff3-b8d7-42a4-99ff-76dc655d426b)


#### 1. 브랜치 생성
```bash
 git branch step1
```

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/bc3a4757-f7a8-4de2-8353-51043f480a1e)

'step1' 이라는 브랜치가 생성되었지만 ,현재 위치는 아직 main이므로 생성한 브랜치로 이동해야 합니다.

#### 2. 브랜치 이동
```bash
git switch step1
```

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/7c7293e1-8522-4155-bbee-b01c0128b666)

main 브랜치에서 step1 브랜치로 이동합니다.

#### 3. 브랜치에서 커밋하기
```bash
git commit
```

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/d95312bb-d9ef-48da-828e-98b5a9cace55)

#### 4. 브랜치 작업 내역 합치기 (Merge)
```bash
git switch step1
git merge bugFix
```

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/61ba3085-771a-43e9-a177-824301005406)

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/eed3a899-d395-4161-88e1-df907a383ae1)


```bash
git switch bugFix
git merge step1
```

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/75e5af2c-c936-4388-8dea-ac02f43cb8a4)

bugFix 브랜치의 위치도 옮겨줍니다.

#### 4.2 브랜치 작업 내역 합치기 (Rebase)
```bash
git switch bugFix
git rebase step1
```

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/91ead461-502b-42a6-8846-1ac240ff1467)

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/6f9a0f28-288b-4aad-a93b-96bf6c960dd3)


#### 5. 최근 커밋을 가리키는 HEAD

![image](https://github.com/kylo-dev/Git-Study/assets/103489352/efe2f7a9-74ed-4f72-b242-d54c41103db0)

```
git switch HEAD^
```
* '^'은 현재 커밋 시점에서 이전 단계로 이동합니다.

* '~n'은 현재 커밋 시점에서 n만큼의 이전 단계로 이동합니다.
