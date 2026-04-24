# 📘 Guia de Comandos Linux

> Trabalho prático — comandos essenciais do GNU/Linux com exemplos.

---

## Navegação

## `ls` — Listar arquivos

**Para que serve:**
Lista os arquivos e pastas do diretório atual. É como abrir uma pasta no explorador de arquivos e ver o que tem dentro.

**Exemplo de uso:**
```bash
ls          # lista básica
ls -l       # lista detalhada (permissões, tamanho, data)
ls -la      # inclui arquivos ocultos (começam com .)
```

---

## `cd` — Mudar diretório

**Para que serve:**
Muda o diretório (pasta) atual. Funciona como clicar numa pasta para entrar nela.

**Exemplo de uso:**
```bash
cd /home/usuario   # vai para a pasta do usuário
cd ..              # volta uma pasta (sobe um nível)
cd ~               # vai direto para o diretório home
```

---

## `pwd` — Mostrar diretório atual

**Para que serve:**
Mostra o caminho completo da pasta em que você está agora. Muito útil quando você se perde navegando pelo terminal.

**Exemplo de uso:**
```bash
pwd
# Saída: /home/usuario/documentos
```

---

## Arquivos

## `mkdir` — Criar pasta

**Para que serve:**
Cria uma nova pasta (diretório). O nome vem de "make directory".

**Exemplo de uso:**
```bash
mkdir minha-pasta                    # cria uma pasta simples
mkdir -p projetos/linux/atividade    # cria toda a estrutura de uma vez
```

---

## `cp` — Copiar arquivos

**Para que serve:**
Copia arquivos ou pastas de um lugar para outro. É como o "Ctrl+C / Ctrl+V" no terminal.

**Exemplo de uso:**
```bash
cp arquivo.txt /backup/       # copia arquivo para a pasta backup
cp -r pasta/ destino/         # copia uma pasta inteira (-r = recursivo)
```

---

## `mv` — Mover ou renomear

**Para que serve:**
Move arquivos e pastas de lugar, ou renomeia. É como o "recortar e colar" do terminal.

**Exemplo de uso:**
```bash
mv relatorio.txt documentos/          # move para outra pasta
mv nome-antigo.txt novo-nome.txt      # renomeia o arquivo
```

---

## `rm` — Remover arquivos

**Para que serve:**
Apaga arquivos permanentemente. Atenção: no Linux não existe lixeira no terminal, o arquivo some de vez!

**Exemplo de uso:**
```bash
rm arquivo.txt          # apaga um arquivo
rm -rf pasta/           # apaga pasta e todo o conteúdo (use com muito cuidado!)
```

---

## `touch` — Criar arquivo vazio

**Para que serve:**
Cria um arquivo vazio, ou se o arquivo já existir, atualiza a data e hora de modificação dele.

**Exemplo de uso:**
```bash
touch novo.txt            # cria um arquivo vazio chamado novo.txt
touch a.txt b.txt c.txt   # cria vários arquivos de uma vez
```

---

## `find` — Buscar arquivos

**Para que serve:**
Procura por arquivos e pastas no sistema usando vários critérios: nome, extensão, tamanho, data, etc.

**Exemplo de uso:**
```bash
find . -name "*.txt"            # busca todos os .txt na pasta atual
find /home -name "relatorio*"   # busca arquivos que começam com "relatorio"
```

---

## Texto

## `cat` — Exibir conteúdo de arquivo

**Para que serve:**
Mostra o conteúdo de um arquivo de texto diretamente no terminal. Ótimo para arquivos pequenos.

**Exemplo de uso:**
```bash
cat README.md                          # exibe o conteúdo do arquivo
cat arquivo1.txt arquivo2.txt          # mostra os dois em sequência
```

---

## `less` — Ler arquivos grandes

**Para que serve:**
Exibe arquivos longos com rolagem, ao contrário do cat que joga tudo de uma vez. Use as setas para navegar e a tecla Q para sair.

**Exemplo de uso:**
```bash
less /var/log/syslog    # lê um arquivo de log grande
less README.md          # navega pelo README com scroll
```

---

## `head` — Primeiras linhas do arquivo

**Para que serve:**
Mostra as primeiras linhas de um arquivo. Por padrão exibe as 10 primeiras, mas você pode escolher quantas quer.

**Exemplo de uso:**
```bash
head arquivo.txt          # mostra as 10 primeiras linhas
head -n 20 arquivo.txt    # mostra as 20 primeiras linhas
```

---

## `tail` — Últimas linhas do arquivo

**Para que serve:**
Mostra as últimas linhas de um arquivo. Com -f fica monitorando em tempo real, muito útil para acompanhar logs.

**Exemplo de uso:**
```bash
tail arquivo.txt           # mostra as 10 últimas linhas
tail -f /var/log/syslog    # fica atualizando ao vivo (Ctrl+C para sair)
```

---

## `grep` — Buscar texto em arquivos

**Para que serve:**
Procura por palavras ou padrões dentro de arquivos. É como o Ctrl+F do editor, mas no terminal.

**Exemplo de uso:**
```bash
grep "erro" arquivo.log          # busca a palavra "erro" no arquivo
grep -r "senha" /etc/            # busca em todos os arquivos da pasta /etc
```

---

## `echo` — Exibir mensagem

**Para que serve:**
Exibe um texto na tela do terminal. Muito útil para mostrar o valor de variáveis ou para escrever conteúdo em arquivos.

**Exemplo de uso:**
```bash
echo "Olá, Linux!"                    # imprime o texto na tela
echo "linha nova" >> arquivo.txt      # adiciona texto ao final de um arquivo
```

---

## Sistema

## `man` — Manual dos comandos

**Para que serve:**
Abre o manual completo de qualquer comando. Se não souber como usar algo, use o man! É o equivalente ao F1 do Linux. Pressione Q para sair.

**Exemplo de uso:**
```bash
man ls      # abre o manual do comando ls
man grep    # veja todas as opções do grep
```

---

## `clear` — Limpar a tela

**Para que serve:**
Limpa toda a tela do terminal, deixando-o sem bagunça visual. Você também pode usar o atalho Ctrl+L.

**Exemplo de uso:**
```bash
clear    # limpa a tela (o histórico de comandos continua salvo)
```

---

## `whoami` — Quem está logado

**Para que serve:**
Mostra o nome do usuário que está usando o terminal agora. Útil quando você está em servidores ou trocando de usuário.

**Exemplo de uso:**
```bash
whoami
# Saída: usuario
```

---

## `ps` — Listar processos

**Para que serve:**
Mostra uma lista dos processos (programas) que estão em execução no sistema naquele momento.

**Exemplo de uso:**
```bash
ps             # mostra processos do usuário atual
ps aux         # mostra todos os processos do sistema com detalhes
```

---

## `kill` — Encerrar processo

**Para que serve:**
Encerra um processo em execução usando o seu número de identificação (PID), que você consegue com o comando ps.

**Exemplo de uso:**
```bash
kill 1234         # encerra o processo de ID 1234 normalmente
kill -9 1234      # força o encerramento imediato (último recurso)
```

---

## `top` — Monitor do sistema

**Para que serve:**
Exibe em tempo real o consumo de CPU, memória e os processos em execução. É como o Gerenciador de Tarefas do Windows, mas no terminal. Pressione Q para sair.

**Exemplo de uso:**
```bash
top      # abre o monitor interativo (atualiza a cada 3 segundos)
```

---

## `df` — Espaço em disco

**Para que serve:**
Mostra o espaço usado e disponível em cada partição do disco. O -h deixa os números legíveis (KB, MB, GB).

**Exemplo de uso:**
```bash
df -h      # exibe o uso de disco em formato legível (human-readable)
```

---

## `du` — Tamanho de arquivos e pastas

**Para que serve:**
Mostra quanto espaço cada arquivo ou pasta está ocupando. Muito útil para descobrir o que está consumindo o disco.

**Exemplo de uso:**
```bash
du -sh pasta/       # mostra o tamanho total da pasta
du -sh *            # mostra o tamanho de tudo no diretório atual
```

---

## `history` — Histórico de comandos

**Para que serve:**
Mostra todos os comandos que você digitou anteriormente no terminal. Útil para relembrar ou reutilizar comandos.

**Exemplo de uso:**
```bash
history              # mostra todo o histórico
history | grep ls    # filtra o histórico mostrando só os comandos com ls
```

---

## `apt` — Gerenciador de pacotes

**Para que serve:**
Gerencia a instalação, atualização e remoção de programas no Ubuntu e Debian. Precisa do sudo para instalar.

**Exemplo de uso:**
```bash
sudo apt update              # atualiza a lista de programas disponíveis
sudo apt install git         # instala o Git
sudo apt remove programa     # desinstala um programa
```

---

## Permissões

## `sudo` — Executar como administrador

**Para que serve:**
Executa um comando com privilégios de administrador (root). O nome vem de "Super User Do". Necessário para instalar programas, alterar configurações do sistema, etc.

**Exemplo de uso:**
```bash
sudo apt update         # atualiza a lista de pacotes (requer senha)
sudo rm /etc/arquivo    # remove arquivo protegido do sistema
```

---

## `chmod` — Alterar permissões

**Para que serve:**
Muda as permissões de leitura, escrita e execução de arquivos e pastas. Controla quem pode fazer o quê com cada arquivo.

**Exemplo de uso:**
```bash
chmod +x script.sh       # dá permissão de execução ao script
chmod 644 arquivo.txt    # dono lê/escreve; outros só leem
```

---

## `chown` — Alterar proprietário

**Para que serve:**
Muda quem é o dono de um arquivo ou pasta. Muito usado em servidores para controlar o acesso a arquivos.

**Exemplo de uso:**
```bash
chown usuario arquivo.txt          # muda o dono do arquivo
chown -R usuario:grupo pasta/      # muda dono e grupo de toda a pasta
```

---

## Rede

## `ping` — Testar conexão de rede

**Para que serve:**
Testa se um servidor ou endereço está acessível pela rede. Mostra o tempo de resposta. Use Ctrl+C para parar.

**Exemplo de uso:**
```bash
ping google.com       # verifica se o Google está acessível
ping 8.8.8.8          # faz ping no servidor DNS do Google pelo IP
```

---

## `wget` — Baixar arquivos da internet

**Para que serve:**
Faz o download de arquivos diretamente pelo terminal, apenas informando a URL. Funciona mesmo sem interface gráfica.

**Exemplo de uso:**
```bash
wget https://exemplo.com/arquivo.zip      # baixa o arquivo no diretório atual
wget -O novo-nome.zip https://url.com     # baixa e salva com outro nome
```

---

