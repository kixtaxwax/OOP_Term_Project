# OOP 텀 프로젝트 - 콘솔 기반 텍스트 에디터

## 🚀 구현할 기능 목록

### 💻 전반적인 동작
- 텍스트 파일(test.txt) 로드하기
- 전체 텍스트를 Word 단위로 자르기
- 잘린 각 단어들을 최대 75 byte를 가지는 Line들로 만들기
- 텍스트 변경 시 현재 라인 조정 필요한지 검사하기 (한 단어가 두 줄에 걸치지 않도록)
  - 삽입 시: 삽입 후 75 byte를 넘는지
  - 삭제 시: 삭제 후 다음 Line의 첫 단어가 현재 Line의 마지막 단어로 올 수 있는지
  - 변경 시: 피변경 단어와 변경 단어의 길이 비교하고  변경 단어가 더 길면 삽입 로직, 피변경 단어가 더 길면 삭제 로직
### ✍🏻 유저 입력에 따른 동작

- 단어 삽입 ex) i(1,10,hello) : 첫 번째 라인의 열 번째 단어 뒤에 hello 넣기
	- 예외: l번째 라인이 존재하지 않을 때
	- 예외: w번째 단어가 존재하지 않을 때
	- 예외: 추가하려는 단어가 75byte를 초과할 때
	- 예외: 숫자 외의 문자가 입력될 때
- 단어 삭제 ex) d(2,10) :  두 번째 라인의 열 번째 단어 삭제
	- 예외: l번째 라인이 존재하지 않을 때
	- 예외: w번째 단어가 존재하지 않을 때
	- 예외: 숫자 외의 문자가 입력될 때
- 단어 검색 ex) s(hello) : 첫 번째 hello가 출력 창의 첫번째 라인에 위치하도록 화면 출력
	- 예외: 단어 w가 존재하지 않을 때
- 단어 변경 ex) c(hello,bye) : 모든 hello를 찾아 bye로 변경
	- 예외: 단어 w1이 존재하지 않을 때
- 다음 페이지 출력 (최대 20라인 단위) : n
- 이전 페이지 출력 (최대 20라인 단위) : p
- 변경 내용 파일에 저장 후 종료 : t

### 🖥 출력 관련 동작
- 현재 상태 페이지 출력하기
- 작업 메뉴 출력하기
- 프로그램 메시지 출력하기
- 유저 입력 프롬프트 출력하기


