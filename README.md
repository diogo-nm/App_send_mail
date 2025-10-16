# 📧 App Mail Send

**App Mail Send** é um aplicativo simples para envio de e-mails diretamente do navegador, desenvolvido em PHP com interface Bootstrap. Este projeto permite enviar mensagens para destinatários especificados, com assunto e corpo do e-mail (sem a possibilidade de anexar arquivos) em HTML.

---

## ⚡ Funcionalidades

- Formulário de envio de e-mail.
- Validação básica de campos (destinatário, assunto e mensagem).
- Envio de e-mails usando **PHPMailer** via SMTP.
- Feedback visual para sucesso ou erro no envio.
- Interface responsiva com Bootstrap 4.

---

## 🗂 Estrutura de Pastas

```text
├── index.php                 # Tela principal com formulário de envio
├── processa_envio.php        # Chama o envio de e-mail usando a biblioteca PHPMailer
├── logo.png                  # Logo do app
├── bibliotecas/PHPMailer/    # Bibliotecas PHPMailer (privadas)
└── processa_envio.php        # Script privado de envio de e-mails (fora do diretório público)
```
⚠️ Alguns arquivos são sensíveis e não devem ser expostos publicamente:
processa_envio.php (com credenciais do SMTP) e a pasta bibliotecas/PHPMailer/.

## 🛠 Tecnologias Utilizadas

- PHP 7.x ou superior  
- PHPMailer  
- Bootstrap 4  
- SMTP (ex.: Gmail)  

---

## 🚀 Como Usar Localmente

1. Instale o **XAMPP** ou outro servidor local PHP.  
2. Coloque os arquivos públicos dentro da pasta `htdocs` do XAMPP.  
3. Garanta que os arquivos privados (como `processa_envio.php` com credenciais) estejam **fora da pasta pública** por segurança.  
4. Acesse `http://localhost/seu-projeto/` no navegador.  
5. Preencha o formulário com:
   - **Para**: e-mail do destinatário  
   - **Assunto**: assunto do e-mail  
   - **Mensagem**: conteúdo do e-mail  
6. Clique em **Enviar Mensagem**.  
7. Você verá o feedback de sucesso ou erro.

---

## 🔐 Arquivos Sensíveis

- `processa_envio.php` → contém credenciais de SMTP  
- `bibliotecas/PHPMailer/` → biblioteca de envio de e-mails  

> ⚠️ Não envie esses arquivos para repositórios públicos.

---

## 💡 Observações

- Para Gmail, é necessário permitir **apps menos seguros** ou gerar **senha de app** se a conta tiver autenticação em 2 fatores.  
- O envio de e-mails depende da configuração SMTP correta.

