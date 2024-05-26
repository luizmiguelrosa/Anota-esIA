<h1 align="center">Reconhecimento de Voz</h1>

<p align="justify">Ao longo dos últimos cinco anos, percebi que a área de reconhecimento de voz apresenta grandes limitações, frequentemente se restringindo a bibliotecas padrão, como **speechrecognition**, e a modelos offline com pouca contribuição da comunidade. As opções são: usar modelos consolidados que necessitam de internet, usar modelos imprecisos mas sem a necessidade de conexão, ou treinar um modelo do zero.</p>

## Modelos em Nuvem

<p align="justify">A biblioteca speechrecognition é particularmente problemática nesta área, pois depende de processamento externo em nuvem, como os serviços da Google ou IBM, o que resulta em atrasos no reconhecimento de voz. Embora esses métodos de processamento em nuvem sejam mais precisos, a experiência do usuário pode ser prejudicada em situações que exigem respostas imediatas.</p>

## Modelos Offline

<p align="justify">Existem métodos offline, como **Vosk** e **Pocketsphinx**, que permitem realizar o processamento de forma mais rápida e sem a necessidade de uma conexão com a internet. No entanto, a dificuldade está em encontrar modelos de reconhecimento de voz treinados para esses métodos, especialmente em Português.</p>

<p align="justify">No site oficial do Vosk, estão disponíveis dois modelos em Português: um para aplicações mais simples e outro para aplicações mais variadas. O modelo mais avançado é o segundo, mas ele está organizado em arquivos que o Vosk do Python não consegue ler automaticamente, exigindo uma organização manual. Para o Pocketsphinx, existe o modelo do Fala Brasil, que é uma continuação de um projeto anteriormente abandonado. Tanto no Vosk quanto no Pocketsphinx, os melhores modelos disponíveis são do projeto Fala Brasil.</p>

## Treinamento de Modelo

<p align="justify">Treinar um modelo do zero é extremamente custoso e requer um conhecimento profundo da gramática da língua do modelo. Também é necessário saber lidar com as entradas dos áudios para desenvolver um método eficaz de treinamento do modelo.</p>

<p align="justify">Desenvolver esses métodos de treinamento já se mostrou inviável, considerando os conhecimentos necessários, como matemática discreta, álgebra linear, entre outros. Portanto, o uso de ferramentas prontas é fundamental para ajudar no processo, diminuindo o gargalo inicial da pesquisa.</p>

<p align="justify">Dependendo do conjunto de palavras, a saída pode ser diferente. Voltando ao exemplo da <a href="/anotacoes/processamento-de-entradas.MD">operação aritmética</a>, precisamos que os dados da operação sejam convertidos para formato numérico; por exemplo, ao invés de "dois", o resultado deve ser "2". Isso pode parecer óbvio, mas se não considerarmos o contexto inteiro da frase, o modelo não saberá diferenciar corretamente entre números e texto.</p>