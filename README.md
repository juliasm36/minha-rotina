# Minha Rotina

App web que criei para organizar faculdade, tarefas, treinos e alimentação num lugar só, e que uso no dia a dia desde o início do ano.

> **Sobre este repositório:** o código não está publicado. Aqui estão a descrição do projeto e um vídeo de demonstração. **O vídeo usa dados de exemplo**: disciplinas, tarefas e compromissos foram inventados.

## Demonstração

https://github.com/user-attachments/assets/0933b303-984c-4943-9b57-990bb33af78e

## O problema

Eu queria ter num lugar só tudo o que faz parte da minha rotina: aulas e provas da faculdade, tarefas de projetos, compromissos, treinos e o plano alimentar. Também queria saber, a qualquer momento, quantas faltas ainda podia ter em cada disciplina, sem fazer a conta na mão.

## A solução

Um app web, feito com Google Sheets e Apps Script, que funciona no computador e no celular.

**Como funciona:**

1. **Agenda:** o mês mostra aulas, provas, entregas, tarefas, compromissos e checklists, com filtros por tipo.
2. **Faculdade:** cadastro a disciplina com dia, horário, períodos, primeira aula e data final, e o app gera todas as aulas do semestre.
3. **Frequência:** marco presença, falta, presença parcial ou "sem aula" em cada encontro, e o app mostra quantas faltas ainda posso ter.
4. **Projetos:** cada projeto tem etapas com data e tarefas ligadas a ele.
5. **Treinos:** a semana de treinos, com tipos que eu mesma cadastro.
6. **Alimentação:** o plano alimentar por refeição, com opções, grupos de substituição e busca por alimento.

**Regras que defini:**

- **Faltas por disciplina:** cada disciplina tem o seu limite de faltas, e a conta é feita por período de aula. Presença parcial conta metade.
- **Aulas geradas a partir da configuração:** se eu mudo o horário ou as datas, o app recria as aulas e mantém as presenças já marcadas.
- **Tarefa num lugar só:** cada tarefa fica num dia, numa semana ou sem data, nunca em dois ao mesmo tempo.
- **Limpeza automática todo dia:** o que já passou sai da agenda. A tarefa pendente com data vencida volta para "sem data", em vez de sumir. Se a limpeza não tiver rodado, o app faz isso ao abrir.
- **Dados ligados entre si:** excluir uma disciplina leva junto as aulas, provas e tarefas dela. Fechar o semestre apaga só a parte da faculdade; projetos, treinos e plano alimentar continuam.

## O resultado

- Uso o app no dia a dia **desde o início do ano**, no computador e no celular.

## Como construí

Construí o projeto com o apoio do Claude (IA da Anthropic). A divisão de papéis foi esta:

**O meu papel**
- Definir o que o app precisava resolver na minha rotina.
- Escrever as regras: conta de faltas, geração das aulas, limpeza diária e o que acontece quando algo é excluído.
- Desenhar as telas e o fluxo de uso, pensando principalmente no celular.
- Testar no uso real e pedir ajustes. Aqui usei a minha experiência anterior em QA: casos de borda, como aula de vários períodos, tarefa vencida e disciplina excluída.

**O papel da IA**
- Escrever o código a partir das minhas especificações.
- Sugerir soluções técnicas, como gravar uma alteração por vez e salvar as datas como texto para o Sheets não convertê-las.

O código foi escrito pela IA. As decisões sobre o que o app deve fazer, e a validação de que ele faz isso, foram minhas.

## Tecnologias

- **Google Sheets:** base de dados (uma aba por tipo de informação)
- **Google Apps Script:** back-end, acionador da limpeza diária e publicação como aplicativo web
- **HTML, CSS e JavaScript:** interface, com versão para celular
- **Claude (Anthropic):** apoio na escrita do código


