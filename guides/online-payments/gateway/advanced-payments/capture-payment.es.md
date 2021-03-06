---
sites_supported:
  - mla
  - mco
indexable: false
---

# Capturar un Advanced Payment

> WARNING
>
> Contacto comercial requerido
>
> Solo puedes integrar este producto si tu contacto comercial te compartió toda la información necesaria para hacerlo.

La API de Advanced Payment permite realizar pagos del tipo [Autorización y Captura](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/guides/online-payments/checkout-api/other-features). Para estos casos se debe crear un Advanced Payment con el campo `capture` en `false`, el cual reservará el monto hasta que se capture.

Para capturarlo, tienes que hacerlo de la siguiente forma:

### Request
```curl
curl -X PUT \
    -H 'Accept: application/json' \
    -H 'Content-Type: application/json' \
    'https://api.mercadopago.com/v1/advanced_payments/ID?access_token=APPLICATION_TOKEN' \
    -d '{...}'
```

### Body
```json
{
  "capture": true
}
```
