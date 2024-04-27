---
layout: post
title:  "Vscode Jupyter Scala Almond"
date:   2023-10-08 21:01:25 +0900
categories: ml-tools
---

## VSCode Jupyter Scala Almond 설치 히스토리

### Visual studio code 에 python, jupyter extension 설치
python 이나 jupyter extension 을 설치할 때 크게 이슈는 없었고, venv 설정까지 어렵지 않게 할 수 있었음.

### Almond 설치
[Almond 문서](https://almond.sh/docs/quick-start-install)를 따라서 진행

* java 1.8 환경 준비, JAVA_HOME 셋팅

```bash
# 이 경로는 brew 를 이용해 설치한 경로
> export JAVA_HOME=/Library/Java/JavaVirtualMachines/temurin-8.jdk/Contents/Home
```

* coursier( 아마도 프랑스어 코지에)를 통해 almond 설치.

```bash
> brew install coursier
> coursier launch --fork almond --scala 2.12 -- --install
Installed scala kernel under /Users/whishaw/Library/Jupyter/kernels/scala
```

* 설치하고 나면 vscode, jupyter notebook 설정에서, kernel 에 scala 가 추가된 것을 확인할 수 있음.

  ![scala kernel 선택 01](/assets/img/2024-02-18-01.png)

  ![scala kernel 선택 02](/assets/img/2024-02-18-02.png)

  ![scala kernel 선택 03](/assets/img/2024-02-18-03.png)


### Spark 사용해보기
[Almond 문서](https://almond.sh/docs/usage-spark)를 따라서 진행