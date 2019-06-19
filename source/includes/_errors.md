# Errors

<aside class="notice">
Esta seção de erro é armazenada em um arquivo separado
<code>includes/_errors.md</code>. Slate permite que você opcionalmente separe 
seus documentos em muitos arquivos ... apenas salve-os no<code>includes</code> 
pasta e adicioná-los ao topo do seu <code>index.md</code>'s frontmatter. 
Os arquivos estão incluídos no pedido listado.
</aside>

A API do Kittn usa os seguintes códigos de erro:


| Error Code | Significado 			 | Solução 								   |
|------------| ----------------------|-----------------------------------------|
|     400    | Solicitação incorreta | Sua solicitação é inválida. 			   |
|     401    | Não autorizado 		 | Sua chave de API está errada. 		   |
|     403    | Proibido 			 | A solicitação é apenas para admin.      |
|     404    | Não encontrado 		 | A solicitação não foi encontrado. 	   |
|     405    | Método não permitido  | Você tentou acessar um método inválido. |
|     406    | Não aceitável 		 | Solicitação com formato invaldido.      |
|     410    | Gone 				 | A solicitado foi removido de nosso serv.|
|     418    | sou um bule de chá.   | Nan 									   |
|     429    | Muitas solicitações   | Desacelere, muitas solicitação.         |
|     500    | Erro interno do serv  | Ocorreu um problema. Tente mais tarde.  | 
|     503    | Serviço indisponível  | Temporariamente off-line. 			   |



