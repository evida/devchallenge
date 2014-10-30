Recursos para o devchallenge do [eVida](https://www.evida.pt).
============

* [Página do concurso](https://devchallengeinfo.evida.pt)

* [Desafios propostos](https://github.com/evida/devchallenge/wiki/Desafios-propostos)

* [Wiki do eVida](https://github.com/evida/evida/wiki)

# Para testar o Hello World há que seguir os seguintes passos


### 1- Definir id da aplicação


As Packaged Apps precisam de ter um ficheiro config.xml configurado correctamente (de acordo com o [standard de Widgets da W3C](http://www.w3.org/TR/widgets/) , que é um ficheiro *manifest* que contém um conjunto importante de informação sobre a aplicação.

Aqui poderá alterar o nome da aplicação e outros campos tais como: autor, descrição, logótipo, entre outros:

```
<?xml version="1.0" encoding="utf-8"?>
<widget xmlns="http://www.w3.org/ns/widgets" version="1.0.0"
        id="http://widgets.tice.ipn.pt/<id_unico>">
   <name>Hello World</name>
   <content src="index.html" />
   <icon src="icon.jpg" />
</widget>
```

O ID da aplicação é definido com o seguinte formato:

`http://widgets.tice.ipn.pt/<id_unico>`,
onde `<id_unico>` deverá ser substituído por uma identificação única da sua aplicação. Este id irá ser usado pela eVida para identificar a sua aplicação, que irá atribuir o seguinte url: `https://www.evida.pt/app/<id_unico>`.

### 2- Obter token OAuth

Para obter as informações do utilizador é necessário aceder à area "Developer:

Localizado na *sidebar*, e escolher "API access", ou aceder a [https://www.evida.pt/dashboard/api-access](https://www.evida.pt/dashboard/api-access). 

Aí, clicando em "Create another Oauth Consumer", preenchendo e submentendo o formulário obtêm-se as chaves "Consumer Key" e "Consumer Secret"

Neste caso, apenas nos interessa o "Consumer Key", que devemos usar para substituir <consumer_key> no ficheiro index.html 

```
  var qs = {
        ...
      	consumer_key: '<consumer_key>'
        ...
  };
```
