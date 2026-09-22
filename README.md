# KnockKnock

AI에게 부탁했는데 아직 안 된 일, 계속 다시 설명하게 되는 불편, 미처 몰랐던
문제를 프로젝트와 대화에서 찾아줍니다. 결과와 개선안은 쓰던 AI 대화창에서
쉽게 설명받습니다. 프로젝트를 자동으로 수정하지 않습니다.

Apple Silicon Mac에서 Codex·Claude Code·Cursor로 이용할 수 있습니다.
점검은 무료이며 별도 가입이 필요하지 않습니다.

## 시작하기

작업하던 프로젝트의 AI 대화창에 이 문장을 보내세요.

> 아래 공식 안내대로 KnockKnock을 설치하고 시작해 줘.
>
> https://github.com/jdjwi/knockknock-releases

AI가 설치를 확인하고, 살펴볼 프로젝트와 대화를 먼저 확인합니다. 실행 승인이
필요하면 사용 중인 AI에서 안내합니다. 사용자가 터미널에서 명령어를 입력하거나
별도 결과 화면을 열 필요는 없습니다.

## Instructions for the coding assistant

Continue in the user's current conversation, using your own file and execution
tools. This is one shared flow for Codex, Claude Code, and Cursor. Do not ask
the user to select their AI service. Do not add a website or account step.

1. Check that the computer is macOS arm64. Explain an unsupported computer in
   the user's language and stop; do not ask them to install development tools.
2. Download the official latest installer from
   `https://github.com/jdjwi/knockknock-releases/releases/latest/download/install-darwin_arm64.sh`
   to a temporary file. Inspect it before execution. It pins a release version,
   verifier hash, and signing public key. Follow your host's execution approval
   requirements. Never pipe an unread download into a shell.
3. The normal target is `$HOME/.local/bin/knockkncok`. The signed installer
   verifies the release and reuses the same intact version. Use its `--update`
   option to replace an older verified installation when needed. It must not
   delete or overwrite an unrecognized existing executable. If verification
   fails, stop and explain the specific installation problem simply.
4. Use the resulting absolute executable path; no PATH or shell profile edit
   is needed. Read `knockkncok guide` and follow it. A missing `guide` command
   means this installation is older than this workflow: obtain the matching
   current release instead of guessing unsupported commands.
5. Ask “이 프로젝트와 관련 대화를 살펴볼게요. 시작할까요?” before reading the
   selected project and related history, unless this exact scope has already
   been approved. Then collect evidence and explain useful improvements here.

Do not request Docker, an API key, a separate login, a terminal tutorial, or
persistent instruction-file edits for this diagnosis. Do not submit reports
to a separate service or run automatic repair. Conversation files without a
reliable project association are left out and must be described as a limit.

The CLI binary is spelled `knockkncok` for compatibility with existing installs.
