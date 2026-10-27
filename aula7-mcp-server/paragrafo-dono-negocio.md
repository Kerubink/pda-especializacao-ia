# Parágrafo para o dono do negócio

Demos ao assistente de IA uma ferramenta para consultar as instruções que o QualiFlow usa para
pedir casos de teste à IA. Isso poupa o assistente de vasculhar o projeto inteiro quando alguém pede
um ajuste nessas instruções. A ferramenta só lê três pastas de textos e só aceita nomes que existem
nelas, então ela não altera nada, não executa nada e não alcança o arquivo onde ficam as senhas
e chaves do sistema. Testamos de verdade: a primeira versão deixava ler esse arquivo de chaves
com um pedido malicioso; na versão final o mesmo pedido é recusado, porque a trava está no
código da ferramenta, não na boa vontade do assistente.

## Risco que mais ameaça o QualiFlow

Prompt injection indireta. O QualiFlow lê texto que qualquer pessoa escreve nos cards do Azure DevOps e do Jira
e o entrega ao modelo; é exatamente o canal usado no ataque 2 do log. Se o assistente obedecesse a
uma instrução escondida num card, o que ele alcança vira o limite do dano, por isso as tools precisam ter pouco
alcance imposto em código (allow-list), como a `consultar_prompt_qualiflow`.
