# Telegram Member Migration - GitHub Actions

Workflow otomatis untuk memindahkan member dari grup Telegram A ke grup B.

## ⚠️ Peringatan

- Telegram ToS melarang spam
- Gunakan delay yang cukup
- Akun harus admin di kedua grup

## Setup

### 1. Dapatkan API Credentials
- Kunjungi [my.telegram.org](https://my.telegram.org)
- Login → API development tools → buat aplikasi
- Catat `api_id` dan `api_hash`

### 2. Tambahkan GitHub Secrets
Repository → Settings → Secrets and variables → Actions:

| Secret | Value |
|--------|-------|
| `TELEGRAM_API_ID` | API ID |
| `TELEGRAM_API_HASH` | API Hash |
| `TELEGRAM_PHONE` | +628xxxx |

### 3. Jalankan Workflow
Actions → Telegram Member Migration → Run workflow
- Input ID grup sumber & tujuan
- Batch size default: 50
- Delay default: 2 detik

## Mendapatkan Group ID
Tambahkan [@userinfobot](https://t.me/userinfobot) ke grup, kirim `/start`.

## Troubleshooting

| Error | Solusi |
|-------|--------|
| FloodWaitError | Tunggu waktu yang ditampilkan |
| PrivacyRestricted | Normal, user di-skip |
| PeerFloodError | Stop, tunggu beberapa jam |
