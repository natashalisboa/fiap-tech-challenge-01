<samp>

# Tech Challenge 01 - Pós Tech FIAP - FSDT/2025 - Grupo 02
<p>💾 Primeiro desafio da pós graduação em desenvolvimento full-stack <a href="https://postech.fiap.com.br/curso/full-stack-development">@FIAP</a></p> 
<details>
  <summary><samp>Descrição do Desafio</samp></summary>
  <br>
Tech Challenge é o projeto da fase que englobará os conhecimentos
obtidos em todas as disciplinas da fase.

## O problema
Hoje, professores e professoras da rede pública de educação muitas
vezes não têm ferramentas para postarem suas aulas e transmitirem
conhecimento para os alunos e alunas de forma prática, centralizada e
tecnológica.
Para solucionar esse problema, vamos utilizar os conhecimentos
adquiridos nessa fase para auxiliar a nossa comunidade com a criação de uma
aplicação de blogging dinâmico utilizando a plataforma OutSystems. A aplicação
deve permitir que alunos e alunas visualizem uma lista de posts, leiam postagens
específicas e ofereça uma visão administrativa para os(as) docentes, permitindo
a criação, edição, listagem e exclusão de postagens.
 
## Requisitos funcionais:
1. Visualização de posts: Os alunos e alunas devem ser capazes de visualizar uma lista de posts na
página principal.
2. Leitura de posts: Os alunos e alunas devem poder ler um post específico ao clicar sobre o
título ou conteúdo.
3. Gerenciamento de postagens (Visão administrativa):
 - Os professores e professoras devem poder criar postagens.
 - Edição de postagens existentes.
 - Listagem de todas as postagens criadas.
 - Exclusão de postagens.
   
## Requisitos técnicos:
1. Plataforma OutSystems: Utilização da plataforma OutSystems para o desenvolvimento da aplicação.
2. Documentação: Documentação mínima descrevendo o fluxo, fluxograma da aplicação e
como realizar operações básicas. Dica: utilize plataformas como draw.io,
lucidchart ou MIRO para desenho do fluxograma.
3. Protótipo de layout: Nessa primeira fase não é necessário se preocupar com um layout moderno,
avançado e com os padrões de UI/UX (Pode ser um layout simples).
3. Autenticação: Nessa primeira fase não é necessário autenticação.
 
## Entrega
1. Código-Fonte: Projeto OutSystems contendo os elementos necessários para o
funcionamento da aplicação.
2. Apresentação gravada: Uma apresentação gravada demonstrando o funcionamento da plataforma,
exibindo o processo de criação, edição e exclusão de postagens e demonstrando
as telas de visualização de uma postagem e de listagem de postagens para o
usuário do blog. O vídeo deve ter de 5min a 10min.
3. Documentação: Documentação simples descrevendo o fluxo da aplicação e como realizar
operações básicas, como foi o processo de trabalho do grupo e quais foram as
dificuldades encontradas.
</details>

## Membros do Grupo 02:
<a href="https://github.com/natashalisboa">Natasha Lisboa</a> | 
<a href="https://github.com/lmagueta">Lucas Magueta</a>
</samp>

# Portal Múltipla Escolha
 <p><img src="/assets/logo.png"></p>
O projeto é inspirado no icônico <strong>Colégio Múltipla Escolha</strong>, cenário da temporada de <strong>Malhação 2004</strong>, que representava um espaço jovem, dinâmico, cheio de troca de conhecimentos, ideias e histórias.<br>
A proposta é criar um blog educacional onde professores e professoras podem postar conteúdos, atividades, reflexões e materiais de apoio para seus alunos e alunas, de forma prática e centralizada. Assim como no colégio da série, este ambiente digital incentiva o protagonismo, a interação e a construção coletiva do conhecimento.

## Fluxo da Aplicação 
 <p><img src="/assets/fluxograma.png"></p>

> **Atenção:** Usuários cujo papel é `Aluno` não possuem acesso à recursos administrativos, ou seja, as funcionalidades de criar, editar ou deletar aulas são restritas a `Docentes`.

### Layout Proposto
A proposta é um design clean e minimalista, priorizando apenas as informações essenciais. A paleta de cores tem como destaque o amarelo, remetendo a memória do fictício Colégio Múltipla Escolha. Também é possível utilizar o dark mode.

### Breve Demonstração:
- [Vídeo](https://www.youtube.com/watch?v=GG_Lx9D9NbI)

### Proposta de testes:
Plataforma: [Portal Múltipla Escolha](https://personal-s3qu3hta.outsystemscloud.com/ME/Login)

<strong>Exemplo de Credencial Aluno (Visão Usuário):</strong><br>
<br>login
   ```
   AlunaLeticia
   ```
senha
   ```
   senhadaleticia
   ```

<strong>Exemplo de Credencial Docente (Visão Administrativa):</strong><br>
<br>login
   ```
   ProfessorOscar
   ```
senha
   ```
   senhadooscar
   ```

## Processo de Trabalho do Grupo e Desafios Encontrados
Durante o desenvolvimento do projeto, nosso grupo enfrentou alguns desafios técnicos e de design, que foram fundamentais para nosso aprendizado. Abaixo listamos os principais pontos:

- **Autenticação e Autorização:** Embora a autenticação não fosse um requisito obrigatório para esta fase, decidimos implementar uma tela de login para simular uma experiência mais próxima da realidade de um portal educacional. Nosso maior desafio foi **compreender e configurar** as `roles` dentro da plataforma `OutSystems`, definindo claramente quais funcionalidades estariam disponíveis para os `docentes` (visão administrativa) e para os `alunos` (visão de usuário). Inicialmente, optamos por deixar visíveis o ícone de edição e o botão de criação de novas postagens também para os alunos, porque esses elementos redirecionam para uma tela de aviso sobre restrição de acesso. Para etapas futuras, consideramos aprimorar essa lógica, ocultando completamente esses elementos para quem não tiver permissão.

- **Aprendizado sobre Widgets e Componentes:** Durante a implementação, percebemos que nem sempre o comportamento dos widgets era exatamente como imaginávamos. Por exemplo, acreditávamos que o widget `Expression` dentro de um `Container` quebraria o texto automaticamente ao atingir o limite do container, o que não aconteceu. Foi necessário aplicar uma estilização personalizada em CSS para resolver o problema de quebra de texto, utilizando a seguinte classe:
 ```
 .break-word {
  word-break: break-word;
  white-space: normal;
}
   ```
Essa solução garantiu que os textos se adaptassem corretamente aos espaços definidos, sem quebrar a harmonia do layout.

- **Estilo e Identidade Visual:** Optamos por um design simples, priorizando a funcionalidade. Criamos uma logo no **Canva** representando o Colégio Múltipla Escolha, e adotamos a cor amarela como elemento principal do tema, conferindo identidade ao projeto. Embora tenhamos mantido um estilo minimalista, identificamos melhorias que podem ser aplicadas nas próximas iterações, sendo elas:
<p>⛔ Classificação por Matérias: Criar um enum com as matérias para associar aos posts, exibindo como tags, facilitando a identificação e futuramente a filtragem dos conteúdos.</p>
<p>⛔ Paleta de Cores Mais Rica: Expandir a paleta para além do amarelo, tornando o visual mais atrativo e menos minimalista.</p>
<p>⛔ Melhorar a Lista de Posts: Além de título e data, exibir um pequeno resumo (excerto) do conteúdo, tornando a navegação mais agradável e informativa para os usuários.</p>

### Conclusão
Cada desafio enfrentado representou uma oportunidade de aprendizado, especialmente na exploração dos recursos da plataforma OutSystems. Estamos satisfeitos com o resultado alcançado nesta fase e motivados para aprimorar ainda mais o projeto nas próximas etapas.
<p><img src="/assets/gerar_certificado_fase.png"></p>
