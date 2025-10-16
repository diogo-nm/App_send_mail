# 🔒 Diretório de Arquivos Sensíveis - App Mail Send

Este diretório contém arquivos que **não devem ser expostos publicamente**, pois possuem credenciais e configurações confidenciais para envio de e-mails.

---

## 🗂 Arquivos Principais

- `processa_envio.php` → Classe e lógica para envio de e-mails utilizando PHPMailer  
- `bibliotecas/PHPMailer/` → Bibliotecas do PHPMailer necessárias para envio  

---

## ⚠️ Configurações Sensíveis

Dentro do arquivo `processa_envio.php`, existem **três informações críticas** que **devem ser preenchidas pelo usuário**:

```php
$mail->setFrom('SEU_EMAIL', 'NOME_REMETENTE'); // Email do remetente
$mail->Username = 'SEU_EMAIL';                 // Usuário SMTP
$mail->Password = 'SUA_SENHA_DE_APLICATIVO';   // Senha SMTP
```
## 🔑 Sobre a Senha de Segurança (App Password)

Para enviar e-mails usando serviços como Gmail, **não é recomendado usar a senha principal da sua conta**.  
Em vez disso, você deve criar uma **Senha de Aplicativo (App Password)** para uso no PHPMailer.

### 📝 Como gerar a senha:

1. Acesse sua conta do Gmail.
2. Clique em **Gerenciar sua conta Google**
3. Vá em **Segurança** → **Senhas de App**.
4. Escolha o aplicativo como `app_send_mail`.
5. Clique em **Gerar**.
6. Copie a senha gerada (uma sequência de 16 caracteres) e **use no lugar de `$mail->Password`** no arquivo `processa_envio.php`, **sem espaço entre os caracteres**.

```php
$mail->Password = 'SUA_SENHA_DE_APLICATIVO';
```

### ⚠️ Nunca exponha suas credenciais

Nunca exponha sua conta de e-mail ou a **Senha de Aplicativo** em repositórios públicos.  
Essas informações são sensíveis e podem ser usadas por terceiros para enviar e-mails em seu nome, comprometendo a segurança da sua conta.

### 🔒 Boas práticas

- Mantenha o arquivo que contém o `$mail->Username` e `$mail->Password` **fora do diretório público** do seu projeto.
- Use variáveis de ambiente (`.env`) ou arquivos de configuração fora da pasta pública para armazenar suas credenciais.
- Revogue senhas de aplicativo antigas caso não estejam mais em uso.
- Teste sempre em **ambientes locais** antes de subir para produção.
