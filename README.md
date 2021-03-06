# devlog_blog_layout_project
블로그 레이아웃 설계

## VERSION 1
## 12월 20일
+ 블로그 메인페이지 html로 레이아웃 설계
    + 상단 header
    + 사이드 카테고리
    + 메인영역
    + footer 

## 12월 21일
+ 블로그 대분류카테고리 상세페이지 html로 레이아웃 설계
    + 상단 header
    + 사이드 카테고리
    + 대분류 카테고리에 속한 소분류 카테고리를 보여주는 메인영역
    + footer
+ 개선해야 하는 사항
    + 각 페이지별로 중복되는 영역을 효율적으로 처리할 수 있는 방법에 대한 고민 필요


## 12월 22일
+ 블로그 소분류 카테고리 상세페이지 html로 레이아웃 설계
  + 상단 header
  + 사이드 카테고리
  + 상세 게시글 영역
  + footer
+ 개션히야 하는 사항
  + css 레이아웃을 사용하여 영역을 분리하는 방법에 대한 고민 필요

  ## 12월 23일
  + 블로그 게시글 작성 페이지 html 과 css로 레이아웃 설계
   + 상단 header
   + 카테고리 선택하는 부분
   + 글 작성하는 부분
   + 글 저장 버튼
  + 잘된 부분
    + div 태그를 display: inline-block을 사용하여 큰 영역을 먼저 잡고 속 내부를 채웠다
    + 카테고리별 게시글 상세페이지
      + 이미지가 inlne-block 속성이고 이미지 밑에 텍스트를 오게 하고싶은 경우
        + 텍스트를 p태그를 사용하였다 
        + 왜냐하면 p태그는 block 태그 이기 떄문이다
  + 개선해야 하는 사항
    + div 태그를 display: inline-block을 사용하지 않고 수평정렬하는 방식에 대한 고민 푤요

 ## 12월 24일
 + 블로그 로그인 , 회원가입 화면 html 과 css로 레이아웃 설계
 + 상단 header
  + 블로그 로고
  + 버튼들

+ 잘된 부분
  + float를 사용하여 div 레이아웃을 나누고 작업한 부분
    + 전에는 div 정렬하는 것에 어려움이 있었는데 float을 쓰니 정렬이 편해졌다
  + block 특성을 갖는 button태그를 div 안에서 가운데 정렬
    + margin: auto; 속성값을 통해 가운데 정렬

+ 개선해야 하는 사항
  + float을 clear:both 한 이후에 div 에 margin-top이 안먹는 이유
    + display: inline-block 한후 margin-top 속성 값을 줌

  + div 안에서 내부 div를 가로 세러 가운데 정렬하는 방법
    + margin: auto; 
      + 좌 , 우를 기준으로 가운데 정렬

  + div 내부에서 input 태그를 가운데 정렬하는 방법

  + div 내부에서 button 가운데 정렬하는 방법
    + position: relative;
    + top , left 속성을 사용하여 가운데를 맞춰줬다
    + 부모요소의 크기를 기준으로 top , left 방향으로 이동하겠다
    + 참고 - https://velog.io/@younoah/css-centering

  + div 내부에서 block 태그 위 , 아래 가운데 정렬
    + verticle-align: middle; -> 세로 가운데 정렬
    + text-align: center; -> 가로 가운데 정렬
    + 참고 - 참고 - https://moonhouse.co.kr/html/400278


  ## 12월 25일
  + 블로그 로그인 회원가입 페이지 레이아웃 수정
    + 잘 한 부분
      + div 내부에서 input 태그를 가운데 정렬하는 방법
        + input 요소의 display 를 inline-block으로 처리
        + margin-left 속성 값을 기존 px 에서 %로 변경
        + input 태그 내의 text를 정렬하기ㅏ 위해 text-align: center 사용

      + float을 clear:both 한 이후에 div 에 margin-top이 안먹는 이유
        + clear: both 처리한 부모 div를 display:inline-block 처리
        + 그후 margin-top 적용

        + 자식 div 가로 세로 가운데 정렬
          + 자식 div의 position을 absolute 처리
          + 부모 div를 position을 relative 처리
          + 부모 div를 기준으로 top , left 속성 값 적용

    + 개선 해야 하는 사항
      + 소분류 카테고리 항목의 글 상세보기 페이지 레이아웃 
        + float , position을 사용하여 레이아웃 수정
    


 ## 12월 26일
   + 블로그 프로젝트 카테고리 소분류 별 글목록 레이아웃 수정
    + float 속성을 사용하여 레이아웃 수정
       * 작업 내용
         + header
         + content
         + footer

      + 잘 된 점
        + float를 사용하여 div 3개를 가로로 정렬 하였다
          + float: left 속성값을 사용하여 div를 왼쪽에 띄운후
          + margin-left 속성으로 여백을 줬다
        + float 처리된 div 밑에 footer div를 만들었다
          + footer div 태그에 float 속성을 제거하기 위해 clear: both를       사용하였다
          + ```
               .content .left_side {
                float: left;
                width: 250px;
                height: 1000px;
                border: 1px solid orange;
                
            }

            .content .right_side {
                float: left;
                width: 700px;
                height: 1000px;
                border: 1px solid red;
                margin-left: 50px;
            }

            ```
          + 참고 - https://victorydntmd.tistory.com/187
          
      + 개선 사항
        + div 태그 내에서 p태그 가로 세로 가운데 정렬 하는 방법
        

## 12월 27일

+ 잘 된 부분
  + 카테고리 상세 페이지 레이아웃 수정
    + 컨텐트 영역에 left_side div 와 right_side div 추가
      + float을 사용하여 left 정렬후 margin-left 속성을 사용하여 여백 줌
      + ul li 태그를 사용하여 내비게이션 바를 만들어봄
        + ```
                    <ul>
                        <li class="dropdown1">
                            <div class="dropdown-menu1">HTTP</div>
                            <div class="dropdown-content1">
                                <a href="#">인터넷과 네트워크</a>
                            </div>
                        </li>
                    </ul>

                    <ul>
                        <li class="dropdown2">
                            <div class="dropdown-menu2">
                                프론트엔드
                            </div>
                            <div class="dropdown-content2">
                                <a href="#">HTML</a>
                                <a href="#">CSS</a>
                            </div>
                        </li>
                    </ul>


          ```
        + 참고 - https://dinfree.com/lecture/frontend/122_css_proj.html
      
      + table 태그를 사용하여 table 생성
        + ```
                 <table border="2">
                    <thead>
                        <tr>
                            <th>#</th>
                            <th>Title</th>
                            <th>댓글수</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>title1</td>
                            <td>(10)</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>title2</td>
                            <td>(5)</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>title3</td>
                            <td>(3)</td>
                        </tr>
                    </tbody>
                </table>
          ```
          + 참고 - https://www.codingfactory.net/10510

        + div를 사용하여 카드 레이아웃 생성
          +   ```
                 <div class="card-box">
                        <img src="images/login_image.png">
                        <div class="card-body">
                            <h5>card-title</h5>
                            <p>content</p>
                            <a href="#" type="button">상세보기</a>
                        </div>
                  </div>


              ```

          + 참고 - https://www.codingfactory.net/11458
    + 알게된 부분
      + li 태그에 앞에 점 없애기
        + list-style-type: none;
      + a 태그 밑줄 없애기
        + text-decoration-line: none;

    + 개선해야 하는 부분
      + 페이징 버튼 레이아웃 
        + 카드 레이아웃 한 줄에 몇개 오게 할지
      + 카드 레이아웃 모양


## 12월 28일
  + 메인페이지 레이아웃 수정
    + 배운점
      + p태그를 가로 세로 정렬하는 방법
        + vertical-align : inline 요소 또는 inline-block요소를 수직 정렬할때 사용
        + text-align : block 요소 안에 있는 inline 요소를 정렬한다 (텍스트를 정렬한다)
    + 잘된점 
      + float을 사용하여 header 레이아웃  배치
        +  ```
           div {
                box-sizing: border-box;
            }

            .blog_top {
                width: 1000px;
                height: 100px;
                border: 1px solid black;
                margin-left: 15%;
            }

            .blog_top .left_side {
                float: left;
                width: 100px;
                height: 50px;
                margin-left: 10px;
                border: 1px solid red;
                margin-top: 15px;

            }

             .right_side div {
                margin-left: 600px;
                float: left;
                border: 1px solid green;
                margin-top: 30px;
                
            }

            .right_side div button {
                margin-left: 10px;
                margin-top: 5px;
            }
           ```
        + div 내그 p 태그 정렬
          + p태그를 div로 한번 감싸서 정렬
            +  ```
                     .left_side .blog_title {
                        width: 80px;
                        height: 40px;
                        border: 1px solid orange;
                        margin-left: 20px;
                        margin-top: -6px;
                        
                    }

                    .blog_title p {
                        font-size: 1.25rem;
                    }
              ```


        + ul li를 사용하여 dropdownlist 구현
          +  ```
                 <ul>
                    <li class="dropdown">
                        <div class="dropdown-menu">HTTP</div>
                        <div class="dropdown-content">
                            <a href="#">인터넷과 네트워크</a>
                            <a href="#">URI와 웹 브라우저 요청흐름 (2)</a>
                            <a href="#">HTTP 기본</a>
                            <a href="#">HTTP 메서드</a>
                        </div>

                    </li>
                </ul>
             ```
            + dropdown : 각각의 메뉴를 구성하는 껍데기 클래스
            + dropdown-menu : 메인 메뉴 항목을 정의하는 클래스
            + dropdown-content : 서브메뉴가 있을 경우 드롭다운으로 나타난다
              + 서브 메뉴 목록 지정 클래스


        + div를 사용하여 card-box 만들기
          + ```
              <div class="card_box">
                  <div class="card_image">
                      <img src="images/login_image.png">
                  </div>
                  <div class="card_content">
                      <h3><a href="#">글 제목</a></h3>
                      <div>
                          <span>작성자</span> <span>작성일</span>
                      </div>
                      
                      <a href="#">대분류 카테고리</a> <a href="#">소분류 카테고리</a>
                      <div class="content">
                          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus, tempore. Dolorum vero sed in consectetur eos commodi animi incidunt optio id hic nesciunt ut, pariatur obcaecati veritatis officiis itaque deserunt.</p>
                      </div>
                  </div>
               </div>
         + div 를 사용하여 footer 만들기
            + ```
                <div class="blog_footer">
                  <div>
                      <p> DevLog.CMY <br>
                          <a href="#">@2021 DevLog.CMY</a><br>
                          Powered By CMY
                      </p>
                      
                  </div>
              </div>

              

            .blog_footer {
                display: inline-block;
                margin-left: 15%;
                margin-top: 20px;
                width: 1000px;
                height: 90px;
                border: 1px solid royalblue;
            }

            .blog_footer div {
                display: inline-block;
                text-align: center;
                margin-left: 50%;
               
            }

            ```

     + 개선해야 하는 부분
       + 페이지네이션 레이아웃 설계
       + 카테고리 상세 페이지 
        + 레이아웃 , 헤더 , footer
       + 글 상세 페이지
         + 레이아웃
           + 가로 3개 div 레이아웃 으로 변경
           + 1:1 채팅 버튼 추가
           + 질문하기 버튼 추가
         + 헤더
         + footer


# 12월 29일
 ## 로그인 , 회원가입 , 글쓰기 페이지 레이아웃 수정
 + 잘 된점
 + div content 영역 분할
 ```
            .login_popup {
                clear: both;
                width: 1000px;
                height: 500px;
                position: relative;
                border: 1px solid brown;
                display: inline-block;
                margin-left: 15%;
                margin-top: 30px;
            }

            .login_popup .popup {
                position: absolute;
                width: 500px;
                height: 400px;
                border: 1px solid orange;
                left: 30%;
                top: 10%;

            }
   + postion relative와 absolute를 사용
  + div 내부 버튼 정렬
  ```
  .login_popup .popup .popup_body div {
                width: 200px;
                height: 100px;
                border: 1px solid black;
                margin-left: 35%;
            }

            .login_popup .popup .popup_body div button {
                display: block;
                margin-bottom: 10px;
                width: 200px;
            }
  + button을 div로 감싸서 버튼 정렬

  ## 향후 계획
  + 블로그
    + 글 상세 페이지 레이아웃 수정
  + 관리자 페이지
    + 관리자 메인 페이지 레이아웃 설계
    + 글 관리 페이지 레이아웃 설계
    + 카테고리 관리 페이지 레이아웃 설계
    + 댓글 관리 레이아웃 설계
    + 카테고리 이동 팝업 레이아웃 설계
    + 카테고리 관리 팝업 레이아웃 설계





# 12월 30일
## 블로그 글 상세 페이지
### 잘된점
+ 이전까지는 레이아웃을 float 와 absolute , relative를 사용하여 잡았다
+ 이번부터는 flex를 적용하여 레이아웃을 잡았다

### 배운점
+ flex의 정렬 방식 - row , column
+ items 요소들을 container로 감싸서 정렬시킨다
+ flex-direction을 사용하여 item들을 가로 방향 또는 세로 방향으로 정렬

## 개선할 점
+ 블로그 상세글 레이아웃의 content 내부 영역 레이아웃 수정


# 12월 31일
## 블로그 글 상세페이지
### 잘된점
+ flex를 사용하여 컨텐츠 영역 레이아웃 설계
```
            .middle_container .middle_center .content_center_container {
                display: flex;
                flex-direction: column;
            }

            .middle_center .content_center_container .content_top {
                margin-top: 20px;
                width: 400px;
                height: 1000px;
                margin-left: 7%;
            }


             <div class="middle_center">
                <div class="content_center_container">
                    <div class="content_top">
                        <h1>글 제목</h1>
                        <div>
                            <span>DevLog.CMY</span> <span>2021-12-31</span> <a href="#">대항목</a> <a href="#">소항목</a>
                        </div>

                        <div>
                            
                            <p>
                                <h2>소제목1</h2>
                                <img src="images/login_image.png">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam quo laboriosam, aliquam suscipit doloribus omnis expedita qui quae nesciunt voluptatibus dolorem, sunt minima repellat, nobis ratione dolor! Ut, dolore dolorem?
                                추우 텍스트 에디터로 변경할 예정


                                <img src="images/login_image.png">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam quo laboriosam, aliquam suscipit doloribus omnis expedita qui quae nesciunt voluptatibus dolorem, sunt minima repellat, nobis ratione dolor! Ut, dolore dolorem?
                                 
                            </p>
                        </div>
                    </div>
                </div>
            </div>
          
            

            .middle_container .middle_right {
                width: 200px;
                height: 700px;
                margin-left: 3%;
                margin-right: 2%;
                margin-top: 20px;
                border: 1px solid purple;
            }

            .middle_right h5 {
                display: inline-block;
                margin-left: 15%;
                font-size: 20px;
            }



            <div class="middle_right">
                <h5>on this page</h5>
                <ul>
                    <li class="dropdown1">
                        <div class="dropdown-menu1">글제목</div>
                        <div class="dropwdown-content1">
                            <a href="#">소제목1</a>
                        </div>
                    </li>
                </ul>
            </div>



```
+ flex를 사용하여 댓글 영역 레이아웃 설계
```
  
            .content_bottom_apply {
                display: flex;
                flex-direction: row;
                width: 1000px;
                height: 400px;
                border: 1px solid orange;
                margin-top: 20px;
                margin-left: 15%;
            }
            
            .content_bottom_apply .container  {
                display: flex;
                flex-direction: column;
                margin-left: 30px;
                margin-top: 20px;
                width: 800px;
                height: 370px;
                border: 1px solid black;
            }

            .container .message1 {
                margin-top: 5px;
                width: 700px;
                height: 100px;
                margin-left: 10px;
                border: 1px solid orchid;
            }

            .container .message1 p {
                margin-left: 50px;
            }

            .container .message2 {
                margin-top: 5px;
                width: 700px;
                height: 100px;
                margin-left: 10px;
                border: 1px solid orchid;
            }

            .message2 span {
                margin-left: 580px;
                margin-top: -2px;
            }
            .message2 img {
                margin-left: 2px;
               
            }

            .message2 p {
                display: inline-block;
                margin-left: 50px;
            }

            .container .type_message {
                margin-top: 20px;
                margin-left: 10px;
                
            }

            .container .type_message form button {
                display: block;
            }

            .content_bottom_apply div img {
                width: 50px;
                height: 50px;
                
            }

            .content_bottom_apply .message_container {
                display: flex;
                flex-direction: column;
                width: 800px;
                height: 100px;
                margin-top: 200px;
                margin-right: 50px;
            }

            .message_container .type_message form button {
                display: block;
            }

            .type_message textarea {
                width: 700px;
                height: 100px;
            }

             <div class="content_bottom_apply">
                <div class="container">
                  <div class="message1">
                      <img src="images/login_image.png" /><span>Leo</span>
                      <p>Good Article</p>
                  </div>
                  <div class="message2">
                      <span>Neo</span> <img src="images/login_image.png" />
                      <p>thank you for you comments^^</p>
                  </div>
                  <div class="type_message">
                      <form>
                          <textarea placeholder="please leave a message">  </textarea>
                          <button type="submit">전송</button>
                      </form>
                  </div>
              </div>
            </div>


```

### 배운점
+ 댓글을 만들때는 flex-direction:column을 사용하여 div를 세로로 정렬하였다
+ 컨텐츠 영역을 만들때는 flex-direction:row를 사용하여 div를 가로로 정렬하였다

### 개선할점
+ 주말에도 조금씩 프로젝트를 진행하자
+ 이번주 주말까지는 상세페이지 화면과 관리자 메인페이지 레아아웃 작업을 끝내도록 하자


# 2022년 01월 01일
## 잘된점
+ flex 레이아웃을 사용하여 카드레이아웃을 만들어봄
+ flex의 주축 , 교차축 개념을 사용하여 카드레이아웃을 정렬함
```
            .middle_list .items .container {
                width: 1000px;
                height: 380px;
                display: flex;
                justify-content: space-around;
                align-items: center;
                border: 1px solid palevioletred;
            }

            .middle_list .items .container .card1 {
                width: 200px;
                height: 300px;
                border: 1px solid red;
            }

```
+ div의 width가 100%인 full-page header를 만들어봄
## 배운점
+ flex의 주축 ,  교차축
    + justify-content가 row 인지 column인지에 따라 주축 과 교차축이 결정된다
    + 기본적으로 주축은 row 방향이다
    + 주축을 정렬할 떄는 justify-content를 사용한다
    + 교차축을 정렬할 때는 align-items를 사용한다
    + [flex에 대한 상세 정리내용](https://unique-wandflower-4cc.notion.site/flexbox-2-1a2104c710014a4387eab8225bf4fa9d)

## 개선할점
+ 블로그 프로젝트 초기부터 지금까지는 div의 모든 레이아웃을 width: 100%로 하고
+ maring-left: 15%를 줘서 가운데에 놓고 작업을 했었다
+ 그런데 블로그 사용자 입장에서 해당 레이아웃의 크기가 내용을 볼때는 답답하게 느껴질수 있겠다고 생각했다
+ 따라서 이를 개선하기 위해 글 상세페이지의 header 부분을 width가 100%인 full-page header로 수정해 보았다
+ 이를 바탕으로 모든 레이아웃에 반영해야 겠다
```
            *{
                padding: 0;
                margin: 0;
                box-sizing: border-box;
            }

             html, body{height: 100%;}

            .top_container {
                display: flex;
                flex-direction: row;
                margin: 0;
                width: 100%;
                height: 100px;
                border: 1px solid black;       
            }
```


# 2022년 01월 02일
## 잘된점
+ 블로그 글 상세페이지 글 밑에 글이 속한 태그를 표시하는 레이아웃 추가
+ 글을 공유할수 있는 버튼 추가
+ 글에 대한 문의를 채팅으로 남길수 있는 1:1문의하기 버튼 추가
+ 글에 대한 이미지를 포함한 장문의 질문을 남길수 있는 질문하기 버튼 추가

## 배운점
+ flex 컨테이너를 만들었다
+ 컨테이너 안에 내부 요소들이 새로 방향으로 쌓일수 있게 flex-direction을 row로 줬다
+ 주축(새로) 기준 내부 요소들이 자연스럽게 여백을 갖도록 justify-content: space-around를 줬다
+ 교차축(가로) 기준 내부 요소들이 가운데 올수 있도록 align-items: center를 줬다
```
   .content_qa_share  {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;    
        width: 1000px;
        height: 100px;
        border: 1px solid peru;
        margin-left: 15%;
        margin-top: 20px;

    }
    
    <div class="content_qa_share">
        <div class="content_tags">
            <a href="#">대항목</a>
            <a href="#">소항목</a>
        </div>
        <div class="q&a_share_buttons">
            <button type="button">공유하기</button>
            <button type="button">1:1문의하기</button>
            <button type="button">질문하기</button>
        </div>
    </div>

```

## 향후 계획
+ 다음주 부터 관리자 페이지 작업 시작
+ 관리자 메인 페이지
+ 관리자 글 관리 페이지
+ 관리자 카테고리 관리 페이지
+ 관리자 댓글 관리 페이지

# VERSION 2
# 2022년 01월 03일

## 잘된점
+ flex를 사용하여 블로그 관라지 페이지 레이아웃 작업 진행
+ css 에서 특성선택자를 사용하여 코드 리펙토링
+ 순수하게 flex만을 사용하여 레이아웃 정렬
## 배운점
+ flex를 사용할 때와 position 속성을 사용하여 정려할 때의 차이를 명확하게 느낄수 있었다
+ flex-direction에 따른 주축 과 교차축 설정 방법
+ justify-content를 사용하여 컨테이너가 감싸고 있는 전체 div를 가로 방향으로 정렬
+ align-items를 사용하여 컨테이너가 감싸고 있는 전체 div를 세로 방향으로 정렬
+ 특성선택자를 통해 html 요소를 더욱 명확하게 선택할 수 있었다
+ 부모 요소 내부에 자식요소를 선택할 때 결합 선택자를 사용하여 관계를 확실하게 표현할 수 있었다
## 향후 계획
+ 관리자 메인페이지 chart.js 적용
+ 글 관리 페이지
+ 카테고리 관리 페이지
+ 댓글 관리 페이지
+ 채팅

# 2022년 01월 04일
## 잘된점
+ 블로그 관리자 메인페이지 작업
+ chart.js 를 적용하여 월별 블로그 방문자 그래프 생성
+ div에 7일간 인기글 목록을 보여주는 ol li 태그를 사용하여 레이아웃 생성

## 배운점
+ chart.js를 사용하여 line chart 생성
+ chart.js cdn 사용하는 방법
```
  <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.7.0/chart.js"></script>
<script>
    const $chart = document.querySelector('#myChart').getContext('2d');
    const myChart = new Chart($chart , {
    type: 'line',
    data: {
        labels: ['January', 'Feb', 'March', 'April', 'May', 'June' , 'July'],
        datasets: [{
            yAxisID: 'y',
            label: '블로그 월별 방문자 그래프',
            data: [12, 19, 3, 5, 2, 3 , 16],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            y: {
                max: 25,
                ticks: {
                    beginAtZero: true,
                    
                }
                
            }
        }
    }



});

</script>
       
```

### 향후 계획
+ 블로그 관리자 글관리 페이지
+ 블로그 관리자 카테고리 관리 페이지
+ 블로그 관리자 댓글 관리 페이지
+ 블로그 관리자 채팅 관리 페이지

              

# 01월 05일

## 잘된점
+ flex를 사용하여 div 내부 요소들을 정렬
+ flex를 사용하여 페이징 레이아웃 구현

## 배운점
+ 자식 컨테이너 의 내부  레이아웃을 정렬할때도 flex를 사용하면 편하다
```
    [class="middle_content"] {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        margin-top: 40px;
        width: 100%;
        height: 900px;
        border: 1px solid red;
    }

    .middle_content  .content_left {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        margin-top: 20px;
        width: 175px;
        height: 850px;
        border: 1px solid red;
        margin-left: 10px;
        
    }

    .middle_content > .content_left  > .content_top {
        width: 160px;
        height: 200px;
        border: 1px solid black;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

        .middle_content > .content_left  > .content_top img {
        width: 50px;
        margin-top: -16px;
    }

    .middle_content > .content_left  > .content_top h4 {
        margin-top: 20px;
    }


    <div class="middle_content">
        <div class="content_left">
            <div class="content_top">
                <img src="../version1/images/login_image.png">
                <h4>DevLog.CMY</h4>
                <button type="button">블로그 관리홈</button>
            </div>
        </div>
    </div>    

```
               
## 향후 계획
+ 카테고리 관리 페이지
+ 댓글 관리 페이지
+ 채팅 관리 페이지
        

# 01월 06일
## 잘된점
+ flex를 사용하여 부모 컨테이너 내부 자식 요소들을 정렬하는 방법을 효율적으로 개선하기 위해 고민
+ 고민 결과
+ 부모 div 안에 화면 양쪽에 배치할 요소들을 두개를 만들어 뒀다
### 문제점
+ 기존에는 요소들을 flex를 사용하여 양쪽에 배치한후
+ 각각 width , height , border를 줘서 한번더 요소들을 감싸는 div를 만들었다
+ div 안에서 원한는 위치로 이동시켰다
+ flex를 사용하여 효율적으로 레이아웃 배치 작업을 진행하려고 했는데 코드의 양이 더 늘어나 버렸다


### 해결책
+ 1. flex를 사용하여 정렬해야 하는 요소들을 justify-content 와 align-items 속성을 사용하여 적절하게 배치시켜준다
+ 2. 각 요소들을  border 속성을 사용하여 테두리를 잡는다
+ 3. 여기서 바로 margin-left 와 margin-right 속성을 사용하여 원하는 위치로 이동시켜 줬다
    + 왜? justify-content 속성의 값을 space-between으로 줬기 때문
    + 이럴 경우 요소들이 양쪽 끝에 붙게 된다
    + 부모 div 의 border와 요소들 사이에 margin을 사용하여 여백을 주기 위해 magin-left 와 margin-right를 사용하였다
+ 4. 처음에 box-sizing 설정을 border-box로 해뒀기 떄문에 border를 기준으로 위치를 조정하는 것이 가능해 졌다
+ 5. 이를 통해 코드의 양을 줄이고 효율적으로 작업할 수 있게 되었다
+ 6. 또한 flex를 사용하는 장점이 두배가 되었다

### 코드 내용
```
* {
    box-sizing: border-box;
}

[class="top_header"] {
    width: 100%;
    height: 100px;
    border: 1px solid black;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}


.top_header h1 {
    display: inline-block;
    border: 1px solid gold;
    margin-left: 5%;
}

.top_header .button_container  {
    display: inline-block;
    border: 1px solid black;
    margin-right: 5%;
}
```


## 배운점
+ box-sizing : border-box



## 개선해야 할 사항
+ 각 화면별로 항상 반복해서 사용하는 레이아웃이 있다
+ 헤더 , 사이드바 , 푸터
+ 이들을 새로운 페이지를 작업 할때마다 다시 만드는 것은 시간 낭비이다
+ 이들을 하나의 페이지에 만들어 두고 필요한 곳에서 가져다 쓸수 있는 방법에 대한 고민 필요



# 01월 07일
## 카테고리 관리 페이지
### 잘된점
+ flex를 사용하여 레이아웃 설계
+ flex 속성을 사용하여 카테고리목록 계층구조 표현

### 고민했던 부분
+ 카테고리의 개수가 증가될때 height의 크기를 자동으로 늘려주는 방법
+ 부모 요소의 height 속성 값을 auto 로 설정하여 해결함

### 상세 코드
```
 <div class="content_right">

    <div class="right_top">
        <h4>카테고리 관리</h4>
        <div class="top_box1">
            <p>카테고리 순서를 변경하고 주제 연결을 설정할 수 있습니다.</p>
            <div>
                <span>8/500</span>
                <button type="button">전체 펼치기</button>
                <button type="button">전체 접기</button>
            </div>
        </div>
        <div class="top_box2">
            <div class="box2_top">
                <h5>분류 전체 보기</h5>
                <div>
                    <button type="button">수정</button>
                    <button type="button">관리</button>
                    <button type="button">이동</button>
                </div>
            </div>
            <div class="box2_second">
                <h5>HTTP<small>(총글수)</small></h5>
                <div>
                    <button type="button">수정</button>
                    <button type="button">관리</button>
                    <button type="button">이동</button>
                </div>
            </div>
            <div class="box2_second_1">
                <div class="a">
                    <h4>인터넷 네트워크 <small>(4)</small></h4>
                    <div>
                        <button type="button">수정</button>
                        <button type="button">관리</button>
                        <button type="button">이동</button>
                    </div>
                </div>
                <div class="a">
                    <h4>URI와 웹브라우저 요청흐름 <small>(4)</small></h4>
                    <div>
                        <button type="button">수정</button>
                        <button type="button">관리</button>
                        <button type="button">이동</button>
                    </div>
                </div>
                <div class="a">
                    <h4>HTTP 기본 <small>(4)</small></h4>
                    <div>
                        <button type="button">수정</button>
                        <button type="button">관리</button>
                        <button type="button">이동</button>
                    </div>
                </div>
                <div class="a">
                    <h4>HTTP 메서드 <small>(4)</small></h4>
                    <div>
                        <button type="button">수정</button>
                        <button type="button">관리</button>
                        <button type="button">이동</button>
                    </div>
                
                </div>
            </div>
            <div class="box2_third">
                <h5>프론트<small>(총글수)</small></h5>
                <div>
                    <button type="button">수정</button>
                    <button type="button">관리</button>
                    <button type="button">이동</button>
                </div>
            </div>
            <div class="box2_third_1">                            
                <div class="a">
                    <h4>HTML <small>(1)</small></h4>
                    <div>
                        <button type="button">수정</button>
                        <button type="button">관리</button>
                        <button type="button">이동</button>
                    </div>
                </div>
                <div class="a">
                    <h4>CSS  <small>(7)</small></h4>
                    <div>
                        <button type="button">수정</button>
                        <button type="button">관리</button>
                        <button type="button">이동</button>
                    </div>
                </div>

            </div>

            <div class="add_category">
                <h4>카테고리 추가</h4>
            </div>
            
            <div class="save_category">
                <h4>변경사항 저장</h4>
            </div>

        </div>
    </div>
    <div class="right_bottom">
        <div>
            <p>카테고리명 글자수: <input type="text"/></p>
        </div>
        <div>
            <p>카테고리별 글수:   <select>
                        <option value="reply_manage">표시합니다.</option>
                        <option value="replay_police">표시하지 않습니다.</option>
                    </select>
            </p>
        </div>
        <div>
            <p>카테고리 새글 발행여부:   <select>
                        <option value="reply_manage">표시합니다.</option>
                        <option value="replay_police">표시하지 않습니다.</option>
                    </select>
            </p>
        </div>
        <div>
            <p><input type="text"/> 일 이내 발행된 글의 경우 새글 표시합니다. </p>
        </div>
    </div>
</div>


```

```
.content .content_right {
    margin-top: 20px;
    width: 1200px;
    /* height: 850px; */
    height: auto;
    border: 1px solid black;
    margin-right: 10px;

    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.content_right .right_top {
    width: 95%;
    /* height: 600px; */
    height: auto;
    border: 1px solid red;
}

.content_right .right_top h4 {
    display: inline-block;
    margin-left: 11%;
}

.content_right .right_top  .top_box1 {
    width: 100%;
    height: 100px;
    border: 1px solid green;
    
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}


.content_right .right_top .top_box2 {
    margin-top: 10px;
    width: 100%;
    /* height: 300px; */
    height: auto;
    border: 1px solid greenyellow;

    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
}


.content_right .right_top .top_box2 .add_category {
    width: 80%;
    height: 50px;
    border: 1px solid black;
    text-align: center;

}

.content_right .right_top .top_box2 .save_category {
    width: 80%;
    height: 50px;
    border: 1px solid black;
    text-align: center;

}



.content_right .right_top .top_box2  .box2_top {
    width: 80%;
    height: 40px;
    border: 1px solid black;
        
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}
.content_right .right_top .top_box2  .box2_second {
    width: 80%;
    height: 40px;
    border: 1px solid black;

    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}

.content_right .right_top .top_box2  .box2_second_1 {
    width: 70%;
    height: auto;
    border: 1px solid red;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
}


.content_right .right_top .top_box2  .box2_second_1 .a {
    width: 100%;
    height: auto;
    border: 1px solid black;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}



.content_right .right_top .top_box2  .box2_third {
    width: 80%;
    height: 40px;
    border: 1px solid black;

    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}


.content_right .right_top .top_box2  .box2_third_1 {
    width: 70%;
    height: auto;
    border: 1px solid red;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;

}



.content_right .right_top .top_box2  .box2_third_1 .a {

    width: 100%;
    height: auto;
    border: 1px solid black;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;


}

.content_right .right_bottom {
    margin-top: 20px;
    width: 95%;
    height: auto;
    border: 1px solid orange;
}

```

# 01월 10일

## 1:1 채팅 문의 페이지
### 작업 내용
+ 목적: 블로그 방문자들이 컨텐츠를 읽다가 댓글로 공개적으로 문의하기 어려운 질문이 생기는 경우 
+ 혹은 긴 상담이 필요한 내용의 경우를 위해 채팅 문의 페이지를 만들어 보았다
### 기능
+ 상단에는 메시지를 받는 사람의 ID 정보가 나온다
+ 내가 보낸 메시지는 오른쪽에 뜨고 상대방이 나한테 보낸 메시지를 왼쪽에 이미지와 함께 뜨도록 레이아웃을 구성해 보았다

## 1:1 채팅 관리 페이지
### 작업 내용
+ 목적: 고객들이 보낸 채팅을 관리하지 위한 페이지

### 기능
+ 고객으로 부터 메시지가 왔는지 확인할 수 있는 왼쪽 레이아웃
+ 특정 고객에서 메시지 답장을 보낼수 있는 오른쪽 레이아웃
+ 상단에는 메시지를 받는 사람의 ID 정보가 나온다
+ 내가 보낸 메시지는 오른쪽에 뜨고 상대방이 나한테 보낸 메시지를 왼쪽에 이미지와 함께 뜨도록 레이아웃을 구성해 보았다

### 개선 해야할 부분
+ 채팅창에서 메시지를 받는 사람과 보낸는 사람이게 필요한 데이터가 어떤게 있을지 고민해 볼것
+ 채팅 입력하는 레이아웃 div 크기에 딱 맞출것




# 01월 11일
## 팝업 레이아웃 생성
### 기존에 만들어 뒀던 회원가입 과 로그인 레이아웃을 사용하여 팝얼 레이아웃을 만들어 보았다

#### 잘된점
+ 자바스크립트의 태그 선택자를 사용하여 필요한 요소를 선택해 왔다
+ 요소에 이벤트를 발생시켜 버튼이 클릭 되었을때 팝업을 띄우는 함수를 생성하였다
+ 팝업이 띄워진 효과를 확실하게 주기 위해 background-layout을 만들고 
+ 버튼이 클릭되었을때 색을 회색으로 바꿔 실제로 띄워져 있는 느낌을 줬다
+ 레이아웃과 팝업의 순서를 z-index 속성을 사용하여 지정해 줬다

#### 배운점
+ document 객체의 querySelector 함수를 사용하여 원하는 html 요소를 가져온다
+ addEventListener 함수를 사용하여 html 요소에 이벤트를 걸어줬다
+ 이벤트가 발생했을때 이를 처리할 함수를 콜백함수로 만들었다
+ 버튼을 누르기 전 과 후에 보여야 하는 레이아웃과 보이지 않아야 하는 레이아웃을 자바스크립트의 style.display 속성을 사용하여 설정해 줬다
+ z-index 속성을 사용하여 요소들의 우선순위를 정해줬다
+ 버튼이 클릭 되었을때 팝업이 떠있는 듯한 효과를 주기 위해 사용했다


#### 개선해야 하는 부분
+ 팝업이 떴을때 기존 메인페이지 레이아웃을 숨기지 않고 
+ 레이아웃 위해 background-layout을 씌우고 그 위에 팝업이 띄워지게 수정
+ 레이어 팝업에 대한 추가적인 학습 필요



# 01월 12일

### 잘된점
+ 블로그 메인페이지에 반복적으로 사용되는 header 와 footer 레이아웃 분리작업진행



# 01월 13일
### 잘된점
+ 메인페이지 레이아웃을 header.html 과 footer.html 로 분리하여 include하여 불러올수 있도록 처리하였다