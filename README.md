# Kava Kids — Sistema de Vendas

Sistema de vendas, estoque, clientes e gestão da **Kava Kids**, loja de roupas infantis.

Aplicativo de arquivo único: roda direto no navegador, sem instalação, sem servidor
e sem internet. Feito para operar no balcão com leitor de código de barras USB e
impressora térmica de cupom de 80 mm.

## Arquivos

| Arquivo | O que é |
|---|---|
| `KavaKids-Sistema.html` | O sistema inteiro. É só abrir no navegador. |
| `COMO-USAR.txt` | Manual de operação da loja. |

## Como abrir

Baixe o `KavaKids-Sistema.html` e dê dois cliques. Ele abre no Chrome ou Edge.

No Chrome, para virar um ícone na área de trabalho:
menu (⋮) → Salvar e compartilhar → Criar atalho → marque **Abrir como janela**.

## O que faz

- **Venda (PDV)** — leitura por código de barras, desconto, forma de pagamento, cupom
- **Troca** — entrada e saída na mesma operação, com compras avulsas no mesmo atendimento
- **Produtos** — marca, modelo, tamanho, cor, gênero, custo e preço, com markup calculado
- **Clientes** — contato, CPF validado, várias crianças por cliente e aviso de aniversário
- **Estoque** — entradas, saídas, ajuste de inventário e alerta de reposição
- **Vendas** — histórico, 2ª via do cupom, exclusão de venda ou de item com estorno
- **Relatórios** — diário, semanal, mensal, anual, por categoria e por cliente
- **Gestão** — faturamento × custo de aquisição, markup, margem, lucro, capital em estoque

Cupom e relatórios saem em bobina térmica de 80 mm (também 58 mm ou A4).

## Onde ficam os dados

**Os dados NÃO estão neste repositório e nunca são enviados para cá.**

O sistema guarda tudo no armazenamento local do navegador (`localStorage`), na máquina
onde é usado. O arquivo `.html` contém apenas o programa — nenhuma venda, nenhum
produto, nenhum cliente.

Consequências práticas:

- Publicar aqui **não publica dado nenhum** das clientes.
- Cada computador e cada navegador tem seus próprios dados. Não há sincronização.
- Abrir pelo GitHub Pages cria um armazenamento separado do arquivo local.
- Para levar dados de uma máquina para outra: **Configurações → Baixar backup**, e
  **Restaurar backup** na outra.

⚠️ **Os arquivos de backup (`.json`) e as exportações (`.csv`) contêm dados pessoais
das clientes — nome, CPF, telefone, e-mail e data de nascimento de crianças.
Nunca faça commit deles.** O `.gitignore` deste repositório já os bloqueia.

## Backup

O sistema avisa sozinho quando o último backup passa de 7 dias. Guarde o arquivo em
pendrive ou nuvem privada. Limpar os dados de navegação do navegador apaga o sistema.

## Observação fiscal

O cupom é comprovante simples, **sem valor fiscal**. Não substitui NFC-e. Emissão
fiscal exige um emissor autorizado pela Sefaz do estado.
