# 🌐 Diretório Público - App Mail Send

Este diretório contém os arquivos que são acessíveis publicamente via navegador.

---

## 🗂 Arquivos e Pastas

- `index.php` → Tela principal com formulário para envio de e-mail  
- `processa_envio.php` → Faz a chamada para o envio do e-mail (chama o arquivo privado)  
- `logo.png` → Logo do aplicativo  
- Arquivos de **CSS** ou imagens adicionais usadas na interface  

---

## ⚠️ Observações

- Este diretório **não deve conter credenciais ou arquivos sensíveis**.  
- Os arquivos de configuração do SMTP e PHPMailer estão fora do diretório público, em `../../app_send_mail/`, para maior segurança.  
- Qualquer alteração nos arquivos públicos deve preservar a chamada correta para os arquivos privados.

---

## 🚀 Como Acessar

1. Coloque este diretório dentro da pasta `htdocs` do XAMPP.  
2. Acesse `http://localhost/nome-do-diretorio/` no navegador.  
3. O formulário de envio estará disponível na `index.php`.

