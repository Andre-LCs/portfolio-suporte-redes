# 🛠️ Limpeza, manutenção e reparo de sistema Windows

# Sequência de comando para fazer uma limpeza/manutenção/conserto de chave de registro corrompidas e reparo de arquivos corrompidos ou ausentes.

# 1. Verifica a integridade da imagem do Windows
DISM /Online /Cleanup-Image /ScanHealth

# 2. Repara a imagem do sistema
DISM /Online /Cleanup-Image /RestoreHealth

# 3. Verifica e corrige arquivos do sistema
sfc /scannow

Executando esses comandos nessa ordem, pelo prompt, será feita a limpeza/restauração do sistema e o computador vai ficar BALA.

---

Se a máquina/dispositivo der problema de não inicialização (não carrega Windows, fica reparando ad infinitum, não carrega boot), aplicar o seguintes comandos no prompt:
chkdsk C: /f /r /x

---

## 📖 Glossário de comandos CHKDSK

Quer saber como executar o disco de verificação de outras maneiras? Aqui estão alguns outros comandos que você pode usar ao executar uma verificação de disco no Prompt de Comando:

- **chkdsk** - Verifica se há problemas na unidade padrão e no sistema de arquivos sem corrigir ou reparar.

- **chkdsk [letra da unidade]:** - Faz o mesmo, mas para a unidade especificada.

- **/f** - O "f" significa "fix" e, neste caso, significa corrigir as informações do sistema de arquivos para que ele o direcione para os arquivos corretos.

- **/r** - O "r" significa "repair”. O /r localiza partes corrompidas do disco rígido e tenta recuperar os arquivos que estavam armazenados nelas.

- **/x** - Desmonta a unidade antes de executar o CHKDSK, o que pode ser necessário para que ele seja executado.

- **/f /r /x** - Executa os comandos /f e /r em uma unidade desmontada.

- **/scan** - Faz a verificação do disco sem desmontá-lo (somente possível com NTFS).

- **/b** - Redefine a lista de clusters defeituosos (partes danificadas do disco) e refaz a verificação deles.

- **/v** - Verifica o disco, mas exibe os nomes dos arquivos enquanto o faz.

- **/i** - Uma verificação mais rápida e menos minuciosa, em que as entradas do índice são examinadas superficialmente e não verificadas profundamente.

- **/c** - Outro tipo de verificação superficial, que não verifica os ciclos nas pastas.
