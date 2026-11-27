# Convite de Formatura

Convite digital baseado no layout que você enviou.

## Como ver

Abra `index.html` no navegador, ou sirva a pasta:

```bash
cd convite && python3 -m http.server 8080
```

Depois acesse `http://127.0.0.1:8080`.

## Conteúdo

- **Mensagem:** você é meu convidado de honra
- **Data:** 28 de dezembro de 2026, às 19h
- **Local:** quadra do colégio
- **RSVP:** QR Code (WhatsApp com mensagem de confirmação)

## Personalizar o QR Code

O QR atual abre o WhatsApp com uma mensagem pronta de confirmação. Para apontar para outro link (formulário, site, WhatsApp pessoal):

1. Edite a URL em `assets/rsvp-url.txt`
2. Gere um novo QR e salve em `assets/qr.png`

Exemplo com Python:

```bash
python3 - <<'PY'
import qrcode
url = open("assets/rsvp-url.txt").read().strip()
# ou troque aqui:
# url = "https://seu-link-de-confirmacao"
img = qrcode.make(url)
img.save("assets/qr.png")
print("QR atualizado")
PY
```

## Trocar a foto

Substitua `assets/formanda.jpg` por uma foto em alta resolução (de preferência o arquivo original, não print de tela).
