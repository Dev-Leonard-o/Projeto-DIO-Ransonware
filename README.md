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

 <li> <strong>Lógica, execução e confirmação </strong><br>
  <ul>
    <li>A estrutura principal do ransonware, é nessa parte do script que confirma a geração da chave, o carregamento, 
  a procura de arquivos, encriptação deles e a geração da mensagem de resgate, caso sucesso, a função "main" é chamada.</li> 
  </ul>
  </li>
  
</ol>
