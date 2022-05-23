# 2022-1-DB-Project
## 프로젝트 소개
### 독서기록서비스
도서를 소개하고 기록하여 회원들이 정보를 얻고, 리뷰를 남길 수 있도록 하는 서비스를 만들고자 함.
### 계기
독서를 잘 하지 않아 매년 책을 더 많이 읽자고 다짐을 하는데 잘 실천이 되지 않는다.  
책의 종류가 워낙 많고 다양하다 보니 책 제목과 표지만으로는 어떤 책을 읽어야 할지 막막한데 검색 한번에 책에 대한 정보와 리뷰를 확인 할 수 있다면 보다 쉽게 읽을 책을 고를수 있지 않을까.  
영화나 드라마의 경우에는 정보,평점,리뷰 등을 바로 확인 할 수 있는 사이트를 몇몇 보았다. 이를 도서에도 적용하면 좋을 것 같다는 생각이 들었다.
### 간단한 구상(기능)
* 회원가입  
* 도서 등록,수정,삭제  
* 도서 검색
* 리뷰 등록
* 등..  
## ER다이어그램
**회원**(__아이디__, 비밀번호, 이름, 나이, 전화번호)  
**도서**(__ISBN__, 제목, 저자, 출판사, 평점)  
**리뷰**(__리뷰번호__, __ISBN__, 작성자, 제목, 내용, 별점)  
![ER다이어그램](https://user-images.githubusercontent.com/81346198/161370876-53f7782b-12a6-4cd4-857c-bf8d78d527a3.jpg)  

## (개체,속성 추가된) 요구사항 명세서
1. 사이트 회원으로 가입하려면 회원아이디, 비밀번호, 이름, 나이, 번호를 입력해야 한다.
2. 회원은 회원아이디로 식별한다.
3. 도서에 대한 제목, 작가, 출판사, 출판일, ISBN 을 유지해야 한다.
4. 도서는 ISBN으로 식별한다.
5. 출판사에 대한 출판사 이름, 주소, 전화번호, 사업자번호 정보를 유지해야 한다.
6. 출판사는 여러 도서를 출판할 수 있고, 하나의 도서는 하나의 출판사가 출판할 수 있다.
7. 출판사는 사업자번호로 식별한다.
8. 출판사가 도서를 출판하면 출판에 대한 발행일 정보를 유지해야 한다.
9. 작가에 대한 작가 이름, 생년월일, 등단, 작가 번호 정보를 유지해야 한다.
10. 작가는 여러 도서를 집필할 수 있고, 하나의 도서는 여러 작가가 집필할 수 있다.
11. 작가는 작가번호로 식별한다.
12. 회원은 여러 도서에 대한 리뷰를 작성할 수 있고, 하나의 도서에 여러 회원이 리뷰할 수 있다.
13. 회원이 도서를 리뷰하면 리뷰에 대한 글번호, 제목, 내용, 작성일, 평점 정보를 유지해야 한다.

## ER 다이어그램
![ERD 0523ver ](https://user-images.githubusercontent.com/81346198/169811297-b45adc7c-6d52-4853-a4e3-034779a02fe4.png)

## 스키마
![릴레이션](https://user-images.githubusercontent.com/81346198/169816099-6f977157-1010-4355-86d1-213c53077efd.png)
![물리적스키마](https://user-images.githubusercontent.com/81346198/169830788-e000fe30-e956-4517-ad58-fcb58a680593.png)
