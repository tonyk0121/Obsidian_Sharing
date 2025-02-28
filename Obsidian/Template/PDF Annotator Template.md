<%*
const tfile = await tp.system.prompt("PDF 문서 이름을 입력하세요(.pdf 제외): ");
if (!tfile) {
    tR += "파일 이름이 입력되지 않았습니다.";
    return;
}

// 입력값을 그대로 노트 제목으로 사용
const noteTitle = tfile.trim();

// 노트 제목 변경
await tp.file.rename(noteTitle);

// 노트 이동 (Attatchment/Literature 폴더로)
const newPath = `Attatchment/Annotation 노트/${noteTitle}`;
await tp.file.move(newPath);

// Property 설정
const createdDate = tp.file.creation_date("YY-MM-DD-dddd");
const updatedDate = tp.file.last_modified_date("YY-MM-DD-dddd");

const frontmatter = `---
annotation-target: ${noteTitle}.pdf
created: ${createdDate}
updated: ${updatedDate}
aliases: 
---`;

tR += `${frontmatter}`;
%>
