# Guia de Comandos Linux

Este repositório foi criado como atividade prática da disciplina de Sistemas Operacionais.
Aqui estão 30 comandos básicos do Linux com explicações e exemplos de uso.

---

## Navegação

## ls

**Para que serve:**
O comando ls serve para listar os arquivos e pastas que estão dentro do diretório em que você se encontra. É como abrir uma pasta no Windows e ver o que tem dentro, só que pelo terminal.

**Exemplo de uso:**
```bash
ls
```
Ao rodar esse comando, o terminal vai mostrar todos os arquivos e pastas do local atual.

---

## cd

**Para que serve:**
O comando cd serve para entrar em uma pasta (diretório). Toda vez que você quer acessar uma pasta diferente pelo terminal, usa esse comando.

**Exemplo de uso:**
```bash
cd Documentos
```
Esse comando faz o terminal entrar na pasta chamada Documentos.

---

## pwd

**Para que serve:**
O comando pwd mostra qual é a pasta que você está usando no momento. É útil quando você não sabe mais onde está dentro do sistema de arquivos.

**Exemplo de uso:**
```bash
pwd
```
O terminal vai mostrar algo como: /home/aluno/Documentos

---

## Arquivos

## mkdir

**Para que serve:**
O comando mkdir serve para criar uma pasta nova. Você escolhe o nome e ele cria a pasta no diretório atual.

**Exemplo de uso:**
```bash
mkdir trabalho
```
Esse comando cria uma pasta chamada trabalho onde você está.

---

## touch

**Para que serve:**
O comando touch serve para criar um arquivo vazio. Ele não coloca nenhum conteúdo dentro, só cria o arquivo em si.

**Exemplo de uso:**
```bash
touch arquivo.txt
```
Esse comando cria um arquivo chamado arquivo.txt vazio no diretório atual.

---

## cp

**Para que serve:**
O comando cp serve para copiar arquivos. Você informa o arquivo original e o destino, e ele faz a cópia.

**Exemplo de uso:**
```bash
cp arquivo.txt copia.txt
```
Esse comando cria uma cópia do arquivo.txt com o nome copia.txt na mesma pasta.

---

## mv

**Para que serve:**
O comando mv serve para mover arquivos para outro lugar ou para renomear um arquivo. É como recortar e colar no Windows.

**Exemplo de uso:**
```bash
mv arquivo.txt Documentos/
```
Esse comando move o arquivo.txt para dentro da pasta Documentos.

---

## rm

**Para que serve:**
O comando rm serve para apagar arquivos. É importante tomar cuidado porque no Linux o arquivo não vai para a lixeira, ele é removido diretamente.

**Exemplo de uso:**
```bash
rm arquivo.txt
```
Esse comando apaga o arquivo chamado arquivo.txt permanentemente.

---

## find

**Para que serve:**
O comando find serve para procurar arquivos e pastas no sistema. Você informa onde procurar e o que procurar, e ele lista tudo que encontrar.

**Exemplo de uso:**
```bash
find . -name "*.txt"
```
Esse comando procura todos os arquivos com extensão .txt dentro da pasta atual e das pastas dentro dela.

---

## Texto

## cat

**Para que serve:**
O comando cat serve para mostrar o que está escrito dentro de um arquivo de texto. O conteúdo aparece direto no terminal.

**Exemplo de uso:**
```bash
cat arquivo.txt
```
O terminal vai exibir tudo que está escrito dentro do arquivo.txt.

---

## less

**Para que serve:**
O comando less abre um arquivo para você ler com calma, podendo rolar o texto para cima e para baixo. É melhor que o cat para arquivos grandes. Para sair, aperte a tecla Q.

**Exemplo de uso:**
```bash
less arquivo.txt
```
O arquivo vai abrir no terminal para leitura. Use as setas do teclado para navegar e Q para fechar.

---

## head

**Para que serve:**
O comando head mostra as primeiras linhas de um arquivo. Por padrão ele mostra as 10 primeiras, mas você pode mudar isso.

**Exemplo de uso:**
```bash
head arquivo.txt
```
O terminal vai mostrar as 10 primeiras linhas do arquivo.txt.

---

## tail

**Para que serve:**
O comando tail mostra as últimas linhas de um arquivo. É o oposto do head. Muito usado para ver as últimas mensagens de arquivos de registro do sistema.

**Exemplo de uso:**
```bash
tail arquivo.txt
```
O terminal vai mostrar as 10 últimas linhas do arquivo.txt.

---

## grep

**Para que serve:**
O comando grep serve para buscar uma palavra ou frase dentro de um arquivo. Ele mostra só as linhas que contêm o que você procurou.

**Exemplo de uso:**
```bash
grep "linux" arquivo.txt
```
O terminal vai mostrar todas as linhas do arquivo.txt que contêm a palavra linux.

---

## echo

**Para que serve:**
O comando echo serve para mostrar um texto na tela do terminal. É muito usado em scripts para exibir mensagens.

**Exemplo de uso:**
```bash
echo "Olá, mundo!"
```
O terminal vai imprimir: Olá, mundo!

---

## Sistema

## man

**Para que serve:**
O comando man abre o manual de um comando. Se você não souber como usar um comando, o man explica tudo: o que faz, como usar e quais opções existem. Aperte Q para fechar.

**Exemplo de uso:**
```bash
man ls
```
O terminal vai abrir o manual completo do comando ls.

---

## clear

**Para que serve:**
O comando clear limpa a tela do terminal. Ele não apaga nada, só tira o que está aparecendo na tela para você ter mais espaço para trabalhar.

**Exemplo de uso:**
```bash
clear
```
A tela do terminal fica em branco, como se você tivesse acabado de abrir.

---

## whoami

**Para que serve:**
O comando whoami mostra o nome do usuário que está logado e usando o terminal no momento.

**Exemplo de uso:**
```bash
whoami
```
O terminal vai mostrar algo como: aluno

---

## history

**Para que serve:**
O comando history mostra uma lista com todos os comandos que você digitou no terminal anteriormente. É útil para lembrar o que você fez ou repetir um comando.

**Exemplo de uso:**
```bash
history
```
O terminal vai listar os últimos comandos usados com um número na frente de cada um.

---

## ps

**Para que serve:**
O comando ps mostra quais programas estão em execução no sistema no momento. Cada programa em execução é chamado de processo.

**Exemplo de uso:**
```bash
ps
```
O terminal vai mostrar os processos que estão rodando com o seu usuário, junto com o número de identificação de cada um (PID).

---

## kill

**Para que serve:**
O comando kill serve para encerrar um processo (programa) que está rodando. Você precisa informar o número de identificação do processo, que é chamado de PID. Esse número você consegue com o comando ps.

**Exemplo de uso:**
```bash
kill 1234
```
Esse comando encerra o processo de número 1234.

---

## top

**Para que serve:**
O comando top funciona como o Gerenciador de Tarefas do Windows. Ele mostra ao vivo quais programas estão rodando e quanto de processador e memória cada um está usando. Para sair, aperte Q.

**Exemplo de uso:**
```bash
top
```
O terminal vai abrir uma tela que atualiza sozinha mostrando os processos em execução.

---

## df

**Para que serve:**
O comando df mostra informações sobre o espaço em disco: quanto está ocupado e quanto ainda está disponível. A opção -h deixa os valores mais fáceis de ler (em MB, GB).

**Exemplo de uso:**
```bash
df -h
```
O terminal vai mostrar o espaço usado e livre de cada partição do disco em um formato legível.

---

## du

**Para que serve:**
O comando du mostra quanto espaço um arquivo ou pasta está ocupando no disco. É útil para descobrir o que está usando muito espaço no computador.

**Exemplo de uso:**
```bash
du -sh pasta/
```
O terminal vai mostrar o tamanho total da pasta de forma resumida e legível.

---

## apt

**Para que serve:**
O comando apt é o gerenciador de pacotes do Ubuntu. Com ele você instala, atualiza e remove programas pelo terminal de forma simples. Quase sempre é usado junto com o sudo.

**Exemplo de uso:**
```bash
sudo apt install nome-do-programa
```
Esse comando instala o programa escolhido no sistema. O terminal vai pedir confirmação antes de instalar.

---

## Permissões

## sudo

**Para que serve:**
O comando sudo permite executar um comando com permissão de administrador. Algumas ações no Linux só podem ser feitas por administradores, como instalar programas. O sudo dá essa permissão temporariamente.

**Exemplo de uso:**
```bash
sudo apt update
```
Esse comando atualiza a lista de programas disponíveis no sistema usando permissão de administrador. O terminal vai pedir sua senha.

---

## chmod

**Para que serve:**
O comando chmod serve para mudar as permissões de um arquivo. No Linux, cada arquivo tem permissões que definem quem pode ler, escrever ou executar ele.

**Exemplo de uso:**
```bash
chmod +x script.sh
```
Esse comando dá permissão de execução ao arquivo script.sh, ou seja, permite que ele seja rodado como um programa.

---

## chown

**Para que serve:**
O comando chown serve para mudar o dono de um arquivo ou pasta. Cada arquivo no Linux pertence a um usuário, e o chown permite alterar isso.

**Exemplo de uso:**
```bash
chown aluno arquivo.txt
```
Esse comando muda o dono do arquivo.txt para o usuário chamado aluno.

---

## Rede

## ping

**Para que serve:**
O comando ping serve para testar se o seu computador está conseguindo se comunicar com outro endereço na internet ou na rede local. Ele manda pacotes e mede o tempo de resposta. Para parar, use Ctrl+C.

**Exemplo de uso:**
```bash
ping google.com
```
O terminal vai mostrar se o Google está respondendo e quanto tempo leva cada resposta.

---

## wget

**Para que serve:**
O comando wget serve para baixar arquivos da internet direto pelo terminal. Você só precisa informar o endereço (URL) do arquivo.

**Exemplo de uso:**
```bash
wget https://site.com/arquivo.zip
```
O terminal vai fazer o download do arquivo e salvar na pasta em que você está.

---

