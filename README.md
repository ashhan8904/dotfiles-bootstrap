# dotfiles — 새 PC 부트스트랩 진입점 (public)

> 🚀 **새 PC 한 줄 세팅** — Claude Code 에 그대로 붙여넣기:
>
> ```
> github.com/ashhan8904/dotfiles-bootstrap 보고 환경세팅해
> ```

> ⚠️ 이 repo 는 **진입점(초인종)** 일 뿐 **비밀 정보 0**. 실제 환경·키·설정은 모두 private repo
> [`ashhan8904/dotfiles-private`](https://github.com/ashhan8904/dotfiles-private) 안에 있으며, 접근엔 GitHub 인증이 필요합니다.

## 새 PC 환경 세팅

### 에이전트한테 — 한 줄
새 PC 에 Claude Code(VSCode extension, 로그인 완료)가 있으면 아무 폴더에서나:

```text
github.com/ashhan8904/dotfiles-bootstrap 보고 환경세팅해
```

에이전트가 자동 수행:
1. `gh` 설치 + `gh auth login` (브라우저 8자리 코드 1회 — GitHub OAuth. PAT 미리 시드 시 생략)
2. `gh repo clone ashhan8904/dotfiles-private`
3. `dotfiles-private/bootstrap/AGENT-INSTRUCTIONS.md` 절차대로 복원 (도구·age키·SSH키·env·`.claude`·자동sync 등록·검증)

### 터미널 직접
```bash
# gh 설치 후
gh auth login --web
gh repo clone ashhan8904/dotfiles-private

# 윈도우
powershell -ExecutionPolicy Bypass -File dotfiles-private\bootstrap\init.ps1
# 맥
bash dotfiles-private/bootstrap/init.sh
```

사람 액션은 **Claude Code 로그인**(진입 전제) + **gh 8자리 1회**(또는 PAT 시드 시 생략) 뿐. 나머지(비밀·키·설정·자동sync)는 자동 복원됩니다.

---

이 repo 에는 토큰·키·계정상세·서버주소 등 **어떤 비밀도 없습니다**. 전부 private `dotfiles-private` 에.
