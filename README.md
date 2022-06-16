<h1>[TUTORIAL] hospedando um site estático usando o s3 na AWS de forma gratuita 🌩🖥</h1>
<h2>[RESQUISITOS]</h2>

<ol>
    <li>Ter uma conta na AWS.</li>
    <li>Ja ter os arquivos html/css/js para fazer upload, (caso não tenha pode baixar uns exemplos no meu repositório).</li>
</ol>

<h2>[VAMOS PARA PRÁTICA!]</h2>
<p>Começarei acessando o serviço S3 dentro da AWS por isso já crie sua conta lá que é bem simples.</p>
<br>

<p><b>1ª</b> Na aba de pesquisa na parte de cima procure por s3 e clique na primeira opção da pesquisa.</p>
<img height="250" width="700" src="/src/print/1.s3.png">

<br>
<p><b>2ª</b> Na coluna à esquerda clique na opção <b>Buckets</b> e no lado direito clique na opção <b>Create bucket.</b></p>
<img height="300" width="800" src="/src/print/2.s3.png">

<br>
<p><b>3ª</b> Na nova pagina aberta você irá seguir a sequência abaixo:</p>
<ol>
    <li><b>Bucket name:</b> Insira o nome do seu bucket ex: meu-bucket-novo. obs:<em> O nome do bucket deve ser exclusivo e não deve conter espaços ou letras maiúsculas.</em></li>
    <li><b>AWS region:</b> Pode deixa a opção ja selecionada.</li>
    <li><b>Block Public Access settings for this bucket:</b> Nessa aba terá a opção <b>Block all public access</b> marcada, desmarque essa opção para seu bucket se tornar público, isso é necessário para funcionar o site estático. E marque a opção abaixo na mesma sequência com a decrição <b>"I acknowledge that the current..."</b> para confimar que o bucket será publico.</li>
    <li>Depois só ir na ultima opção da página e clicar em <b>Create bucket.</b></li>
</ol>

<br>
<p><b>4ª</b> Será criado seu bucket e estará na aba <b>Buckets</b>, no meu caso criei um bucket com o nome tutorial-site-s3.</p>
<img height="450" width="800" src="/src/print/3.s3.png">

<br>
<p><b>5ª</b> Clique no seu bucket para acessar as configurações disponíveis. Na aba já aberta <b>Objects</b> é onde você irá carregar os arquivos do site, para carregar basta clicar em <b>Upload.</b></p>

<br>
<p><b>6ª</b> Em upload você pode simplesmente arrastar os arquivos e soltar na pagina ou se preferir selecionar a pasta com os arquivos no Computador clique em <b>Add files</b> para arquivos soltos ou em <b>Add folder</b> para enviar a pasta com todos os arquivos dentro.</p>
<p>OBS: Deixar o arquivo index.html na pasta raiz do seu bucket, isso evitará problemas quando o link para acessar o site for criado.</p>
<img height="500" width="700" src="/src/print/4.s3.png">

<br>
<p><b>7ª</b> Depois é só clicar na última opção <b>Upload</b> para carregar os arquivos no bucket.</p>

<br>
<p><b>8ª</b> Agora retorne para a pagina inicial das configurações do seu bucket e clique na aba <b>Permissions.</b></p>
<img height="400" width="650" src="/src/print/5.s3.png">

<br>
<p><b>9ª</b> Descendo a pagina encontre a opção <b>Bucket policy</b> e clique em <b>Edit.</b> No campo de <b>Policy</b> copie e cole o codígo JSON abaixo: </p>
<p><a href="https://github.com/abimaellsilva/aws-s3-site-estatico/blob/main/policy-s3.json">Clique aqui para abrir arquivo JSON</a></p>

<p>OBS: No codigo na linha <b>"Resource": "arn:aws:s3:::nome-do-seu-bucket/*"</b> colocar o nome do seu bucket no caso o meu ficou assim <b>"Resource": "arn:aws:s3:::tutorial-site-s3/*"</b></p>
<img height="490" width="630" src="/src/print/6.s3.png">

<p>Apague o código que aparece automaticamante e copie o seu codigo JSON informado acima. Depois só clicar em <b>Save changes</b> para salvar.</p>

<br>
<p><b>10ª</b>Agora nas aba de cima clique em <b>Properties.</b></p>
<img height="420" width="730" src="/src/print/7.s3.png">
<p>Encontre a opção <b>Static website hosting</b> e clique em <b>Edit.</b></p>

<br>
<p><b>11ª</b> Na nova pagina "Edit static website hosting" aberta você irá seguir a sequência abaixo:</p>
<ol>
    <li><b>Static website hosting:</b> Selecione a opção <b>Enable.</b></li>
    <li><b>Hosting type:</b> Pode deixar a opção <b>Host a static website</b> selecionada.</li>
    <li><b>Index document:</b> Digite o seu arquivo index.html</li>
    <li><b>Error document - optional:</b> Caso tenha o arquivo de error.html pode infomar nessa opção caso não tenha pode ignorar.</li>
    <li>Depois só ir na ultima opção da página e clicar em <b>Save changes.</b></li>
</ol>

<br>
<p><b>12ª</b> Ainda na Aba Properties em <b>Static website hosting</b> na última opção em <b>Bucket website endpoint</b> foi criado um link para acesso ao seu site estático.</p>
<p>Para acessar seu site basta clicar no link criado.</p>
<img height="350" width="830" src="/src/print/8.s3.png">
<p>Pronto! Seu site está online agora. ✅</p>

