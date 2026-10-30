# LETCOOR 1.0.0 — Documentação completa do utilizador

> Documentação elaborada a partir do código-fonte real do **LETCOOR 1.0.0** fornecido em 30 de outubro de 2026.
> Esta documentação descreve as funções realmente disponibilizadas pela aplicação Android/Windows e pela interface atual.

---

## Índice

1. [Primeiros passos: ligar os dispositivos](#1-primeiros-passos-ligar-os-dispositivos)
2. [Permissões importantes, sobretudo offline](#2-permissões-importantes-sobretudo-offline)
3. [Criar ou entrar num grupo](#3-criar-ou-entrar-num-grupo)
4. [Compreender o ecrã principal](#4-compreender-o-ecrã-principal)
5. [O mapa tático](#5-o-mapa-tático)
6. [Criar uma sinalização](#6-criar-uma-sinalização)
7. [Criar um objetivo](#7-criar-um-objetivo)
8. [Criar uma ordem](#8-criar-uma-ordem)
9. [Criar um ponto de reunião](#9-criar-um-ponto-de-reunião)
10. [Enviar um alerta de segurança](#10-enviar-um-alerta-de-segurança)
11. [Interagir com um objeto já publicado](#11-interagir-com-um-objeto-já-publicado)
12. [O painel «Comando e atividade»](#12-o-painel-comando-e-atividade)
13. [O menu do grupo ou da equipa](#13-o-menu-do-grupo-ou-da-equipa)
14. [Equipas](#14-equipas)
15. [Participantes e funções](#15-participantes-e-funções)
16. [Convidar um novo participante](#16-convidar-um-novo-participante)
17. [Operações](#17-operações)
18. [Campanhas de funções](#18-campanhas-de-funções)
19. [Sessões](#19-sessões)
20. [Partilha de dados entre equipas](#20-partilha-de-dados-entre-equipas)
21. [Gestão do grupo e das equipas](#21-gestão-do-grupo-e-das-equipas)
22. [Limites de publicação](#22-limites-de-publicação)
23. [Localização](#23-localização)
24. [Notificações](#24-notificações)
25. [Mapas offline](#25-mapas-offline)
26. [Ligação de rede e funcionamento offline](#26-ligação-de-rede-e-funcionamento-offline)
27. [Privacidade, bloqueio e recuperação](#27-privacidade-bloqueio-e-recuperação)
28. [Funções disponíveis](#28-funções-disponíveis)
29. [Conselhos de preparação antes de uma atividade](#29-conselhos-de-preparação-antes-de-uma-atividade)
30. [Resolução de problemas](#30-resolução-de-problemas)
31. [Resumo rápido](#31-resumo-rápido)

---

# 1. Primeiros passos: ligar os dispositivos

O LETCOOR utiliza um sistema de convites entre dispositivos. Um convite pode ser transmitido por **código QR**, **ligação**, partilha do sistema ou ficheiro, consoante a plataforma.

Para maximizar as hipóteses de ligação, sobretudo **sem Internet**, prepare os dois dispositivos antes da troca.

## 1.1 Antes de digitalizar o código QR ou abrir a ligação

Nos dois dispositivos:

1. Abra o LETCOOR e mantenha a aplicação em primeiro plano durante a primeira ligação.
2. Ative o **Wi‑Fi**.
3. Ative o **Bluetooth**.
4. Aceite os pedidos do Android/Windows relativos a **dispositivos próximos**, Bluetooth, Wi‑Fi Direct ou rede local.
5. Se o Android propuser tornar o telefone visível por Bluetooth, aceite durante a fase de ligação.
6. Se o Android pedir para ativar o serviço de localização para permitir a deteção por rádio, recomenda-se que o ative para garantir a compatibilidade com as API de proximidade do telefone.
7. A **câmara** só é necessária para digitalizar um código QR. Não é necessária se utilizar uma ligação.

> **Importante:** autorizar ou ativar o serviço de localização do Android para a descoberta por proximidade não ativa automaticamente a partilha da sua posição no LETCOOR. A partilha de localização é uma função separada e permanece desativada enquanto não a ativar manualmente.

## 1.2 Ligação por código QR

### No dispositivo que convida

1. Abra o menu do grupo ou da equipa tocando no respetivo nome no canto superior esquerdo.
2. Abra o separador **Convidar**.
3. Se estiverem disponíveis vários destinos, escolha o **grupo** ou a **equipa** a que se pretende aderir.
4. Abra **Partilhar convite**.
5. Selecione **Mostrar código QR**.
6. Mantenha o QR visível no ecrã.

Um QR pode ser composto por várias partes. O LETCOOR percorre-as automaticamente. É possível pausar a passagem ou avançar manualmente para a parte anterior/seguinte.

### No dispositivo convidado

1. No ecrã inicial, escolha **Entrar com um convite**.
2. Prima o botão de digitalização do QR.
3. Autorize a câmara se o Android/Windows o solicitar.
4. Aponte para o QR do outro dispositivo.
5. Se o QR tiver várias partes, mantenha a câmara apontada para o ecrã até o LETCOOR ter lido todas as partes.
6. O LETCOOR importa o convite e prepara uma **resposta**.
7. O dispositivo convidado apresenta então uma **ligação de resposta** ou um **QR de resposta** que deve ser devolvido ao dispositivo que convidou.

### Devolver a resposta ao dispositivo que convidou

No dispositivo que criou o convite:

1. Permaneça em **Convidar**.
2. Abra **Receber a resposta**.
3. Digitalize o QR de resposta, cole a ligação de resposta ou utilize o mecanismo de partilha disponível.
4. O LETCOOR verifica a resposta e inicia depois a ligação direta.

A aplicação apresenta em seguida o estado da tentativa: preparação de proximidade, ligação à Internet, procura local, ligação estabelecida ou tempo limite excedido.

## 1.3 Ligação por ligação

O procedimento é idêntico, mas sem câmara.

### Dispositivo que convida

Em **Convidar > Partilhar convite**:

1. Escolha **Ligação de convite**.
2. Prima **Copiar ligação** ou o botão de partilha.
3. Envie a ligação ao outro participante.

### Dispositivo convidado

1. Abra **Entrar com um convite**.
2. Cole a ligação em **Convite a aceitar**, ou utilize o botão da área de transferência.
3. O LETCOOR processa automaticamente uma ligação válida.
4. Em seguida, devolva a **ligação de resposta** ao dispositivo que o está a convidar.

### Dispositivo que convida

Em **Receber a resposta**:

1. Cole a ligação de resposta ou digitalize o QR de resposta.
2. O LETCOOR verifica a resposta.
3. A ligação inicia-se automaticamente.

## 1.4 Porque é necessário devolver uma resposta?

O fluxo bidirecional permite que os dois dispositivos conheçam as informações necessárias para a tentativa de ligação. O LETCOOR pode então testar os caminhos disponíveis e autenticar o par antes da admissão no grupo ou na equipa.

## 1.5 Admissão no grupo e na equipa

Um convite válido é assinado e aponta para um destino definido no momento da sua criação.

- Um convite de grupo permite entrar no grupo correspondente.
- Um convite proveniente de uma equipa pode incluir acesso ao **grupo principal e à equipa de quem convida**.
- As chaves privadas do grupo ou o histórico completo não são colocados no código QR.
- A admissão é validada pelo protocolo LETCOOR após a autenticação; não existe validação manual adicional para um convite válido, salvo se a política de admissão ou as permissões do espaço o impedirem.

---

# 2. Permissões importantes, sobretudo offline

O LETCOOR utiliza várias funções do sistema. Para utilização sem Internet, as permissões de proximidade são particularmente importantes.

## 2.1 Bluetooth e Wi‑Fi Direct

Em **Definições > Permissões**, o LETCOOR disponibiliza:

- **Bluetooth e Wi‑Fi Direct — Permitir**
- **Câmara — Permitir**
- **Localização — Verificar**

Em versões recentes do Android, o LETCOOR pode pedir, nomeadamente, permissões do sistema relacionadas com:

- dispositivos próximos;
- pesquisa Bluetooth;
- ligação Bluetooth;
- anúncio Bluetooth;
- Wi‑Fi Direct / dispositivos Wi‑Fi próximos;
- acesso à rede local nas versões Android que o exigem.

Em algumas versões antigas do Android, a descoberta Bluetooth/Wi‑Fi pode depender da permissão de localização do Android.

## 2.2 Localização: duas coisas diferentes

É necessário distinguir entre:

1. **A localização do sistema Android utilizada por algumas API de descoberta por proximidade.**
2. **A partilha voluntária da sua posição no LETCOOR.**

Pode utilizar o LETCOOR sem publicar a sua posição no mapa. A partilha de localização é configurada separadamente através do ícone **Localização**.

## 2.3 Câmara

A câmara serve apenas para digitalizar códigos QR. A digitalização não requer o microfone.

Se o acesso à câmara for recusado:

- utilize a ligação de convite;
- ou volte a autorizar a câmara nas definições do Android/Windows.

## 2.4 Notificações do sistema

As notificações do sistema podem ser ativadas a partir do centro de notificações do LETCOOR. Permitem receber alertas nativos para determinados eventos quando a plataforma o permite.

---

# 3. Criar ou entrar num grupo

No primeiro arranque, se o dispositivo ainda não tiver nenhum grupo, o LETCOOR apresenta o ecrã inicial.

Tem duas opções:

- **Criar um grupo**
- **Entrar com um convite**

## 3.1 Criar um grupo

1. Prima **Criar um grupo**.
2. Introduza o **Nome do grupo**.
3. O nome deve conter pelo menos 2 caracteres.
4. Prima **Criar**.

O criador recebe a função de administração do grupo e pode depois criar equipas, convidar participantes e gerir o espaço de acordo com as capacidades concedidas pelo Core.

## 3.2 Entrar num grupo

1. Prima **Entrar com um convite**.
2. Importe a ligação ou o QR.
3. Siga a troca convite/resposta descrita no início desta documentação.

## 3.3 N.º pessoal

Cada dispositivo possui um **N.º pessoal** apresentado durante a integração inicial e no separador **Contexto**.

Este número funciona como identificador legível pelo utilizador na interface. A identidade criptográfica real baseia-se na identidade do dispositivo LETCOOR e não neste código apresentado.

---

# 4. Compreender o ecrã principal

O LETCOOR utiliza uma interface **centrada no mapa** em vez de uma sucessão de páginas clássicas.

## 4.1 Cabeçalho

Na parte superior do ecrã:

- à esquerda: o **nome do grupo ou da equipa atualmente selecionado**;
- o subtítulo indica **Grupo** ou **Equipa**;
- pode aparecer o estado **Não sincronizado** se o contexto estiver a funcionar sem sincronização;
- um sino abre as **Notificações**;
- o botão **Comando** abre o painel de comando e atividade;
- um indicador mostra o estado da rede: Internet direta, retransmissão, Wi‑Fi Direct, Wi‑Fi local, Bluetooth, LAN, sincronização ou procura de ligação.

## 4.2 Mapa central

O mapa apresenta os objetos autorizados no contexto atual:

- ordens;
- sinalizações;
- objetivos;
- encontros / pontos de reunião;
- alertas de segurança;
- presença de equipa;
- presença exata quando autorizada;
- movimentos / trajetórias consoante os direitos e as partilhas ativas.

## 4.3 Legenda

O botão `?` apresenta a legenda, nomeadamente:

- Perigo;
- Objetivo;
- Ponto de reunião;
- Equipa.

## 4.4 Rodapé

A parte inferior do ecrã indica:

- o número de membros ativos no contexto;
- o número de objetos ativos;
- a eventual presença de uma sessão em curso; caso contrário, o seu N.º pessoal.

## 4.5 Abrir o menu do grupo ou da equipa

Toque no nome do contexto no canto superior esquerdo.

O painel contém os separadores:

- **Contexto**
- **Equipas**
- **Participantes**
- **Convidar**
- **Operações**
- **Gestão**
- **Definições**

Algumas funções só aparecem se a sua função tiver a permissão correspondente.

---

# 5. O mapa tático

## 5.1 Deslocar-se

O mapa é utilizado como um mapa tátil clássico: deslocamento e zoom.

## 5.2 Adicionar um objeto

Para publicar um objeto espacial:

1. Faça uma **pressão prolongada** no local pretendido.
2. O LETCOOR abre **Adicionar aqui**.
3. São apresentadas as ações autorizadas para a sua função.

As possibilidades são:

- **Sinalização**
- **Objetivo**
- **Ordem**
- **Ponto de reunião**
- **Alerta de segurança**

As ações não autorizadas no seu contexto não são apresentadas.

## 5.3 Formas geográficas

Consoante o tipo de objeto, o LETCOOR permite:

- **Ponto**;
- **Zona circular**;
- **Polígono**;
- **Traçado**.

Para uma zona circular, o raio pode ser ajustado de **10 a 500 m**.

Para um polígono ou um traçado:

1. escolha a geometria;
2. prima **Desenhar no mapa**;
3. adicione os vértices no mapa;
4. utilize **Anular o último**, **Terminar** ou **Cancelar**.

O número de pontos é limitado pela interface.

## 5.4 Duração / prazo

Os objetos espaciais que não sejam de segurança podem receber uma duração entre **5 e 360 minutos**, em passos de 5 minutos.

---

# 6. Criar uma sinalização

1. Faça uma pressão prolongada no mapa.
2. Escolha **Sinalização**.
3. Selecione o tipo.
4. Introduza opcionalmente um nome e uma descrição.
5. Escolha a geometria e a duração.
6. Prima **Publicar**.

## Tipos de sinalização disponíveis

- Perigo
- Obstáculo
- Rota bloqueada
- Passagem impraticável
- Passagem aberta
- Adversário observado
- Grupo observado
- Movimento observado
- Problema de equipamento
- Personalizado

Consoante a sua função, uma sinalização pode ser publicada dentro da equipa ou ao nível do grupo.

Os batedores e responsáveis com as permissões necessárias podem, nomeadamente, confirmar, contestar, resolver ou promover determinadas sinalizações.

---

# 7. Criar um objetivo

1. Faça uma pressão prolongada no mapa.
2. Escolha **Objetivo**.
3. Introduza **Objetivo a realizar**.
4. Escolha o tipo.
5. Escolha a prioridade.
6. Selecione a geometria.
7. Defina o prazo.
8. Prima **Publicar**.

## Tipos de objetivo

- Alcançar um ponto
- Manter uma zona
- Capturar uma zona
- Recuperar um objeto
- Chegar a um encontro
- Observar uma zona
- Personalizado

## Objetivo de equipa ou objetivo final do grupo

Quando a função e o contexto o permitem, o formulário permite escolher:

- **Todo o grupo — objetivo final**;
- **Esta equipa — objetivo de equipa**.

O objetivo final é visível para os membros do grupo e para as equipas de acordo com as regras de autorização do Core.

## Prioridades

A interface disponibiliza:

- P0 — Urgente
- P1 — Alta
- P2 — Normal
- P3 — Baixa

---

# 8. Criar uma ordem

1. Faça uma pressão prolongada no mapa.
2. Escolha **Ordem**.
3. Introduza a instrução personalizada, se necessário.
4. Escolha o tipo de ordem.
5. Escolha a prioridade.
6. Pode associar a ordem a um **objetivo** existente.
7. Pode associar a ordem a um **encontro** existente.
8. Se necessário, o LETCOOR permite criar diretamente um objetivo ou um encontro no mesmo local e depois regressar à ordem.
9. Escolha a geometria e a duração.
10. Prima **Publicar**.

## Tipos de ordem

- Deslocar-se
- Reagrupar-se
- Manter a posição
- Avançar
- Recuar
- Defender
- Observar
- Proteger um objetivo
- Personalizado

## Ordem do chefe de grupo

Quando a publicação é uma ordem de comando do grupo, o chefe de grupo escolhe as **equipas destinatárias**. O código operacional prevê que este tipo de ordem se destine aos chefes das equipas selecionadas.

## Ordem de equipa

Um chefe de equipa pode criar ordens dentro da sua equipa. Uma ordem de equipa também pode ser associada a uma ordem de comando principal quando essa relação estiver disponível.

---

# 9. Criar um ponto de reunião

1. Faça uma pressão prolongada no mapa.
2. Escolha **Ponto de reunião**.
3. Dê-lhe um nome curto.
4. Escolha um **Ponto** ou uma **Zona circular**.
5. Defina a duração / prazo.
6. Publique.

O ponto de reunião cria um encontro que também pode ser utilizado como referência por uma ordem.

---

# 10. Enviar um alerta de segurança

O alerta de segurança é uma publicação prioritária.

1. Faça uma pressão prolongada no mapa.
2. Escolha **Alerta de segurança**.
3. Introduza uma mensagem, se necessário.
4. Escolha o tipo.
5. Prima **Enviar alerta**.

## Tipos disponíveis

- Ferimento
- Interromper a atividade
- Perigo
- Pessoa desaparecida
- Outra emergência

Um alerta personalizado exige uma mensagem.

O LETCOOR lembra na interface que o alerta P0 deve ser utilizado em caso de perigo ou necessidade de ajuda.

Consoante as permissões, um responsável pode depois **Marcar como resolvido**.

---

# 11. Interagir com um objeto já publicado

Toque num objeto do mapa para abrir a respetiva ficha.

As ações propostas dependem do tipo de objeto e das suas permissões.

## Sinalização

Ações possíveis:

- Confirmar
- Contestar
- Resolver
- Prolongar por 15 min
- Cancelar a sinalização
- Promover ao grupo, quando a sinalização provém de uma equipa e a função o permite

Para determinados objetos operacionais, o LETCOOR também pode disponibilizar:

- **Confirmar no terreno**;
- **Votar para resolver**;
- **Assinalar passagem aberta**;
- **Remover a informação**.

## Objetivo

Um utilizador com a permissão correspondente pode alterar o respetivo estado:

- Em curso
- Concluído
- Falhado
- Cancelado

## Ordem

Podem ser propostas respostas consoante o tipo de ordem:

- Recebida
- Aceite
- Concluída
- Impossível

O painel simplificado **Operações > Ordens** utiliza pelo menos a confirmação **Recebida** quando a ordem exige uma resposta.

## Alerta de segurança

O responsável autorizado pode escolher **Marcar como resolvido**.

---

# 12. O painel «Comando e atividade»

O botão **Comando** na parte superior do ecrã abre um painel separado destinado a operações que não estão necessariamente associadas a um ponto no mapa.

Inclui até três separadores:

- **Notificações**
- **Publicar**
- **Histórico**

Os separadores só aparecem quando têm conteúdo ou quando uma ação está autorizada.

## 12.1 Notificações

Apresenta os objetos operacionais acessíveis:

- ordem de comando;
- ordem de equipa;
- objetivo;
- objetivo final do grupo;
- anúncio;
- relatório a verificar;
- sinalização verificada.

Cada cartão pode indicar:

- texto;
- tipo;
- estado;
- equipa/grupo;
- objetivo ou encontro associado;
- equipas visadas;
- confirmações de receção;
- votos;
- progresso por equipa.

Consoante a sua função, os botões podem disponibilizar:

- Recebida;
- Verificar no terreno;
- Remover;
- Marcar como lido;
- Declarar concluído;
- Votar concluído;
- Votar impossível;
- Votar resolvido;
- Resolver.

## 12.2 Publicar

O LETCOOR apresenta apenas as publicações autorizadas para a sua função e contexto.

Os tipos internos atualmente geridos pela interface incluem:

- Ordem de comando
- Ordem de equipa
- Objetivo de equipa
- Objetivo final do grupo
- Anúncio
- Relatório a verificar
- Sinalização verificada

Para uma ordem de comando, escolha as equipas destinatárias.

Para uma ordem de equipa, pode selecionar uma ordem de comando principal.

Introduza depois a descrição e prima **Publicar**.

As publicações criadas a partir deste painel utilizam atualmente uma duração operacional predefinida de cerca de 30 minutos no código da interface.

## 12.3 Histórico

Apresenta os eventos registados com a respetiva data, resumo e identificador do objeto.

---

# 13. O menu do grupo ou da equipa

Toque no nome do contexto no canto superior esquerdo.

## Separador Contexto

Apresenta:

- o seletor **Grupo ou equipa**;
- o número de membros;
- o número de dispositivos ligados;
- o estado da sessão;
- as suas funções;
- o tema Sistema / Claro / Escuro;
- o idioma;
- o seu **N.º pessoal**, que pode ser copiado.

Os idiomas atualmente disponibilizados pela interface são: **Sistema, Français, English, العربية, Deutsch e Русский**. A interface muda automaticamente para o sentido da direita para a esquerda no caso do árabe.

## Separador Equipas

Consulte [Equipas](#14-equipas).

## Separador Participantes

Consulte [Participantes e funções](#15-participantes-e-funções).

## Separador Convidar

Consulte [Convidar um novo participante](#16-convidar-um-novo-participante).

## Separador Operações

Consulte [Operações](#17-operações).

## Separador Gestão

Consulte [Gestão do grupo e das equipas](#21-gestão-do-grupo-e-das-equipas).

## Separador Definições

Contém atualmente:

- mapas offline;
- gestão das permissões Bluetooth/Wi‑Fi Direct;
- autorização da câmara;
- verificação da localização.

---

# 14. Equipas

O separador **Equipas** apresenta as equipas do grupo.

Para cada equipa, o LETCOOR mostra, nomeadamente:

- nome;
- número de membros;
- chefe de equipa;
- lista de participantes;
- o seu estado de acesso à equipa.

## Estados de acesso

- **É membro · acesso pronto**
- **Adesão registada · receção das chaves em curso**
- **Não faz parte desta equipa**

Se for membro e o acesso estiver pronto, prima **Abrir a minha equipa**.

## 14.1 Criar uma equipa

Esta função aparece para o chefe de grupo com a permissão correspondente.

1. Introduza o **Nome da equipa**.
2. Escolha o **Chefe de equipa** entre os membros do grupo.
3. Selecione opcionalmente os membros iniciais.
4. Pode utilizar:
   - Selecionar tudo;
   - 10 pessoas;
   - 15 pessoas;
   - Desselecionar tudo.
5. Prima **Criar a equipa e nomear o respetivo chefe**.

Uma equipa aceita no máximo 200 membros iniciais no formulário, incluindo o chefe.

Os membros selecionados abandonam a eventual equipa anterior dentro do mesmo grupo para entrar na nova.

Quando o grupo já possui dez equipas ou mais, o código impõe regras adicionais de dimensão mínima: as equipas ativas devem ter pelo menos quatro membros para continuar a expansão.

## 14.2 Substituir o chefe de equipa

Se a ação estiver autorizada:

1. abra a equipa;
2. utilize **Substituir o chefe de equipa**;
3. escolha um membro do grupo.

## 14.3 Limiares de validação

Os responsáveis autorizados podem definir:

- votos de batedores necessários para concluir;
- votos de batedores necessários para declarar impossível;
- votos necessários para resolver uma sinalização.

---

# 15. Participantes e funções

O separador **Participantes** apresenta os membros do contexto selecionado.

Pode procurar um participante pelo respetivo N.º pessoal ou identificador.

Toque num participante para abrir as ações disponíveis.

## 15.1 Funções permanentes e funções de sessão

Quando existe uma sessão disponível, o gestor pode escolher:

- **Permanente**;
- **Sessão**.

Uma função permanente permanece associada ao membro de acordo com as regras do grupo/equipa.

Uma função de sessão aplica-se à sessão selecionada.

## 15.2 Atribuir ou retirar uma função

As funções que pode atribuir aparecem sob a forma de botões.

Um botão ativo indica que a função já está presente. Premir esse botão permite retirá-la quando tiver autoridade para o fazer.

Existe também uma secção **Administrar uma função numa equipa** que permite escolher:

1. a equipa de destino;
2. a função;
3. **Atribuir a função de equipa** ou **Retirar a função de equipa**.

## 15.3 Atribuição de sessão

Um administrador de sessão pode definir o participante como:

- Ativo;
- Em pausa;
- Saiu;
- Removido.

Também pode escolher a equipa da sessão ou **Sem equipa**.

Prima **Aplicar a atribuição**.

## 15.4 Remover um membro

Quando a permissão está disponível, aparece o botão **Remover deste grupo ou desta equipa**.

## 15.5 Transferir a administração do grupo

O responsável autorizado pode selecionar outro participante e utilizar **Transferir a administração**.

O destinatário deverá depois aceitar a transferência na secção **Gestão**.

## 15.6 Bloquear um dispositivo

A secção **Moderação** permite, quando a sua função o autoriza:

- **Bloquear este dispositivo**;
- apresentar os dispositivos bloqueados;
- **Levantar o bloqueio**.

Um dispositivo bloqueado continuará a ser recusado em novos convites até o bloqueio ser levantado.

---

# 16. Convidar um novo participante

Abra **Convidar**.

## 16.1 Escolher o destino

Consoante a sua função, o menu **Destino** permite escolher:

- o grupo;
- uma equipa.

Um administrador do grupo pode ter vários destinos no menu.

## 16.2 Admissões abertas / fechadas

A interface pode indicar:

- **Admissões abertas**;
- **Admissões fechadas**.

Se a sua função o permitir:

- **Abrir o acesso**;
- **Fechar o acesso**.

Uma equipa também pode herdar o fecho geral do grupo.

## 16.3 Partilhar o convite

O LETCOOR permite:

- ligação;
- QR;
- cópia;
- partilha do sistema;
- ficheiro `.letcoor` nas plataformas onde o botão é disponibilizado.

## 16.4 Receber a resposta

Depois de o outro dispositivo importar o convite:

1. abra **Receber a resposta**;
2. digitalize ou cole a ligação de resposta;
3. o LETCOOR inicia a ligação.

Se as tentativas pela Internet e por proximidade expirarem, o botão **Tentar novamente** permite recomeçar.

## 16.5 Repor um convite

O botão de reposição permite invalidar/regenerar a troca atual quando a sua função o permite.

---

# 17. Operações

O separador **Operações** permite escolher um grupo ou uma equipa e apresenta depois vários sub-separadores consoante os direitos e o conteúdo:

- **Ordens**
- **Anúncios**
- **Funções**
- **Partilha entre equipas**
- **Sessões**
- **Histórico**

## 17.1 Ordens

Apresenta as ordens ativas com:

- tipo;
- prioridade;
- texto;
- estado da resposta.

Quando é necessária uma confirmação, o botão **Recebida** permite confirmar a receção a partir desta vista.

## 17.2 Anúncios

Apresenta os anúncios ativos.

Cada anúncio pode incluir:

- tipo;
- texto;
- estado fixado;
- botão **Confirmar receção**.

Um membro autorizado pode criar um anúncio escolhendo:

### Tipos

- Informação
- Importante
- Informação do grupo
- Informação de sessão
- Regra da atividade
- Coordenação

### Expiração

- 15 min
- 1 h
- 4 h
- 24 h
- Sem expiração

Uma caixa permite **Fixar o anúncio**.

---

# 18. Campanhas de funções

As campanhas de funções permitem abrir temporariamente lugares para uma determinada função.

Encontram-se em:

**Menu do grupo/equipa > Operações > Funções**

## 18.1 Entrar numa campanha

Uma campanha aberta apresenta:

- a função;
- o respetivo estado;
- o modo;
- o número de lugares já atribuídos / capacidade.

Prima **Entrar** para solicitar a função.

## 18.2 Modos de campanha

### Primeiros pedidos válidos — `FIRST_VALID`

Os primeiros pedidos elegíveis são atribuídos automaticamente até a capacidade disponível ser atingida.

O código só permite este modo para funções consideradas não privilegiadas.

### Validação por um responsável — `ADMIN_APPROVAL`

Os pedidos permanecem pendentes até serem aprovados por um responsável.

O gestor vê **Pedidos pendentes** e pode premir **Aprovar** para cada participante.

## 18.3 Criar uma campanha

Se a sua função permitir gerir campanhas:

1. escolha a **Função**;
2. escolha o **Modo** proposto para essa função;
3. escolha o número de **Lugares** de 1 a 64;
4. escolha a **Duração**:
   - 15 min;
   - 1 h;
   - 4 h;
   - 24 h;
5. prima **Abrir uma campanha**.

## 18.4 Fechar uma campanha

Um gestor autorizado pode premir **Fechar**.

## 18.5 Retirar o seu pedido

Em **Histórico**, um pedido ainda pendente pode apresentar **Retirar o meu pedido**.

## 18.6 Funções disponíveis para as campanhas

O código disponibiliza às campanhas, consoante o contexto e os seus direitos:

- Batedor do grupo;
- Batedor de equipa;
- Retransmissor;
- Cobertura;
- Assalto.

A função de Chefe de grupo nunca é atribuída por campanha.

---

# 19. Sessões

Uma sessão representa um período operacional limitado dentro do grupo.

## 19.1 Criar uma sessão

A partir de **Gestão**, se tiver a permissão:

1. abra a secção **Sessão**;
2. introduza a duração em minutos;
3. a duração máxima apresentada é de **56 dias**;
4. prima **Criar uma sessão**.

## 19.2 Consultar as sessões

Em **Operações > Sessões**, o LETCOOR apresenta:

- data de criação;
- estado: aberta/terminada ou estado de atribuição;
- a sua eventual equipa;
- fim previsto.

## 19.3 Gerir uma sessão

O responsável autorizado pode:

- adicionar **+ 1 h**;
- **Terminar** a sessão.

## 19.4 Funções e atribuições durante uma sessão

Em **Participantes**, pode escolher uma sessão administrada, atribuir funções limitadas a essa sessão e atribuir participantes a uma equipa/estado.

---

# 20. Partilha de dados entre equipas

Esta função está disponível a partir de uma **equipa** em:

**Operações > Partilha entre equipas**

Não dá automaticamente acesso ao conteúdo privado de outra equipa. Utiliza uma oferta de partilha criada e aceite explicitamente.

## 20.1 Propor uma partilha

1. Escolha a **Equipa de destino**.
2. Escolha os **Dados partilhados**.
3. Escolha a precisão.
4. Defina a frequência.
5. Defina a expiração.
6. Prima **Propor a partilha**.

## 20.2 Classes de dados disponíveis

- Presença geral da equipa
- Sinal
- Estado da equipa
- Posição precisa
- Histórico de deslocações

## 20.3 Precisão

- Vista geral / agregada
- Aproximada
- Precisa

Se **Posição precisa** estiver selecionada, a precisão torna-se necessariamente precisa na interface.

## 20.4 Frequência

Ajustável entre **5 e 300 segundos**, em passos de 5 segundos.

## 20.5 Expiração

- 15 min
- 1 h
- 4 h
- 24 h

## 20.6 Aceitar ou revogar

A equipa destinatária autorizada pode premir **Aceitar**.

Uma oferta ou uma partilha pode ser **Revogada** pelo lado que disponha da permissão correspondente.

---

# 21. Gestão do grupo e das equipas

O separador **Gestão** centraliza as funções administrativas.

## 21.1 Selecionar um espaço

O seletor **Grupo ou equipa** permite escolher o espaço a administrar.

## 21.2 Entrar numa equipa existente

Quando a ação está autorizada, uma equipa pode apresentar:

- **Entrar**;
- **Recuperar acesso** quando a adesão existe, mas as chaves precisam de ser recuperadas.

## 21.3 Sair de uma equipa

Prima **Sair da equipa** e verifique o resumo antes de confirmar.

## 21.4 Dissolver uma equipa

Um responsável autorizado vê **Dissolver a equipa**.

A confirmação indica que:

- a equipa será dissolvida para os respetivos membros;
- os membros permanecem no grupo;
- os outros dispositivos aplicam a dissolução quando a recebem.

## 21.5 Sair de um grupo

Um membro normal pode preparar um plano de saída e depois confirmá-lo.

Se o participante liderar equipas, o LETCOOR pode ter de dissolver essas equipas antes da saída, de acordo com o plano calculado pelo Core.

## 21.6 Dissolver um grupo

O chefe de grupo autorizado pode utilizar **Dissolver o grupo**.

A confirmação avisa que o grupo e as respetivas equipas serão dissolvidos. Os dispositivos offline terão de voltar a ligar-se para receber a dissolução.

## 21.7 Entrar num novo grupo ou numa nova equipa

A página **Gestão** contém também um bloco **Entrar num grupo ou numa equipa** com o mesmo sistema de convite da integração inicial.

## 21.8 Convites pendentes

Quando o Core disponibiliza convites a aceitar, estes aparecem com um botão **Aceitar** até à expiração.

## 21.9 Estado da equipa

O responsável autorizado pode publicar:

- Pronta
- Em deslocação
- Em posição
- Em reunião
- Precisa de ajuda
- Desligada

## 21.10 Política de posição exata

Numa equipa, um responsável autorizado pode escolher:

- **Permitir**;
- **Recusar**

para a política de posição exata da equipa.

## 21.11 Transferência de administração

Se existir uma transferência de administração pendente para si, a secção apresenta **Aceitar a transferência de administração**.

---

# 22. Limites de publicação

Em **Gestão**, os responsáveis autorizados podem definir os limites de publicação do grupo ou da equipa.

Os limites podem ser definidos:

- por predefinição;
- para um membro específico.

Parâmetros atualmente disponibilizados:

- número de alertas de segurança ativos;
- sinalizações por minuto;
- sinalizações por 4 minutos.

Os valores do formulário vão de 1 a 1000.

---

# 23. Localização

O ícone **Localização** aparece no mapa quando a plataforma fornece localização nativa.

## 23.1 Ativar a partilha

1. Abra **Localização**.
2. Selecione **Partilhar a minha localização**.
3. Defina a precisão.

O LETCOOR volta a publicar a presença periodicamente enquanto a partilha estiver ativa e a aplicação conseguir obter a posição.

## 23.2 Precisão

O controlo deslizante vai de **0 m a 1 km**.

- **0 m**: precisão disponível no dispositivo, sem deslocamento adicionado pelo LETCOOR.
- valor superior: a posição partilhada é deslocada aleatoriamente dentro do raio escolhido.

## 23.3 Parar a partilha

Selecione **Não partilhar a minha localização**.

A partilha também é interrompida quando o contexto muda ou quando a aplicação interrompe a presença de acordo com o respetivo ciclo de vida.

## 23.4 Estados apresentados

- A obter localização…
- Partilha ativa com o seu grupo
- Partilha à espera de retomar
- Localização não partilhada

> A partilha de localização não é obrigatória para entrar num grupo, utilizar o mapa, enviar ordens ou utilizar a rede mesh.

---

# 24. Notificações

Toque no **sino** na parte superior do ecrã.

O centro de notificações reúne:

- eventos do grupo;
- alterações de ligação/transporte;
- avisos do sistema LETCOOR.

O indicador mostra o número de notificações não lidas.

## 24.1 Leitura

As notificações são marcadas como lidas quando ficam suficientemente visíveis na lista ou quando a secção correspondente é consultada.

## 24.2 Navegação

Tocar numa notificação pode abrir:

- a secção Participantes;
- Equipas;
- Operações;
- um objeto do mapa;
- o painel Comando.

## 24.3 Notificações do sistema

As definições do sino permitem ativar/desativar as notificações nativas do sistema quando a plataforma o permite.

---

# 25. Mapas offline

Abra:

**Menu do grupo/equipa > Definições > Mapas offline**

## 25.1 Selecionar uma zona

1. Prima **Selecionar mosaicos no mapa**.
2. O LETCOOR fecha o painel e apresenta uma grelha no mapa.
3. Toque nas células que pretende guardar.
4. O contador indica o número de células selecionadas num máximo de 20.
5. Prima **Validar** para voltar às definições ou **Cancelar**.

## 25.2 Nível de detalhe

O menu **Detalhe** permite selecionar um nível de zoom de 3 a 14.

Uma zona demasiado grande com um nível de detalhe elevado pode ser recusada. A interface pede então para reduzir o detalhe ou escolher células mais pequenas.

## 25.3 Instalar

Depois de selecionar as células:

1. prima **Instalar as células selecionadas**;
2. acompanhe o progresso;
3. pode **Cancelar a transferência**.

## 25.4 Eliminar um mapa

Os mapas instalados são apresentados com o respetivo zoom e tamanho. Prima **Eliminar** para libertar espaço.

---

# 26. Ligação de rede e funcionamento offline

O LETCOOR pode utilizar vários transportes para a mesma rede lógica.

A interface reconhece, nomeadamente:

- **Internet direta**;
- **Internet por retransmissão**;
- **Rede local (LAN)**;
- **Wi‑Fi local**;
- **Wi‑Fi Direct**;
- **Bluetooth**.

## 26.1 Mesh lógica

O LETCOOR não exige que cada membro esteja diretamente ligado a todos os outros.

Exemplo:

```text
Telefone A ↔ Telefone B ↔ Telefone C ↔ Telefone D
```

Um evento autorizado pode ser retransmitido entre pares de acordo com a topologia e as regras de alcance do grupo/equipa.

O transporte físico e a identidade LETCOOR são separados: um par continua identificado pela sua identidade LETCOOR mesmo que o caminho de rede mude.

## 26.2 Sem Internet

Para maximizar as hipóteses de funcionar sem Internet:

- ative o Wi‑Fi;
- ative o Bluetooth;
- autorize dispositivos próximos;
- autorize a rede local se o Android o pedir;
- aceite a visibilidade/emparelhamento do sistema quando o LETCOOR o solicitar;
- mantenha o LETCOOR em primeiro plano durante a primeira ligação;
- aproxime os dispositivos durante o arranque inicial;
- não recuse os diálogos do sistema necessários para o rádio de proximidade.

## 26.3 Estado dos transportes de proximidade

O LETCOOR pode apresentar separadamente:

- Wi‑Fi local;
- Wi‑Fi Direct;
- Bluetooth;

com estados como:

- permissão necessária;
- ativação necessária;
- inicialização;
- pronto;
- procura;
- par encontrado;
- ligação;
- grupo formado;
- autenticação LETCOOR;
- ligado;
- recuperação;
- indisponível.

## 26.4 Wi‑Fi Direct ocupado

Se o Android indicar que o Wi‑Fi Direct está ocupado, o LETCOOR pode tentar uma recuperação. O ecrã de informação do Wi‑Fi Direct aconselha, nomeadamente, verificar:

- se o Wi‑Fi está ativo;
- se a partilha de ligação/hotspot entra em conflito com o Wi‑Fi Direct;
- se já existe outra procura/ligação Wi‑Fi Direct em curso.

## 26.5 A rede pode mudar de transporte

O estado na parte superior do ecrã pode apresentar diferentes transportes durante a sessão. O LETCOOR pode dispor de rotas alternativas para um par e utilizar a rota disponível de acordo com o estado da rede.

---

# 27. Privacidade, bloqueio e recuperação

O LETCOOR aplica vários comportamentos de proteção quando os dados privados de um grupo deixam de poder ser verificados junto de outros membros.

## 27.1 Bloqueio após ausência

O código da interface prevê um ecrã:

**Sessão bloqueada após um minuto de ausência.**

Prima **Voltar a ligar** para recuperar o acesso.

## 27.2 Verificação da ligação aos membros

Quando é necessária uma recuperação de privacidade, o LETCOOR apresenta:

**A verificar a ligação aos membros…**

Tenta encontrar um membro acessível e pode apresentar os detalhes dos transportes de proximidade.

## 27.3 Eliminação automática local

Para determinados grupos configurados com recuperação automática, se não for possível restabelecer a ligação durante o período previsto, os dados locais do grupo podem ser eliminados **após verificação**.

A interface atual anuncia um prazo de vinte minutos para os grupos em causa.

Quando a opção é disponibilizada, pode:

- eliminar/repor os dados locais;
- ou escolher **Manter os dados por minha conta e risco**, o que desativa a eliminação automática para este contexto.

O LETCOOR avisa que manter esses dados pode aumentar o risco em caso de comprometimento físico do dispositivo.

## 27.4 Proteção no desktop

No desktop, a vista privada pode ser ocultada/desfocada quando a janela perde o foco e depois atualizada antes de voltar a ser apresentada.

---

# 28. Funções disponíveis

O modelo de domínio do LETCOOR define nove funções.

| Função | Função geral no código atual |
|---|---|
| **Administrador do grupo** (`GROUP_ADMIN`) | Administração do grupo, criação de equipas e sessões, gestão de membros/funções, campanhas, dissolução, transferência de administração, anúncios. |
| **Coordenador do grupo** (`GROUP_LEADER`) | Coordenação ao nível do grupo, ordens/objetivos/sinalizações do grupo, campanhas e anúncios consoante as permissões. |
| **Chefe de equipa** (`TEAM_LEADER`) | Ordens/objetivos/encontros/estado da sua equipa, partilha entre equipas, anúncios, campanhas de equipa. |
| **Batedor do grupo** (`GROUP_SCOUT`) | Sinalização e confirmação/promoção ao nível do grupo consoante as permissões. |
| **Batedor de equipa** (`TEAM_SCOUT`) | Relatório/sinalização da equipa, confirmação e promoção consoante as permissões. |
| **Retransmissor** (`TRANSMITTER`) | Capacidade de retransmissão prevista pelo domínio e publicação de determinadas presenças resumidas de acordo com a política; esta função não concede acesso aos dados privados de outras equipas. |
| **Cobertura** (`COVER`) | Etiqueta operacional com as capacidades básicas do membro. |
| **Assalto** (`ATTACKER`) | Etiqueta operacional com as capacidades básicas do membro. |
| **Membro** (`MEMBER`) | Capacidades básicas: sinalização normal na sua equipa quando permitida, alerta de segurança, resposta a ordens, presença autorizada e participação em campanhas. |

> As permissões são calculadas pelo Core e são aditivas. A interface apresenta apenas as ações realmente autorizadas. Pertencer a um grupo não dá automaticamente acesso aos dados privados de todas as suas equipas.

---

# 29. Conselhos de preparação antes de uma atividade

Para uma utilização real, sobretudo numa zona onde a Internet possa ser fraca:

1. Instale a mesma versão do LETCOOR nos dispositivos.
2. Crie o grupo antes do início da atividade.
3. Faça os participantes entrar enquanto ainda estiverem fisicamente próximos.
4. Aceite as permissões de proximidade em cada Android.
5. Ative o Bluetooth e o Wi‑Fi.
6. Teste pelo menos uma ligação sem dados móveis se o funcionamento offline for importante.
7. Crie as equipas e atribua os chefes antes de se dispersarem.
8. Abra uma sessão se pretender funções/atribuições de sessão e o histórico correspondente.
9. Transfira os mapas offline necessários antes de perder a Internet.
10. Verifique se os participantes sabem abrir:
    - Notificações;
    - Comando;
    - a respetiva equipa;
    - a função Alerta de segurança.
11. Ative a partilha de localização apenas se quiser realmente publicá-la.

---

# 30. Resolução de problemas

## Os dois dispositivos não se encontram offline

Verifique nos dois dispositivos:

- Wi‑Fi ativado;
- Bluetooth ativado;
- permissões de **Dispositivos próximos** concedidas;
- permissão de rede local concedida se o Android a solicitar;
- aplicação visível/detetável se o sistema pedir confirmação;
- LETCOOR em primeiro plano durante a procura inicial.

Se o Android abrir as definições de localização, ative o serviço de localização para maximizar a compatibilidade de descoberta. Isto não ativa a partilha de posição do LETCOOR.

## «Wi‑Fi Direct indisponível» ou «ocupado»

- desative temporariamente uma partilha de ligação/hotspot manual;
- aguarde alguns segundos;
- volte a iniciar a tentativa;
- verifique se outra aplicação ou ligação Wi‑Fi Direct está ativa.

## O QR não funciona

- aguarde até que todas as partes do QR tenham sido lidas;
- aproxime os ecrãs;
- aumente o brilho do ecrã que apresenta o QR;
- utilize o controlo de zoom da câmara;
- utilize a ligação em vez do QR, se necessário.

## A câmara foi recusada

- utilize a ligação;
- ou abra as definições da câmara do Windows/Android a partir do LETCOOR quando o botão estiver disponível.

## A ligação é aceite, mas a conexão expira

- verifique a Internet ou a proximidade;
- aproxime os dispositivos;
- ative Wi‑Fi e Bluetooth;
- aceite os diálogos do sistema;
- prima **Tentar novamente** quando o botão aparecer.

## Estou no grupo, mas não numa equipa

Abra:

**Contexto > Equipas** ou **Gestão**.

Se a equipa permitir a adesão, utilize **Entrar**. Um convite de equipa também pode admitir diretamente o participante no grupo principal e na equipa de destino, consoante o ticket recebido.

## «Adesão registada · receção das chaves em curso»

A adesão é conhecida, mas o acesso criptográfico à equipa ainda não está pronto. Mantenha os dispositivos ligados para permitir a recuperação/sincronização das chaves. Se o botão **Recuperar acesso** aparecer em Gestão, utilize-o.

## Um objeto não está visível

Verifique:

- o grupo/equipa selecionado;
- as suas permissões;
- a expiração do objeto;
- a sincronização de rede;
- que um objeto privado da equipa não é automaticamente visível para as outras equipas.

## A localização não aparece

- verifique a permissão de localização;
- verifique se **Partilhar a minha localização** está selecionado;
- verifique o grupo atual;
- aguarde a próxima publicação periódica;
- verifique se a política da equipa permite a precisão necessária.

---

# 31. Resumo rápido

## Para entrar no LETCOOR

```text
Dispositivo que convida
  ↓
Convidar
  ↓
QR ou ligação
  ↓
O dispositivo convidado importa
  ↓
O dispositivo convidado produz uma resposta
  ↓
O dispositivo que convida digitaliza/cola a resposta
  ↓
Ligação + autenticação + admissão
```

## Para criar algo no mapa

```text
Pressão prolongada no mapa
  ↓
Sinalização / Objetivo / Ordem / Ponto de reunião / Alerta de segurança
  ↓
Preencher o formulário
  ↓
Escolher zona / duração, se disponível
  ↓
Publicar
```

## Para gerir um grupo

```text
Nome do grupo no canto superior esquerdo
  ↓
Contexto | Equipas | Participantes | Convidar | Operações | Gestão | Definições
```

## Para uma campanha de funções

```text
Operações
  ↓
Funções
  ↓
Escolher função + modo + lugares + duração
  ↓
Abrir uma campanha
  ↓
Os membros entram
  ↓
Atribuição automática ou validação por um responsável consoante o modo
```

## Para funcionar sem Internet

```text
Wi‑Fi LIGADO
Bluetooth LIGADO
Permissões de proximidade autorizadas
Rede local autorizada se solicitada
Emparelhamento/visibilidade aceites se solicitados
Dispositivos próximos no primeiro contacto
LETCOOR aberto em primeiro plano
```

O LETCOOR pode depois utilizar os transportes disponíveis e retransmitir as informações autorizadas entre pares de acordo com a topologia da rede mesh.

---

**LETCOOR 1.0.0 — Documentação do utilizador**
