# Prova de disparo — checklist-pre-commit (QualiFlow)

Comando (executado em ~/Projetos/QualiFlow, sem citar o nome da skill):

    claude -p "confere se essa mudança tá pronta pra eu commitar" --allowedTools "Skill"

Resultado: o agente chamou `Skill {"skill": "checklist-pre-commit"}` sozinho, rodou
`git status`/`git diff`, procurou credenciais com grep, marcou pytest/lint/test/build como N/A
(só `.gitignore` e `.claude/` mudaram) e devolveu o checklist ✅/N-A sem commitar nada.
