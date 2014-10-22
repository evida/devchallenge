Recursos para o devchallenge do [eVida](https://www.evida.pt).
============

* [Página do concurso](https://devchallengeinfo.evida.pt)

* [Desafios propostos](https://github.com/evida/devchallenge/wiki/Desafios-propostos)

* [Wiki do eVida](https://github.com/evida/evida/wiki)

# Para testar o Hello World há que seguir os seguintes passos

As Packaged Apps precisam de ter um figueiro config.xml propriamente configurado, que é um ficheiro manifest que contém um conjunto imoportante de informação sobre a aplicação.

Aqui poderá alterar o nome da aplicação e outros campos tais como: autor, descrição, logo, entre outros:

```
<?xml version="1.0" encoding="utf-8"?>
<widget xmlns="http://www.w3.org/ns/widgets" version="1.0.0"
        id="http://widgets.tice.ipn.pt/<id_unico>">
   <name>Hello World</name>
   <content src="index.html" />
   <icon src="icon.jpg" />
</widget>
```

O ID da aplicação está definido com o seguinte formato:

http://widgets.tice.ipn.pt/<id_unico>
onde <id_unico> deverá ser substituído por uma identificação única da sua aplicação. Este id irá ser usado pela eVida para identificar a sua aplicação, que irá atribuir o seguinte url: `https://www.evida.pt/app/<id_unico>`.
