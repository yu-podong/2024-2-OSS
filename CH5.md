# CH5 커맨드 박스 수정

## 3번
### 수정 전
```
opensw@tux:~$ mkdir ex
opensw@tux:~$ ls-ld ex/
drwxrwxr-x 2 opensw opensw 4096 Sep 27 11:05 ex/
opensw@tux:~$ < Your Commands Here >
opensw@tux:~$ cd ex-bash: cd: ex: Permission denied
opensw@tux:~$
```

### 수정 후
```
opensw@tux:~$ mkdir ex
opensw@tux:~$ ls -ld ex/
drwxrwxr-x 2 opensw opensw 4096 Sep 27 11:05 ex/
opensw@tux:~$ < Your Commands Here >
opensw@tux:~$ cd ex
-bash: cd: ex: Permission denied
opensw@tux:~$
```

## 4번
### 수정 전
```
opensw@tux:~$ ls-al chmodtest---x-w-r-- 1 
opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$ 
```

### 수정 후
```
opensw@tux:~$ ls -al chmodtest
---x-w-r-- 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$ 
```

## 5번
### 수정 전
```
opensw@tux:~$ touch myfile
opensw@tux:~$ ls-al
----r---w- 1 opensw opensw 0 Sep 27 11:23 myfile
opensw@tux:~$
```

### 수정 후
```
opensw@tux:~$ touch myfile
opensw@tux:~$ ls -al 
----r---w- 1 opensw opensw 0 Sep 27 11:23 myfile
opensw@tux:~$
```

## 6번
### 수정 전
```
opensw@tux:~$ ls-al chmodtest
---x-w-r-- 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
opensw@tux:~$ Your Commands
opensw@tux:~$ ls-al chmodtest
---x-wSr-- 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
opensw@tux:~$ Your Commands
opensw@tux:~$ ls-al chmodtest
---x-w-r-T 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
opensw@tux:~$ Your Commands
opensw@tux:~$ ls-al chmodtest
---s-w-r-- 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
```

### 수정 후
```
opensw@tux:~$ ls -al chmodtest
---x-w-r-- 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
opensw@tux:~$ Your Commands
opensw@tux:~$ ls -al chmodtest
---x-wSr-- 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
opensw@tux:~$ Your Commands
opensw@tux:~$ ls -al chmodtest
---x-w-r-T 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
opensw@tux:~$ Your Commands
opensw@tux:~$ ls -al chmodtest
---s-w-r-- 1 opensw opensw 0 Sep 27 11:10 chmodtest
opensw@tux:~$
```
