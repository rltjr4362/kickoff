# Kickoff

Claude Code와 Codex에서 새 프로젝트나 기능을 시작할 때 쓰는 에이전트 스킬입니다. 브레인스토밍과 그릴링을 거쳐 `SPEC.md`에 무엇을 만들지 정리합니다. 1부를 승인하면 구현 방식과 검토 계획을 작성하고, 2부를 승인하면 구현을 시작합니다.

## 설치

이 저장소는 Private입니다. 접근 권한을 받은 GitHub 계정으로 인증한 뒤 설치하세요. GitHub CLI를 쓴다면 `gh auth login` 후 `gh auth setup-git`을 실행하면 HTTPS 주소로 복제할 수 있습니다.

아래 명령 중 사용하는 도구에 맞는 명령을 실행하세요. 모든 프로젝트에서 스킬을 사용할 수 있습니다.

**Claude Code**

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/rltjr4362/kickoff.git ~/.claude/skills/kickoff
```

Claude Code에서 `/kickoff 출석 현황판 만들기`를 입력합니다.

**Codex**

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/rltjr4362/kickoff.git ~/.agents/skills/kickoff
```

Codex에서 `$kickoff 출석 현황판 만들기`를 입력합니다.

특정 프로젝트에서만 사용하려면 해당 프로젝트 루트에서 `.claude/skills/kickoff` 또는 `.agents/skills/kickoff`로 설치하세요. 스킬이 새로 설치됐는데 목록에 보이지 않으면 새 세션을 여세요.

## 함께 사용할 수 있는 스킬

- `superpowers:brainstorming`과 `grilling`이 설치돼 있으면 1부에서 순서대로 사용합니다. 설치하지 않은 경우에도 Kickoff의 지침으로 같은 단계를 진행합니다.
- Orca 워커를 사용하는 경우에는 Orca와 `orchestration`이 필요합니다.
- Claude Code에서 `effortless`를 사용 중이면 준비 단계에 활용합니다.

스킬 본문은 [SKILL.md](SKILL.md), 명세서 양식은 [spec-template.md](spec-template.md)에 있습니다.
