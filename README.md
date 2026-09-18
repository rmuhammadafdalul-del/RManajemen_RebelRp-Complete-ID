# RManajemen_RebelRp

Bot Discord Node.js + discord.js + SQLite, siap untuk GitHub dan Railway/hosting Node.js.

## Setup slash command
- `/setup` atau `/setup ticket` — membuat/menyiapkan channel `create-ticket` di kategori Support dan memasang panel Report/Formulir/Donasi.
- `/setup role` — memasang panel pengambilan role dan selalu menambahkan tombol **Warga** menggunakan `ROLE_WARGA_ID`.
- `/setup welcome` — mengaktifkan sistem welcome untuk server menggunakan `WELCOME_CHANNEL_ID`.
- `/setup goodbye` — mengaktifkan sistem goodbye untuk server menggunakan `GOODBYE_CHANNEL_ID`.
- `/panel` — kirim panel ticket.
- `/rolepanel` — kirim panel role.

## Variables
Salin `.env.example` ke environment variables hosting. Gunakan ID Discord, bukan nama channel/kategori/role.

Wajib:
- `DISCORD_TOKEN`
- `CLIENT_ID`
- `GUILD_ID`
- `STAFF_ROLE_ID`
- `SUPPORT_CATEGORY_ID`
- `DONATION_CATEGORY_ID`
- `REPORT_CATEGORY_ID`
- `FORM_CATEGORY_ID`
- `LOG_CHANNEL_ID`
- `ROLE_PANEL_CHANNEL_ID`
- `ROLE_WARGA_ID`

`CREATE_TICKET_CHANNEL_ID` boleh dikosongkan; `/setup` akan membuat `create-ticket` di kategori Support.

## Penting
Bot harus mempunyai permission **Manage Channels**, **Manage Roles**, **Send Messages**, **View Channels**, **Read Message History**, dan **Embed Links**. Untuk self-role, role bot harus berada di atas role yang diberikan.

Welcome/Goodbye sengaja tidak aktif sebelum `/setup welcome` dan `/setup goodbye` dijalankan. Status aktivasi disimpan di SQLite.
