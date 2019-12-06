# ngrok

[Dashboard](https://dashboard.ngrok.com/status)

## ssh gateway
`ssh -R 0:localhost:22 tunnel.us.ngrok.com tcp 22`

## Authtoken Setup
`ngrok authtoken <YOUR_AUTHTOKEN>`

## RSA Key Setup
[Docs](https://ngrok.com/docs#ssh-gateway-public-key)

## Sample Output
```
ngrok by @inconshreveable

Tunnel Status                 online
Version                       2.0/2.0
Web Interface                 http://127.0.0.1:4040
Forwarding                    http://92832de0.ngrok.io -> localhost:80
Forwarding                    https://92832de0.ngrok.io -> localhost:80

Connnections                  ttl     opn     rt1     rt5     p50     p90
                              0       0       0.00    0.00    0.00    0.00
```
