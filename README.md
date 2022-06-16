<h1>[TUTORIAL] hospedando um site estático no aws s3 de forma gratuita</h1>
<h2>[RESQUISITOS]</h2>

<ol>
    <li>Ter uma conta na AWS.</li>
    <li>Ja ter os arquivos html/css/js para fazer upload, (caso não tenha pode baixar uns exemplos no meu repositório).</li>
</ol>

<h2>[VAMOS PARA PRÁTICA!]</h2>
<p>Começarei acessando o serviço S3 dentro da AWS por isso já crie sua conta lá que é bem simples.</p>
<br>

<p><b>1ª</b> Na aba de pesquisa na parte de cima procure por s3 e clique na primeira opção da pesquisa</p>
<img height="250" width="750" src="/src/print/1.s3.png">

<br>
<p><b>2ª</b> Na coluna à esquerda clique na opção <b>Buckets</b> e no lado direito clique na opção <b>Create bucket.</b></p>
<img height="250" width="750" src="/src/print/2.s3.png">

<br>
<p><b>3ª</b> Na nova pagina aberta você irá seguir a sequência abaixo:</p>
<ol>
    <li><b>Bucket name:</b> Insira o nome do seu bucket ex: meu-bucket-novo. obs:<em> O nome do bucket deve ser exclusivo e não deve conter espaços ou letras maiúsculas.</em></li>
    <li><b>AWS region:</b> Pode deixa a opção ja selecionada</li>
    <li><b>Block Public Access settings for this bucket:</b> Nessa aba terá a opção <b>Block all public access</b> marcada, desmarque essa opção para seu bucket se tornar público, isso é necessário para funcionar o site estático. E marque a opção abaixo na mesma sequência com a decrição <b>"I acknowledge that the current..."</b> para confimar que o bucket será publico.</li>
    <li>Depois só ir na ultima opção da página e clicar em <b>Create bucket.</b></li>
</ol>

<br>
<p><b>4ª</b> Será criado seu bucket e estará na aba <b>Buckets</b>, no meu caso criei um bucket com o nome tutorial-site-s3.</p>
<img height="400" width="750" src="/src/print/3.s3.png">

