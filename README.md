# Vue3 Quasar App (vue3-quasar-app)

## posts(커뮤니티 목록 만들기)

1. 메인 페이지
 
   - 커뮤니티 목록 페이지의 1번 게시글을 클릭하면 게시글 수정하기 페이지로 이동

2. 게시글 수정 페이지

   - 수정하기를 클릭하면 목록으로 이동할 수 있는 게시글 수정 페이지로 이

3. 게시글 수정 페이지

   - 목록으로 이동하기를 클릭하면 메인페이지로 이동
  
## mypage

1. mypage --> 메인 페이지 

2. Profile을 클릭 시 목록 하단에 Mypage/Profile가 출력되는 페이지로 이동
  
3. Password 클릭 시 목록 하단에 Mypage/Password가 출력되는 페이지로 이동

4. Bookmark 클릭 시 목록 하단에 Mypage/Bookmark가 출력되는 페이지로 이동 


<details>
  
- 모두 버튼의 그림자를 제거하기 위해 사용되지만, 최종적으로 버튼이 표현되는 스타일에 약간의 차이가 있음

- flat은 평평하고 배경색이 없는 스타일로 버튼을 더 단순하고 미니멀한 디자인으로 표현하고 싶을 때

- unelevated는 배경색은 유지하되 그림자를 제거한 스타일로 버튼을 만들고 싶을 때
<summary>  <span style="font-size:100%">flat Vs unelvaled</span>
</summary>
</details>

<details>
  <summary> <span style="font-size:100%">router-link방식과 clik이벤트 방식의 차이점</span></summary>
1. a href

  - 네이버나 구글같은 검색 엔진 서비스에서는 크롤링 봇이 존재(웹사이트에서 검색하면 수집을하는 봇)

  - 그 봇이 검색엔진에 노출시킬수있도록 도와주는데 그게 a href를 통해 수집을 함

  - 그래서 검색 했을 때 보여질 확률 높음

2. rout-link

  - 관리자 페이지 같은 경우 노출이 되면 안되지만 만약 노출이 되어야하는 경우 게시글을 SEO최적화를 하고싶으면 라우트를 사용하는게 효율적
  </details>


