---
name: baglam-guncelleme
description: Bu projede bağlam dosyalarına (AGENTS.md, context/PROJE.md, DEVIR.md, KARARLAR.md, skill'ler) bir şey yazarken — karar, hata/ders, ilerleme, devir notu, yeni dosya, oturum sonu, kullanıcı "devir" deyince — MUTLAKA önce bunu oku. Neyin nereye ve ne kadar yazılacağını anlatır.
---

# Bağlam nasıl güncellenir

**Bilgi tek yerde yaşar;** diğer dosyalar numarayla ya da yolla atıf yapar. Güncelleme **anında** yapılır (oturum sonuna bırakılmaz) ve **kısa** yazılır: olay değil sonuç.

## Neyi nereye yazarım

| Ne oldu | Nereye | Nasıl |
|---|---|---|
| Kullanıcı bir karar verdi | `context/KARARLAR.md` sonuna `### K-NN · başlık — kim (tarih)` | Ne / Neden / Gizli ayrıntı. Sıradaki numarayı dosyanın başında güncelle |
| Bir hata yaşandı, ders çıktı | O **işin skill'i**, "Bu işte yaşanmış hatalar" | Önce var olan maddeye bak; aynı kök sebepse ona kısa örnek ekle. Yeni madde yalnız yeni kök sebep için. Hiçbir skill'e uymuyorsa yeni skill aç (`ornek-is`'i kopyala) |
| Bir iş bitti | `context/PROJE.md` "Yapılacaklar" | `- [x] ~~madde~~ → sonuç (dosya)`, "Bitenler"e indir |
| Durum değişti (araç, sürüm, ilerleme) | `context/PROJE.md` "Durum" hücresi | Üstüne yaz |
| Yeni dosya/klasör açıldı | `AGENTS.md` "Dosyalar" tablosu | Ne olduğu + ne zaman okunacağı |
| Oturum bitiyor / kullanıcı "devir" dedi | `context/DEVIR.md` | **Baştan yaz** (eskisinin altına ekleme), en çok ~30 satır |

## Yazım kuralları

- Tarihler mutlak (2026-11-14), "dün" değil.
- Gerekçesiz kural yazma: "şunu yap, çünkü …".
- Ölçmediğini ölçülmüş gibi yazma; tahmin "tahmin" diye.
- Şifre ve API anahtarı hiçbir bağlam dosyasına yazılmaz.

## Dosyaları yalın tutma

- AGENTS + DEVIR + PROJE kısa kalır; her oturumda okunuyorlar. Büyüyen ayrıntı ilgili skill'e ya da ayrı bir dosyaya iner (ve `AGENTS.md` tablosuna girer).
- Aynı bilgiyi iki dosyaya yazma; biri eskir.
