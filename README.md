# Projeto-DIO-Ransonware

<p> Neste projeto, documentarei e registrarei todos os procedimentos desde a construção do ransonware, até a dissecação e o entendimento sobre como o malware se manifesta, funciona e como podemos nos proteger. </p>

<p>  →→→→ Aviso Importante ←←←←
  <br>
Este projeto foi desenvolvido exclusivamente para fins educacionais, no contexto do Bootcamp da Digital Innovation One (DIO).
Todo o código aqui presente deve ser utilizado apenas em ambiente controlado, com autorização e para fins de estudo.
O uso indevido deste tipo de software é crime, previsto pela legislação brasileira (Lei 12.737/2012 — Lei Carolina Dieckmann).</p>

<h3>Objetivo do Projeto</h3>

<p>Este repositório apresenta uma simulação controlada de um ransomware, com o propósito de demonstrar:</p>

<ul>
  <li>Funcionamento básico de criptografia simétrica (Fernet);
  <li>Geração e carregamento de chaves de criptografia;</li>
  <li>Escrita de mensagem de aviso (simulação de nota de resgate);</li>
  <li>Comportamento típico de malwares modernos, analisado de forma segura.</li>
</ul>

<h4>Funcionamnto padrão do malware</h4>

<ol>
  
  <li> <strong>Importação de biblioteca e geração de chave </strong><br>
  <ul>
    <li>Utilização e importação da criptografia vindo da biblioteca Fernet</li> 
    <li>Gera um arquivo chave com criptografia em fernet</li>
  </ul>
  </li>

   
  <li> <strong>Carregamento da chave </strong><br>
  <ul>
    <li>Após a criação da função de carregar a chave, retorna e realiza o carregamento da chave criptografada</li> 
  </ul>
  </li>


   <li> <strong>Lógica de Encriptação dos arquivos </strong><br>
  <ul>
    <li>Criptografa os arquivos e embaralha todas as escritas presentes nos arquivos</li> 
  </ul>
  </li>
  

   <li> <strong> Localização dos arquivos e criptografando-os </strong><br>
  <ul>
    <li>Com uma função lista, percorremos os diretórios da vítima com um array em lista </li> 
  </ul>
  </li>

 <li> <strong>Criação da mensagem de resgate</strong><br>
  <ul>
    <li>Ao término da encriptação de todos os arquivos, é gerado uma tela contendo as informações para que o usuário envie a requisição para o atacante para ter os seus arquivos devolvidos (e muitas das vezes o atacante devolve porcentagens desses arquivos
    ou nem devolvem.</li> 
  </ul>
  </li>

 <li> <stronge> Execução Principal e confirmação </strong><br>
  <ul>
    <li>A estrutura principal do ransonware, é nessa parte do script que confirma a geração da chave, o carregamento, 
  a procura de arquivos, encriptação deles e a geração da mensagem de resgate, caso sucesso, a função "main" é chamada.</li> 
  </ul>
  </li>

</ol>


<ul>
  <li>Funcionamento básico de criptografia simétrica (Fernet);
  <li>Geração e carregamento de chaves de criptografia;</li>
  <li>Escrita de mensagem de aviso (simulação de nota de resgate);</li>
  <li>Comportamento típico de malwares modernos, analisado de forma segura.</li>
</ul>

<h4>Descriptografando arquivos </h4>

<ol>
  
  <li> <strong>Carregamento da chave </strong><br>
  <ul>
    <li>Importa o cryptography.fernet e faz o carregamento da chave </li> 
  </ul>
  </li>


  <li> <strong>Lógica de descriptografia </strong><br>
  <ul>
    <li>Aplica a lógica reversa da criptografia, descriptografando os dados dos arquivos </li> 
  </ul>
  </li>


  <li> <strong>Busca de arquivos</strong><br>
  <ul>
    <li>Busca todos os arquivos em uma lista, semelhante a função de criptografar os arquivos e aplica a função
    para todos os arquivos encriptografados</li> 
  </ul>
  </li>
  

   <li> <strong>Recuperação e </strong><br>
  <ul>
    <li>Aplica a lógica reversa da criptografia, descriptografando os dados dos arquivos </li> 
  </ul>
  </li>
   
   


</ol>


<p>Uma das formas de se proteger diante de um ransonware, é manter o antivírus atualizado, o sistema operacional atualizado e jamais clicar em links suspeitos ou arquivos que não conhecemos.</p>



<h4>Keylogger</h4>

<p>Um keylogger é um tipo de software (ou hardware) que registra pressionamentos de teclas do utilizador. Em contexto malicioso, serve para capturar credenciais, mensagens, dados financeiros e outras informações sensíveis. Em contexto defensivo ou de pesquisa, keyloggers são estudados para entender vetores de ataque e desenvolver detecções.</p>


<h4>Como se proteger dos keyloggers?</h4>

<ul>
  <li>Usar sempre antivírus</li>
  <li>Evite inicializar macros suspeitos</li>
  <li>Atualizar sempre o sistema operacional de sua escolha</li>
  <li>Usar sempre autenticação em dois fatores</li>
</ul>
<br>
<br>

<h4>Reflexão sobre o projeto.</h4>

<p>O estudo e a experimentação prática com ransomware e keyloggers em ambientes controlados revelam muito mais do que simplesmente a construção de códigos maliciosos — eles expõem a fragilidade natural dos sistemas digitais e a importância crescente da cibersegurança como disciplina e como postura.

Ransomwares representam a face mais evidente e agressiva das ameaças modernas: são ruidosos, destrutivos e têm impacto direto e mensurável. Em poucos segundos, conseguem paralisar empresas inteiras, comprometer operações críticas e causar prejuízos financeiros e reputacionais irreversíveis. Ao analisar a lógica interna de um ransomware — desde a enumeração de diretórios até a criptografia dos arquivos-alvo — fica evidente que a força desse tipo de ataque não está apenas na sofisticação técnica, mas na previsibilidade do comportamento humano. Basta um clique incorreto, um anexo aberto ou uma atualização ignorada para que a cadeia de ataque seja disparada.</p>
<p> A reflexão final que fica é clara:

Entender como ataques funcionam é a melhor forma de aprender como se defender.

Estudar, construir e analisar esses códigos não é um exercício de destruição, mas sim de conscientização. É compreender a lógica do adversário para reforçar nossas próprias estruturas. É assumir que vulnerabilidades existem — e sempre existirão —, mas que cabe a nós, como profissionais ou estudantes de segurança, transformar conhecimento técnico em barreiras reais contra o cibercrime.

No fim, trabalhar com ransomware e keyloggers dentro de um laboratório não nos transforma apenas em melhores técnicos, mas em analistas mais completos, mais críticos e mais preparados para atuar em um cenário onde as ameaças evoluem diariamente.</p>
