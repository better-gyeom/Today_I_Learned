## CSS

### BOX model 구성

- 모든 요소는 박스모델이고, 왼쪽에서 오른쪽으로, 위에서부터 아래로 쌓인다. (normal flow)
- 하나의 박스는 네 부분(영역)으로 이루어진다.
   - content : 글이나 이미지 등 요소의 실제 내용
   - padding : 테두리 안쪽의 내부 여백. 요소에 적용된 배경색, 이미지는 padding 까지 적용된다.
   - border : 테두리 영역
   - margin : 테두리 바깥의 외부 여백. 배경색을 지정할 수 없다.

    ![](boxmodel.PNG)

- shorthand
    ```
    .mar {
        margin: 10px 20px 30px 40px;
    } /* 상 - 우 - 하 - 좌 */
    ```
    ```
    .mar {
        margin: 10px
    } /* 상하좌우 전부 */
    ```
    ```
    .mar {
        margin: 10px 20px
    } /* 상하 - 좌우 */
    ```
    ```
    .mar {
        margin: 10px 20px 30px
    } /* 상 - 좌우 - 하 */
    ```

### CSS display

- 모든 요소는 박스모델이고, display에 따라 크기와 배치가 달라진다.
- inline / block 요소
  - inline
    - 줄바꿈이 일어나지 않는 행의 일부 요소
    - contents 만큼만 영역을 차지한다.
    - width, height,margin을 지정할 수 없다.
    - 상하 여백은 line-height로 지정한다.
    - ex_ div / ul, ol, li / p / hr / form ...
  - block
    - 화면 크기 전체의 가로 폭을 차지한다.
    - 줄바꿈이 일어나는 요소
    - 블록 요소 안에 인라인 요소가 들어갈 수 있다.
    - ex_ span / a / img / input, label / b, em, i, strong ...