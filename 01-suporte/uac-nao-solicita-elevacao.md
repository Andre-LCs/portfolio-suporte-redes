# 🛠️ Problema: UAC não solicita elevação

## 📌 Contexto
Usuário não conseguia executar programas como administrador.

## 🔍 Diagnóstico
- Sistema não mostrava janela de confirmação
- UAC desativado no registro

## 🛠️ Solução
Ativado via comando:

reg add HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v EnableLUA /t REG_DWORD /d 1

## ✅ Resultado
Sistema voltou a solicitar elevação normalmente.

## 📘 Aprendizado
Alterações no registro impactam diretamente permissões do sistema.
