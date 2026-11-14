# [Proje adı]

[2–4 cümle: proje ne, kimin için, şu anki ana hedef. Senin rolün (ajan) ne, karar kimde.]

## Okuma sırası

**Her şeyi okuma.** Oturum başında yalnız şunlar, bu sırayla:

1. `context/DEVIR.md` — son oturumun devir notu: neredeyiz, sıradaki
2. `context/PROJE.md` — amaç, durum, yapılacaklar

`context/KARARLAR.md` bir karara atıf görünce (`K-03`) ya da karar gerekince açılır.
**Bir işe başlarken o işin skill'ini oku** (`.claude/skills/`): skill o işin adımlarını ve o işte yaşanmış hataları taşır. Bağlam dosyalarına bir şey yazmadan önce `baglam-guncelleme` skill'ini oku.

## Dosyalar

| Dosya | Ne | Ne zaman |
|---|---|---|
| `AGENTS.md` | bu dosya | her oturum |
| `context/DEVIR.md` | devir notu | her oturum başı; oturum sonunda baştan yazılır |
| `context/PROJE.md` | amaç, durum, yapılacaklar | her oturum başı |
| `context/KARARLAR.md` | numaralı kararlar | karar gerekince |
| `.claude/skills/<iş>/SKILL.md` | iş başına talimat + yaşanmış hatalar | o işe başlarken |
| [klasör ya da dosya] | [ne] | [ne zaman] |

## Kurallar

1. **Bilgi tek yerde yaşar;** diğer dosyalar numara (`K-NN`) ya da yolla atıf yapar. Güncelleme anında ve kısa.
2. **Bakmadan "oldu" deme.** Çıktıyı kendin aç, çalıştır ya da ölç. [Projeye göre: ör. "her görsel değişikliği kareyle kontrol et", "testleri çalıştır".]
3. **Uydurma.** Bilmiyorsan "bilmiyorum" de; tahmini "tahmin" diye yaz.
4. **Karar [senin adın]'da:** [ör. konu, görsel yön, son metin, yayın]. Bunların dışında karar gerektirmeyeni onay beklemeden yap, bitmiş işi göster. "Dur" denince dur.
5. **Kapanmış karar yeniden tartışılmaz;** yapılacaklardan madde silinmez, bitince işaretlenir.
6. **Şifreler ve API anahtarları** yalnız [ör. `.env`]'de; bağlam dosyalarına girmez.
[7. Projeye özgü kuralların. Her kural gerekçesiyle: "şunu yap, çünkü …"]

## Çalışma

[Dil ve üslup (ör. "benimle her zaman Türkçe yaz"), uzun işler arka planda mı, dosyaları kim siler, git kullanılıyor mu.]
