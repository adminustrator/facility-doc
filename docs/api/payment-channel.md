---
sidebar_position: 1
---

# Payment Channel

Melampirkan metode pembayaran yang dipakai untuk transaksi pada Fasilitas yang tersedia di OneSmile.

## Endpoint

<kbd>POST</kbd> `/payment-channel/FACILITY`

## Request Parameters

### Header Parameters

| Header Parameter   |  Status  |  Type  | Description        |
| ------------------ | :------: | :----: | ------------------ |
| **X-Auth-Account** | required | string | authorized account |

## Responses

### 200 - Success

```json
{
    "success": true,
    "msg": "Success",
    "data": [
        {
            "code": "VABNIXENDIT_FACILITY",
            "name": "Bank BNI",
            "description": "Pembayaran Melalui Virtual Account BNI",
            "method": "<div>     <p style=\"margin-bottom: 5px\">1. Pembayaran melalui ATM/MBANKING</p> <p style=\"margin-bottom: 5px\">2. Pilih menu “Transfer”</p> <p style=\"margin-bottom: 5px\">3. Pilih menu “Virtual Account Billing”</p>  <p style=\"margin-bottom: 5px\">4. Masukkan nomor Virtual Account pada menu “Input Baru”</p>  <p style=\"margin-bottom: 5px\">5. Periksa kembali nominal transaksi sudah benar</p>  <p style=\"margin-bottom: 5px\">6. Konfirmasi Transaksi dan Masukkan Password Transaksi</p> </div>",
            "type": "Transfer Virtual Account",
            "logo": "https://api.onesmile.digital/img/pembayaran/bni.png"
        },
        {
            "code": "VAMANDIRIXENDIT_FACILITY",
            "name": "Bank Mandiri",
            "description": "Pembayaran Melalui Virtual Account Mandiri",
            "method": "<div>     <p style=\"margin-bottom: 5px;\">1. Pembayaran melalui ATM/MBANKING</p>      <p style=\"margin-bottom: 5px;\">2. Pilih menu “Bayar” </p>      <p style=\"margin-bottom: 5px;\">3. Masukkan nomor Virtual Account</p>      <p style=\"margin-bottom: 5px;\">4. Periksa kembali nominal transaksi sudah benar</p>      <p style=\"margin-bottom: 5px;\">5. Konfirmasi Transaksi</p> </div>",
            "type": "Transfer Virtual Account",
            "logo": "https://api.onesmile.digital/img/pembayaran/mandiri.png"
        },
        {
            "code": "VABRIXENDIT_FACILITY",
            "name": "Bank BRI",
            "description": "Pembayaran Melalui Virtual Account BRI",
            "method": "<div>     <p style=\"margin-bottom: 5px;\">1. Pembayaran melalui ATM/MBANKING</p>     <p style=\"margin-bottom: 5px;\">2. Pilih menu “Virtual Account Billing”</p>     <p style=\"margin-bottom: 5px;\">3. Masukkan nomor Virtual Account</p>     <p style=\"margin-bottom: 5px;\">4. Periksa kembali nominal transaksi sudah benar</p>     <p style=\"margin-bottom: 5px;\">5. Konfirmasi Transaksi dan Klik “Bayar”</p> </div>",
            "type": "Transfer Virtual Account",
            "logo": "https://api.onesmile.digital/img/pembayaran/bri.png"
        },
        {
            "code": "OVO_FACILITY",
            "name": "OVO",
            "description": "Pembayaran Melalui Aplikasi Ovo",
            "method": "<div>     <p style=\"margin-bottom: 5px;\">1. Buka Aplikasi OVO</p>      <p style=\"margin-bottom: 5px;\">2. Buka “Inbox”</p>      <p style=\"margin-bottom: 5px;\">3. Pilih Tagihan</p>      <p style=\"margin-bottom: 5px;\">4. Masukkan PIN OVO</p>      <p style=\"margin-bottom: 5px;\">5. Transaksi berhasil</p> </div>",
            "type": "Wallet",
            "logo": "https://api.onesmile.digital/img/pembayaran/rQNAFW47a8s4sVxCeZ0M7b4jaRzJUjQdgDvtjGKm.png"
        },
        {
            "code": "DANA_FACILITY",
            "name": "DANA",
            "description": "Pembayaran Melalui Aplikasi Dana",
            "method": "<div>     <p style=\"margin-bottom: 5px;\">1. Masukkan No Handphone yang terdaftar di DANA</p>      <p style=\"margin-bottom: 5px;\">2. Masukkan PIN DANA</p>      <p style=\"margin-bottom: 5px;\">3. Transaksi berhasil</p> </div>",
            "type": "Wallet",
            "logo": "https://api.onesmile.digital/img/pembayaran/logo_dana.png"
        }
    ]
}
```

### 401 - Unauthorized Account

```json
{
  "status": false,
  "msg": "Unauthorized account"
}
```
