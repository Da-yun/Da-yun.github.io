---
title: "Welcome to SQL!"
date: 2021-01-26 08:26:28 -0400
categories: DataBase Basic
---

# basic 1 
# my sql 데이터 베이스 선택
+ USE my sql;

# 'db'테이블 구조 확인
+ DESC db;

# 기존에 'board' 데이터베이스가 존재 한다면 삭제
+ DROP DATABASE IF EXISTS board;

# 새 데이터 베이스 생성
+ CREATE DATABASE board;

# 데이터 베이스 선택
+ USE board; 

# 테이블 확인
+ SHOW TABELS;

# 게시물 테이블을 만든다. 제목 내용 컬럼을 추가
+ CREATE TABLE article(
title CHAR(100),
`body` TEXT
);

# 확인
+ SHOW TABLES;

# 데이터 하나 추가하기
+ INSERT INTO article
SET title = 'aaa',
`body = 'bbb';

# 제목 조회
+ SELECT title
FROM article;
# 내용 조회
+ SELECT `body`
FROM article

# 제목, 내용 칼럼 데이터 조회
+ SELECT title, `body`
FROM article;

# 모든 데이터 조회
+ SELECT *
FROM article

# 모든 데이터 id로 내림차순 정렬하기
+ SELECT * 
FROM article
ORDER BY id DESC;

# 모든 데이터 ID, 오른차순 title 내림차순 정렬 조회
+ SELECT *
FROM article
ORDER BY id ASC, title DESC


< 프로그래머스 문제 풀어보기 >
[프로그래머스 59034](https://programmers.co.kr/learn/courses/30/lessons/59034 "모든 레코드 조회하기")
+ 정답 (모든 데이터를 ID 순으로 조회하기)
- SELECT * 
From ANIMAL_INS
ORDER BY ANIMAL_ID ASC

[프로그래머스 59403](https://programmers.co.kr/learn/courses/30/lessons/59403 "동물 아이디와 이름")
+ 정답 (ID와 이름만 선택하여 가져오고 ID 내림차순 순으로 정렬한다)
- SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
ORDER BY ANIMAL_ID ASC

[프로그래머스 59035](https://programmers.co.kr/learn/courses/30/lessons/59035 "역순 정렬하기")
+ 정답 (NAME과 DATATIME만 가져오고 DESC로 역순 정렬)
- SELECT NAME, DATETIME
FROM ANIMAL_INS
ORDER BY ANIMAL_ID DESC

[프로그래머스 59404](https://programmers.co.kr/learn/courses/30/lessons/59404  "여러기준 정렬하기")
+ 정답 (NAME을 기준으로 오름차순 정렬하고 NAME ASC, -> 같다면 DATETIME 기준으로 내림차순 DESC 기준이 되는 정렬을 먼저 써주면 됌 작은 따옴표로 )
- SELECT ANIMAL_ID, NAME, DATETIME
FROM ANIMAL_INS
ORDER BY NAME ASC, DATETIME DESC

















