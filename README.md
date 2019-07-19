# Entity
Register of employees using Entity Framework. References in portuguese.

---------------------------------

Especificações:

MVC: Model, View, Controller

onde

Models - Classes que representam os dados da aplicação e que usa a lógica de validação para impor as regras de negócio para os dados;

Views - Arquivos Templates que sua aplicação usa para gerar resposta HTML dinâmica;

Controller - Classes que tratam as requisições do navegador, retornam os dados e então especificam templates views que retornam a resposta ao navegador para apresentação do resultado;
Inicialmente o projeto foi realizado sem a utilização do ADO.NET;
Após problemas no Visual Studio e de ter encontrado um artigo falando sobre o ADO.NET, este foi utilizado;
Foi necessário pesquisar sobre a utilização do HTML por ter esquecido alguns conceitos;

Referente aos Helpers - HTML

url.Action e HTML.ActionLink são Helpers e ambos tem a função de gerar links baseados nas rotas definidas na configuração da aplicação.
O redirecionamento é feito no controller usando RedirectToAction(). O 1º permite que uma lógica seja montada usando o link gerado de 
acordo com a rota Ex:

<a href="@Url.Action("MinhaAction", "MeuController")">
    <div class="meu-botao">
        <img src="@Url.Content("~/Images/minha-imagem.jpg")" />
        Um texto dentro do botão
    </div>
</a>

O segundo gera uma tag <a> com texto simples dentro e alguma configuração como controller, as tokens de rota e alguma configuração HTML como 
class e id. Ex comparativo:

@Html.ActionLink("Link", "action", "controller", new { id = "123" }, null)

Resultado:

<a href="/controller/action/123">Link</a>

JÁ url.Action:

Url.Action("action", "controller", new { id = "123" })

Resultado:

/controller/action/123 

O motor de views de ambos é o RAZOR (permite a existência de código C# misturado com HTML.

Associado ao Model-First - Entity Framework 4.1, abordagem que permite modelar a base de dados de forma visual.


Referências:

treinaweb.com.br
macoratti.net
youtube.com
programandodornet.wordpress.com
github.com
devmedia.com.br


 


