# Styling Text (텍스트 효과)

* "\~~"를 앞, 뒤에 추가해 취소선 효과 부여  
    | 예시 코드 | 출력 결과 |  
    | --- | --- |  
    | `~~This was mistaken text~~` | ~~This was mistaken text~~ |  
# Link & Mention(링크 & 멘션)
## Autolink (자동 링크)
* URL을 입력하면 자동으로 링크로 변환  
    | 예시 코드 | 출력 결과 |  
    | --- | --- |  
    | `Visit https://github.com` | Visit https://github.com |  
## Relative Links (상대 경로 링크)
* 링크 URL에서 레퍼지토리 내 현재 markdown file 기준 상대 경로를 사용해 링크 지정  
## Mentioning people and teams (멘션)
* 유저명, 또는 팀명 앞에 '@'를 붙여 멘션  
* 멘션을 받은 유저 또는 팀은 알림을 받음  
## Reference Issue and pull requests (Issue 및 Pull Request 참조)
* 여러 방법으로 Issue 및 Pull Request를 참조 가능  
    | 형식 | 예시 코드 |  
    | --- | --- |  
    | 전체 URL | `https://github.com/jlord/sheetsee.js/issues/26` |  
    | #번호 | `#26` |  
    | GH-번호| `GH-26` |  
    | 유저(조직)명/레포지토리명#번호 | `jlord/sheetsee.js#26` |  
## Reference Commit (커밋 참조)  
* 여러 방법으로 Commit을 참조 가능, 각 방법에 따라 다른 출력 결과  
    | 형식 | 코드 |  
    | --- | --- |  
    | 전체 URL | `https://github.com/jloard/sheetsee.js/commit/a5c3785ed8d6a35868bc169f07e40e889087fd2e` |  
    | SHA | `a5c3785ed8d6a35868bc169f07e40e889087fd2e` |  
    | 유저명@SHA | `jloard@a5c3785ed8d6a35868bc169f07e40e889087fd2e` |  
    | 유저명/레포지토리명@SHA | `jloard/sheetsee.js@a5c3785ed8d6a35868bc169f07e40e889087fd2e` |  
# Using emoji (이모지)
* emoji code 앞에 ':'를 붙여 emoji 사용  
    | 예시 코드 | 출력 결과 |  
    | --- | --- |  
    | `:+1: This PR looks great! - it's ready to merge! :shipit:` | :+1: This PR looks great! - it's ready to merge! :shipit: |  
# Tables (표)
## Creating a table (표 생성)
* '|'와 '-'를 사용해 표 생성   
* '|'는 표의 각 열을 구분지음 (각 행의 마지막에는 '|' 없어도 무관)  
* '-'는 헤더 행과 나머지 행을 구분지음  
* 예시  
    * 예시 코드  

            | First header | Second Header|
            |--------------|--------------|
            | Content Cell | Content Cell |
            | Content Cell | Content Cell |
    * 출력 결과  
        | First header | Second Header|  
        |--------------|--------------|  
        | Content Cell | Content Cell |  
        | Content Cell | Content Cell |  
* '|'가 반드시 정렬되어야 할 필요 없음, '-'는 각 열 당 3개 이상이면 무관  
    * 예시 코드  

            | Command | Description |
            | --- | --- |
            | git status | List all new or modified files
            | git diff | Show file difference that haven't been staged

    * 출력 결과  
        | Command | Description |  
        | --- | --- |  
        | git status | List all new or modified files  
        | git diff | Show file difference that haven't been staged  
## Formatting text in table (표 내부 텍스트 효과 부여)
* 표 내부 텍스트에 Text Styling, 링크, 코드 등의 효과 부여 가능  
* 예시  
    * 예시 코드  

            | Command | Description |
            | --- | --- |
            | `git status` | List all *new or modified* files
            | `git diff` | Show file difference that **haven't been** staged
    * 출력 결과  
        | Command | Description |  
        | --- | --- |  
        | `git status` | List all *new or modified* files  
        | `git diff` | Show file difference that **haven't been** staged  
## Text aligning in table (표 내부 텍스트 정렬)
* 각 열 정렬을 위해 헤더 행 직후 행에 '-'와 함께 :를 사용해 정렬 가능  
* 정렬 종류  
    | 종류 | 코드 |  
    | --- | --- |  
    | 좌측 정렬 | \:\-\-\- |  
    | 중앙 정렬 | \:\-\-\-\: |  
    | 우측 정렬 | \-\-\-\: |  
* 예시  
    * 예시 코드  

            | Left-aligned | Center-aligned | Right-aligned |
            |      :---    |      :---:     |      ---:     |
            | git status   | git status     | git status    |
            | git diff     | git diff       | git diff      |
    * 출력 결과  
        | Left-aligned | Center-aligned | Right-aligned |
        |      :---    |      :---:     |      ---:     |
        | git status   | git status     | git status    |
        | git diff     | git diff       | git diff      |
# Code Blocks (코드 블럭)
* indent 대신 '`'을 3개 사용해 명시적으로 코드 블럭의 시작과 끝 지정 가능  
    * 예시 코드  

            ```
            function test () {  
                console.log("notice the blank line before this function?");  
            }  
            ```
    * 출력 결과  
        ```
        function test () {
            console.log("notice the blank line before this function?");
        }
        ```
* 코드의 언어를 코드 블럭 시작 "```" 뒤에 명시해 문법 하이라이팅 가능
    * 예시 코드  

        \```ruby
        function test () {  
            console.log("notice the blank line before this function?");  
        }  
        \```  
    * 출력 결과  
        ```ruby
        function test () {
            console.log("notice the blank line before this function?");
        }
        ```
