# Kickoff

Claude Code와 Codex에서 새 프로젝트나 기능을 시작할 때 쓰는 에이전트 스킬입니다. 브레인스토밍과 그릴링을 거쳐 `SPEC.md`에 무엇을 만들지 정리합니다. 1부를 승인하면 구현 방식과 검토 계획을 작성하고, 2부를 승인하면 구현을 시작합니다.

## 설치

아래 명령 중 사용하는 도구에 맞는 명령을 실행하세요. 모든 프로젝트에서 스킬을 사용할 수 있습니다.

**Claude Code**

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/rltjr4362/kickoff.git ~/.claude/skills/kickoff
```

Claude Code에서 `/kickoff 설치 점검`을 입력합니다. Superpowers가 없으면 `/plugin install superpowers@claude-plugins-official`로 추가할 수 있습니다. 준비되면 `/kickoff 출석 현황판 만들기`처럼 실행하세요.

**Codex**

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/rltjr4362/kickoff.git ~/.agents/skills/kickoff
```

Codex에서 `$kickoff 설치 점검`을 입력합니다. Superpowers가 없으면 Codex 앱의 **Plugins** 또는 CLI의 `/plugins`에서 **Superpowers**를 찾아 설치할 수 있습니다. 준비되면 `$kickoff 출석 현황판 만들기`처럼 실행하세요.

특정 프로젝트에서만 사용하려면 해당 프로젝트 루트에서 `.claude/skills/kickoff` 또는 `.agents/skills/kickoff`로 설치하세요. 스킬이 새로 설치됐는데 목록에 보이지 않으면 새 세션을 여세요.

## 함께 사용할 수 있는 스킬

- `superpowers:brainstorming`과 `grilling`을 사용할 수 있으면 1부에서 순서대로 호출합니다. 위 플러그인 설치는 선택 사항입니다. Kickoff에 브레인스토밍과 그릴링의 기본 절차가 들어 있어 별도 설치 없이도 두 단계를 진행할 수 있습니다. [Superpowers 공식 설치 문서](https://github.com/obra/superpowers#installation)
- Orca 워커를 사용하는 경우에는 Orca와 `orchestration`이 필요합니다.
- Claude Code에서 `effortless`를 사용 중이면 준비 단계에 활용합니다.

스킬 본문은 [SKILL.md](SKILL.md), 명세서 양식은 [spec-template.md](spec-template.md)에 있습니다.
