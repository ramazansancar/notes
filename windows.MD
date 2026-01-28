# Windows

## PM2 Kullanımı

### Next.js Uygulaması Başlatma

Normalde Linux ve MacOS için kullanılan PM2 komutu `pm2 start npm --name "whois" -- start -p 7000` Windows ortamında çalışmayabilir.

```bash
pm2 start node_modules/next/dist/bin/next --name "whois" -- start -p 7000
```
