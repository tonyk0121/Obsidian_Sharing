PDF나 EPUB 파일을 열고 하이라이크, 댓글 추가 추가 등의 주석 작업을 수행할 수 있는 커뮤니티 플러그인이다.
![[Pasted image 20250227215114.png]]
# 사용 방법
1. 주석을 달고자 하는 노트의 [프론트매터](https://kaminik.tistory.com/entry/%EC%98%B5%EC%8B%9C%EB%94%94%EC%96%B8%EC%9D%98-%EC%8B%AC%ED%99%94-1-%ED%94%84%EB%A1%9C%ED%8D%BC%ED%8B%B0Properties#%ED%94%84%EB%A1%9C%ED%8D%BC%ED%8B%B0%EC%9D%98-%ED%95%84%EC%9A%94%EC%84%B1%EA%B3%BC-%EA%B8%B0%EB%8A%A5)에 다음과 같이 'annotation-target' 속성을 추가한다.
```yaml
--- 
annotation-target: 파일경로/파일명.pdf 
---
```
2. 노트 상단의 '더보기' 메뉴(세 점 아이콘)를 클릭하고 'Annotate'를 선택하여 주석 모드로 전환한다.
3. PDF 또는 EPUB 파일에서 원하는 부분을 선택하여 하이라이트하고, 댓글을 추가한다.
4. 주석은 로컬 마크다운 파일에 저장되며, Obsidian 링크를 통해 다른 노트와 연결할 수 있다.
# Template 사용방법 
위 과정을 자동화하기 위해 Templater를 이용해서 자동화하도록 만들었으니 아래 방법을 사용하면 된다.
	템플릿 파일 : [[PDF Annotator Template]]

1. `ctrl+n` 또는 Command Pallete(`ctrl+p`) > `Templater: Create new note from Template` 
2. `PDF Annotator Template` 선택
3. 열고 싶은 pdf파일 이름 입력. (.pdf 제외)
4. 우측 상단 '더보기' 메뉴 ( $\vdots$ 아이콘)를 클릭하고 `Annotate`를 선택하면 주석 모드로 전환된다.
![[Pasted image 20250227214319.png]]