# Designer Starter Kit

Figma로 만든 디자인 시스템을 **Claude Code와 대화하면서** 코드로 옮기고,
`/playground`에서 직접 눌러 보고, Vercel로 배포해 보는 연습용 프로젝트예요.

> 코드를 몰라도 돼요. VS Code의 Claude 패널에 **“시작하자”** 라고 보내면 Claude가 순서대로 안내해요.

## 시작하기

1. 이 페이지 오른쪽 위 **Use this template › Create a new repository** → 내 계정에 레포 만들기
2. 내 레포 화면에서 초록색 **Code** 버튼 › HTTPS 주소 복사
3. VS Code에서 빈 작업 폴더를 열고 Claude 패널에:
   `이 레포를 여기에 클론하고 VS Code로 열어줘: [붙여넣기]`
4. 클론된 폴더를 연 뒤 Claude 패널에: **`시작하자`**

준비물(VS Code, Git, Node.js, Claude Code 확장, Claude 구독)은 함께 받은 가이드 장표를 따라 설치해요.

## 들어 있는 것

| 위치 | 무엇 |
|---|---|
| `CLAUDE.md` | Claude가 항상 먼저 읽는 규칙서 (진행 순서, 디자인 규칙, 안전 규칙) |
| `app/globals.css` | 디자인 토큰 (Figma Variables가 들어갈 곳) |
| `components/ui/Button.tsx` | 예시 컴포넌트 |
| `app/playground/` | `/playground` 확인 페이지 |
| `.claude/skills/` | 스킬 6개: figma-sync, build-component, grid-check, playground-polish, ship, new-skill |
| `.claude/agents/figma-reviewer.md` | Figma 대조 검수 서브에이전트 (읽기 전용) |
| `.claude/settings.json` | 파일을 고칠 때마다 4px·색 규칙을 자동 검사하는 훅 |
| `.mcp.json` | Figma MCP 서버 연결 설정 |
| `scripts/check-design.mjs` | 규칙 검사 스크립트 (`npm run check`) |
| `design-system/PROGRESS.md` | 진행 체크리스트 |

## 규칙 한 줄 요약

토큰만 쓰고, 4px 그리드를 지키고, **Figma와 다르면 고치는 곳은 항상 Figma**.

## 명령어 (Claude가 대신 실행해요)

```bash
npm install      # 처음 한 번
npm run dev      # 미리보기: http://localhost:3000/playground
npm run check    # 4px 그리드·색 규칙 검사
npm run build    # 배포 전 확인
```
