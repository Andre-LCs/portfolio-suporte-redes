# 🛠️ Procedimento: Formatação via WinPE (DiskPart / Clean All)

## 📌 Cenário
Utilizado em casos de disco corrompido, falha de sistema ou necessidade de formatação completa.

## 📌 Procedimento

Quando abre o WinPE, ele automaticamente executa o script para passar imagem.

Tem que fechar aquela tela e apertar as teclas **Ctrl + C** para cancelar o script de implantação.

Vai aparecer algo como:
"selecione Y para continuar e N para cancelar"

Aperta **Y** e dá Enter para confirmar.

---

Depois disso, execute:


diskpart


O CMD vai entrar no modo DiskPart do Windows.

---

Selecione o disco que contém os arquivos (normalmente é o disco 0, mas se tiver mais de um HD pode ser o 1).


select disk 0


(ou 1, dependendo do caso)

---

Após selecionar o disco que vai ser formatado, execute:


clean all


Esse comando faz a limpeza completa do disco, zerando todos os bits (formatação low level).

---

## ⏱️ Observações

- O processo pode demorar bastante  
- Em HDD é mais lento  
- O CMD pode não avisar quando termina  
- Pode apertar espaço de vez em quando para verificar  

Se tiver mais de um disco, repetir o processo para o outro.

---

## 🔄 Finalização

Após terminar:

- Pode desligar o computador  
- Reiniciar e verificar se funcionou  

---

## ⚠️ Importante

Após o CMD estar aberto, pode remover o pendrive que o ambiente continuará funcionando.
