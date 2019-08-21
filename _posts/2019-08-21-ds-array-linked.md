---
title: "ArrayList vs LinkedList"
excerpt: "ArrayList와 LinkedList의 차이점"
categories:
  - datastructure
comments: true
date: 2019-08-21
# last_modified_at: 2019-08-12T19:37:00+09:00
tag: 
    - datastructure
    - arraylist
    - linkedlist
gallery: #이미지 갤러리
    - url: /assets/images/datastructure/arraylistLinkedlist.png
      image_path: /assets/images/datastructure/arraylistLinkedlist.png
      alt: "arraylistLinkedlist"
      title: "arraylistLinkedlist"
---

### ArrayList vs LinkedList

#### 구조 비교
{% include gallery caption="이미지 출처 **http://www.nextree.co.kr/p6506/**."  %}

- ArrayList에서 삽입 삭제
    - 리스트의 자료가 삽입될 위치 만큼 기존의 데이터를 앞으로 혹은 뒤로 미는 과정을 거쳐야됨.
    - 그 후에 자료를 입력하고 삽입 및 삭제 연산을 마침.
- LinkedList에서 삽입 삭제
    - 추가될 자료의 노드를 생성 하고 이전의 노드를 찾아 연결 시킴.
    - 삭제될 자료의 노드를 제거 하고 이전의 노드와 그 다음 노드를 연결시킴.

#### 퍼포먼스 비교

| |ArrayList|LinkedList|
|:---:|:---:|:---:|
|Indexing|Θ(1)|Θ(n)|
|Insert/delete at beginning|Θ(n)|Θ(1)|
|Insert/delete at end|Θ(1)|Θ(n)-last element is unknown<br>Θ(1)-last element is known|
|Insert/delete in middle|Θ(n)|search time + Θ(1)|
|Wasted space (average)|Θ(n)|Θ(n)|