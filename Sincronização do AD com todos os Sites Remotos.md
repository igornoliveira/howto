## Forçar Sincronização do Microsoft AD Com Todos os Sites Remotos

Este é um  comando interessante caso haja algum problema com a replicação automática dos sites remotos do AD.
Ele força a replicação do AD primário para todos os sites.
O comando deve ser feito à partir do AD Primário. Na tela de Prompt do MS-Dos, entre com o comando abaixo:

```
repadmin /syncall /e /A /P /d /q
```

#### Aqui cada um dos parâmetros explicados:

* /syncall: Sincroniza o domain controller principal com todos os parceiros de replicação;

* /e: Enterprise… indica que a replicação será estendida a todos os sites remotos;

* /A:  All; Sincroniza todas as partições do home server;

- /P: Indica que as mudanças serão replicadas a partir do servidor primário;

- /d: Identifica os servidores por seus nomes distintos em eventuais mensagens que possam aparecer;

- /q: Quiet mode. Não mostra as mensagens de status. Caso você esteja fazendo isso manualmente por algum problema, é melhor não usar este parâmetro para identificar algum erro.

## Verificando o status da replicação do Active Directory (AD)

#### Repadmin 

Digite o comando **repadmin /showreps** e aperte Enter.

```
repadmin /showreps > nomedoarquivo.txt
```

Existem outros comandos do repadmin, são eles: 

1. Mostra a estatísca das replicações.

    ```
    Repadmin /replsummary
    ```

2. Mostra informações sobre replicações entre sites.

    ```
    Repadmin /showism
    ```

#### Dcdiag

Digite dcdiag **/test:replications** e aperte Enter.

dcdiag /test:replications > nomedoarquivo.txt

Outro commando importante do dcdiag é dcdiag /test:dns que apresenta um relatório sobre o estado do DN.

Lembre-se: Para gerar um arquivo .txt na raíz do C: digite cd / 