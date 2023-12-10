---
title: "mac에서 MySQL 설치하기"
excerpt: "mac에서 MySQL 설치해보았다."

categories:
  - cs
tags:
  - DB
  - 데이터베이스
---

# Mac OS에서 MySQL 설치하기

Homebrew를 통해서 MySQL 설치하는 방법입니다.  
저는 제로초님의 서적(Node.js 교과서)을 참고했고,  
터미널에서 진행하면 됩니다.

### MySQL 설치 및 시작

```
$ brew install mysql
$ brew services start mysql
$ mysql_secure_installation
```

위 과정을 거치고 나면 여러가지 설정을 하겠냐고 합니다.  
<br/>

- Would you like to setup VALIDATE PASSWORD component?  
  비밀번호 설정을 하겠냐는 것입니다.  
  저는 보안을 위해 yes 하고, Medium으로 설정했습니다.

- Remove anonymous users? (Press y|Y for Yes, any other key for No)  
  익명 사용자를 제거할지를 묻는 옵션입니다.
  y를 설정하시면 접속할 때마다 u 옵션을 명시해야 합니다.  
  저는 y 설정했습니다.

- Disallow root login remotely? (Press y|Y for Yes, any other key for No)  
  원격접속 가능 여부를 묻는 것인데,  
  질문이 "root login 원격으로 허용 불가?" 이므로  
  저는 원격접속 원해서 n 설정했습니다.

- Remove test database and access to it? (Press y|Y for Yes, any other key for No)  
  저는 db에 테스트 데이터베이스가 있으면 은근 유용한 것 같아서 y 해줬습니다.
- Reload privilege tables now? (Press y|Y for Yes, any other key for No)
  직역하면,  
  "지금 권한 테이블을 reload 하겠니?" 입니다.  
  인터넷 찾아보니 권한을 변경했을 경우 y 하는 것이라고들 하셔서,  
  저는 n 했습니다.

### MySQL 접속하기

이제 설치가 끝났으므로 접속하면 됩니다.
접속은 아래와 같이 터미널에 입력하고, 비밀번호 입력하면 됩니다.

```
$ mysql -h localhost -u root -p
```

### MySQL 종료하기

```
$ mysql> exit
```
