---
title: Política de Privacidade do Orçamento
lang: pt
---

# Política de Privacidade do Savings Challenge & Budget

*Esta é uma tradução. Se ela divergir da [versão em inglês](../privacy), prevalece a versão em inglês.*

Data de vigência: 2026-11-22

Esta política explica como o Savings Challenge & Budget (exibido como "Orçamento" na sua Tela de Início, o "App"), desenvolvido por Stanislau Malchanau ("nós"), trata as suas informações. Em resumo: **não coletamos, vendemos nem compartilhamos seus dados pessoais. Seu orçamento fica no seu dispositivo e na sua própria conta do iCloud. O App não guarda nem movimenta dinheiro, não está conectado a nenhum banco e não dá aconselhamento financeiro.**

## 1. Dados que o App guarda

O App guarda no seu dispositivo: seus gastos, ganhos e estornos (o valor, a moeda e a cotação usada, a categoria, uma observação, a data, a hora e o fuso horário, e como o registro foi adicionado, por exemplo digitado, a partir de uma nota fiscal ou pelo Apple Pay), suas categorias e os limites delas, seu orçamento mensal e os ajustes dele (o dia em que o seu mês começa, se o que sobrar passa para o mês seguinte), seus pagamentos recorrentes, suas metas de economia com o que você guardou e retirou, seus desafios de economia, as cotações que você mesmo digitou, o orçamento compartilhado que você mantém com uma pessoa que você convida (seção 3), suas respostas às perguntas da primeira abertura e seus ajustes (o horário do lembrete, o bloqueio com Face ID, o som e a vibração). Os registros apagados ficam 30 dias em "Apagados recentemente" para que você possa recuperá-los.

Esses registros descrevem como você gasta e economiza, e algumas leis tratam esse tipo de informação como financeira ou sensível. Eles nunca saem do seu dispositivo e da sua conta do iCloud (seções 2 e 3). Não operamos servidores que recebam os seus registros, não temos acesso a eles, e o App nunca envia seus registros a um serviço de IA online nem a mais ninguém. O único servidor que operamos (seção 6), um servidor pequeno, responde com cotações e assina digitalmente ofertas de desconto; ele nunca recebe os seus registros.

## 2. Sincronização com o iCloud

Se você tiver uma sessão iniciada no iCloud, o App sincroniza seu orçamento pelo CloudKit da Apple, no banco de dados privado da sua própria conta do iCloud, para que ele esteja lá em um iPhone novo e depois de reinstalar o App. Esses dados são armazenados e protegidos pela Apple de acordo com a Política de Privacidade da Apple (https://www.apple.com/legal/privacy/). Não podemos vê-los, lê-los nem exportá-los. Quando algo muda no iCloud, o serviço de push da Apple pode despertar o App para que ele busque a mudança; essa notificação não traz nenhum dos seus registros. Você pode desativar a sincronização em Ajustes do iOS > [seu nome] > iCloud; seu orçamento então fica apenas neste iPhone.

## 3. O orçamento compartilhado

Você pode convidar uma pessoa para um orçamento que vocês mantêm juntos. O convite é um link do iCloud que você mesmo envia, e o orçamento compartilhado é armazenado pela Apple em uma zona compartilhada do CloudKit que só vocês dois podem abrir. O que qualquer um de vocês adicionar a ele é visto pela outra pessoa, e cada registro mostra quem o adicionou; o seu próprio orçamento nunca é compartilhado. Se você digitar um nome para o orçamento compartilhado, a outra pessoa o vê junto aos seus registros; ele fica armazenado com o seu orçamento na sua conta do iCloud e na zona compartilhada. O App informa à pessoa convidada se a sua assinatura está ativa, para que ela possa adicionar registros ao orçamento compartilhado de graça (seção 2 dos Termos de Uso). Qualquer um de vocês pode sair do orçamento compartilhado ou fechá-lo no App a qualquer momento. Se você deixar de compartilhar, a outra pessoa pode ficar com uma cópia somente para leitura do que havia no orçamento compartilhado até então. Quando a Apple avisa o App de que a outra pessoa adicionou algo, a notificação passa pelo serviço de push da Apple.

## 4. Scanner de notas fiscais e a câmera

O App usa a câmera apenas quando você abre o scanner de notas fiscais, e o iOS pede a sua permissão na primeira vez. A foto da nota é lida no seu iPhone: o framework Vision da Apple encontra o texto dela e qualquer código QR e, nos iPhones com Apple Intelligence, o modelo de linguagem da Apple que roda no próprio aparelho ajuda a encontrar o total, a moeda e o nome da loja. A foto e o texto reconhecido ficam apenas na memória do iPhone enquanto são lidos e são apagados logo depois. Eles nunca são salvos, nunca são enviados pela internet e nunca chegam a nós nem a qualquer serviço online. Só fica guardado o gasto que você então salva (o valor, a moeda, a data e o nome da loja na observação), como qualquer outro registro.

## 5. Apple Pay pelos Atalhos

O App não lê a sua Carteira, os seus cartões nem o seu banco. Se você optar por configurar uma automação pessoal no app Atalhos da Apple com o gatilho "Transação", então, cada vez que você pagar com Apple Pay em uma loja, os Atalhos passam o valor e o nome do estabelecimento para a ação do App que adiciona um gasto, no mesmo iPhone, e o App registra um gasto com esses dados. Nada disso é enviado para nós; o registro é guardado e sincronizado como qualquer outro (seções 1 e 2). Nada acontece a menos que você mesmo configure a automação, e você pode alterá-la ou apagá-la nos Atalhos a qualquer momento.

## 6. Cotações e ofertas de desconto (nosso servidor)

Operamos um único servidor pequeno, no Cloudflare Workers, para duas tarefas. Nenhuma delas recebe os seus registros.

- **Cotações.** Quando um gasto está em uma moeda diferente da sua moeda principal, ou quando você muda a sua moeda principal, o App pede ao servidor as cotações daquele dia. O pedido traz apenas a data: nenhum valor, nenhuma moeda e nada sobre você. O servidor pega as cotações de referência do dia do Banco Central Europeu e, para as moedas que o banco não publica, as cotações de bancos centrais reunidas pelo serviço aberto Frankfurter, e devolve a tabela inteira daquele dia; o seu iPhone escolhe a cotação de que precisa. Os gastos na sua moeda principal nunca precisam do servidor.
- **Ofertas de desconto.** Se você desativar a renovação, o App pode oferecer um preço menor para o seu próximo período (seção 2 dos Termos de Uso). A Apple exige que essa oferta tenha a nossa assinatura digital, então, logo antes da compra, o App envia ao servidor apenas o identificador do próprio App, os identificadores do plano e da oferta e, quando a Apple pede, o número que a App Store deu à compra da sua assinatura atual. O servidor adiciona um número aleatório de uso único, assina tudo digitalmente, responde e não guarda nada. Ele não fica sabendo nada sobre quem você é: nem nome, nem Conta Apple, nem nenhum dos seus registros.

Como qualquer servidor, o nosso vê o endereço IP de um pedido para poder respondê-lo. Ele não armazena esse endereço em nada do que guarda e não associa pedidos a uma pessoa. A Cloudflare, que opera o servidor, pode manter logs técnicos de curta duração dos pedidos para segurança e confiabilidade, de acordo com a própria política de privacidade dela (https://www.cloudflare.com/privacypolicy/).

## 7. Notificações e widgets

O lembrete da noite é agendado no seu iPhone, e só se você permitir notificações. Nenhum dado é enviado para nós para entregá-lo. Os widgets leem o seu orçamento no seu dispositivo.

## 8. Bloqueio com Face ID

Se você ativar o bloqueio, o App pede ao iOS que verifique o seu Face ID ou o seu código. O Face ID é tratado inteiramente pelo iOS: o App nunca vê os dados do seu rosto e só fica sabendo se a verificação foi aprovada.

## 9. Compras

As assinaturas são vendidas e processadas pela Apple por meio da App Store. Não recebemos seus dados de pagamento. A Apple informa ao App se a sua assinatura está ativa, qual plano você escolheu, com o preço, se a renovação está ativada e se há uma oferta disponível para a sua Conta Apple; a seção 10 explica o que disso vai para as nossas estatísticas de uso.

## 10. Estatísticas de uso e relatórios de falhas

Para saber quais recursos ajudam e onde o App atrapalha, o App envia sinais de uso anônimos ao TelemetryDeck, um serviço de análise da TelemetryDeck GmbH (Augsburg, Alemanha) com servidores na UE. O código dele é o único código no App que não vem da Apple nem de nós. Um sinal indica uma ação no App: por exemplo, que uma etapa da primeira abertura foi concluída e qual das respostas de múltipla escolha foi escolhida (o que atrapalhou antes, se você definiu um orçamento mensal, o dia em que o seu mês começa, o tipo da sua primeira meta na lista e em quantos meses), quanto tempo levou o primeiro gasto, que um gasto ou um ganho foi adicionado e como (digitado, por um widget, uma nota fiscal, o Apple Pay ou um arquivo) e se estava na sua moeda principal, que uma meta foi criada (o tipo dela na lista e se ela tem uma data), que um valor foi guardado, que um desafio começou ou um quadradinho foi marcado, que um painel foi aberto ou um arquivo foi importado (com uma contagem aproximada das linhas dele), que a tela de assinatura ou uma oferta foi exibida, que um plano foi escolhido ou que uma assinatura começou, foi renovada ou restaurada, que o App pediu uma avaliação ou, como um código de erro curto, que algo não funcionou, por exemplo que a App Store não respondeu. Ele vem com o horário, arredondado para a hora, e com detalhes técnicos gerais: as versões do App e do iOS, o modelo do dispositivo, o idioma, a região e o fuso horário, e ajustes de tela e de acessibilidade, como o modo escuro ou o tamanho do texto. Quando uma assinatura começa ou é renovada, o sinal também traz o plano, o preço convertido em dólares americanos, a moeda e o país da sua App Store, para que possamos ver quais planos as pessoas escolhem.

Um sinal nunca contém seus valores, saldos ou números do orçamento, suas categorias, observações ou nomes de metas, nomes de lojas ou de estabelecimentos, fotos de notas fiscais ou o texto delas, as cotações que você digitou, seu nome, seu e-mail, sua Conta Apple ou sua localização, nem nada sobre a pessoa com quem você compartilha um orçamento. Sua instalação é identificada apenas por um identificador aleatório que o App mistura com um salt e transforma em hash antes do envio, de modo que os sinais não podem ser associados a você nem seguir você entre apps. O TelemetryDeck não guarda endereços IP e não usa cookies. Olhamos para esses sinais apenas como estatísticas para melhorar o App; não os vendemos, não os compartilhamos com anunciantes e não os usamos para rastrear você. O App não contém código de publicidade ou de rastreamento e não rastreia você em outros apps ou sites.

Além disso, se você optar por compartilhar análises com desenvolvedores de apps em Ajustes do iOS > Privacidade e Segurança > Análise e Melhorias, a Apple pode nos fornecer estatísticas de uso e relatórios de falhas agregados e anônimos. Eles não identificam você.

## 11. Game Center

Se você tiver uma sessão iniciada no Game Center, as conquistas pelos seus marcos de economia são informadas ao Game Center da Apple na sua conta do Game Center e tratadas de acordo com a Política de Privacidade da Apple. Uma conquista diz apenas que um marco foi alcançado; seus registros, observações e nomes de metas não são enviados. Não recebemos a sua identidade do Game Center.

## 12. Importação e exportação

A exportação dos seus gastos e ganhos como arquivo CSV e a importação de um arquivo CSV de outro app de orçamento são feitas no seu dispositivo. O App lê apenas o arquivo que você escolhe, e um arquivo exportado vai apenas para onde você o enviar pelo menu de compartilhamento.

## 13. O que o App não faz

O App não guarda, não movimenta, não investe nem empresta dinheiro. Ele não está conectado a nenhum banco, cartão ou conta de pagamento e não dá aconselhamento financeiro, tributário ou de investimentos. Ele não acessa a sua Carteira, sua localização, seus contatos, sua fototeca nem seu microfone, e não tem conta, login, publicidade, chat nem feed público.

## 14. Crianças

O App é adequado para todas as idades (classificação 4+) e não coleta intencionalmente informações pessoais de ninguém, incluindo crianças menores de 13 anos (ou a idade equivalente no seu país).

## 15. Retenção e exclusão de dados

Os dados ficam enquanto você os mantiver. Você pode apagar um registro no App a qualquer momento; ele espera 30 dias em "Apagados recentemente" e depois desaparece. Você pode apagar tudo apagando o App e, para os dados sincronizados, em Ajustes do iOS > [seu nome] > iCloud > Gerenciar Armazenamento da Conta > Orçamento. O que você adicionou a um orçamento compartilhado fica lá para a outra pessoa até que um de vocês o apague ou que o orçamento compartilhado seja fechado. Como não guardamos nenhuma cópia, não há mais nada a apagar do nosso lado. Os sinais de uso são anônimos e não podem ser associados a você, e o nosso servidor não guarda nada sobre você, então não existe nenhum registro pessoal de nenhum dos dois para consultar ou apagar.

## 16. Seus direitos

Dependendo de onde você mora (por exemplo, pela LGPD no Brasil, pelo GDPR na UE, pelo UK GDPR, pela CCPA/CPRA na Califórnia, pela APPI no Japão ou pela PIPA na Coreia), você pode ter o direito de acessar, corrigir, excluir ou portar seus dados pessoais e de se opor ao tratamento deles ou restringi-lo. Como não guardamos seus dados, você pode exercer esses direitos diretamente no seu dispositivo e no iCloud, como descrito acima; a exportação CSV em Ajustes dá a você todos os seus gastos e ganhos em um único arquivo. Você também pode nos contatar com qualquer pedido ou dúvida e pode reclamar à autoridade de proteção de dados do seu país.

Não vendemos nem compartilhamos informações pessoais conforme definido pela CCPA/CPRA.

## 17. Alterações

Se esta política mudar, atualizaremos a data acima e, em caso de mudanças relevantes, avisaremos você no App.

## 18. Contato

Stanislau Malchanau, Belarus
E-mail: 7tam.official@gmail.com
