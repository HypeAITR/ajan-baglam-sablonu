# Ajan bağlam şablonu

Yapay zekâ ajanıyla (Claude Code, Codex, Gemini CLI, Cursor…) birden çok oturum süren bir iş yapıyorsan, ajan her yeni oturumda her şeyi unutur. Bu şablon o unutmayı azaltmak için küçük bir dosya düzeni: ajan oturum başında birkaç kısa dosya okur, neredeyiz, neye karar verdik, sıradaki ne bilir; yaşadığı hatalar da bir dahaki sefere işin talimat dosyasında durur.

Bu bizim video kurgusunda kullandığımız düzenin **sade hâli**. Hepsi bu kadar değil; başlangıç noktası. Kendi işine göre büyüt.

## Ne var

```
AGENTS.md                         giriş: proje ne, okuma sırası, kurallar   (ajan ilk bunu okur)
CLAUDE.md, GEMINI.md              tek satır: "AGENTS.md'yi oku" (bu adları arayan araçlar için)
context/PROJE.md                  amaç, şu anki durum, yapılacaklar
context/DEVIR.md                  son oturumun devir notu (her oturum sonunda baştan yazılır)
context/KARARLAR.md               numaralı kararlar: ne, kim, neden
.claude/skills/baglam-guncelleme/ neyin nereye yazılacağı (ajan için)
.claude/skills/ornek-is/          bir iş için talimat dosyası örneği; kopyala, kendi işine çevir
```

## Nasıl başlanır

1. Bu klasördeki dosyaları kendi proje klasörüne kopyala.
2. Ajanı o klasörde aç ve şunu yaz:

   ```text
   AGENTS.md'yi oku. Sonra bana projemi sorarak köşeli parantezli [ ... ] yerleri doldur.
   Bilmediğin yere "henüz yok" yaz, uydurma.
   ```

3. Her oturumun sonunda: `"devir" yaz, DEVIR.md'yi güncelle.` Yeni oturumun başında: `AGENTS.md'yi ve okuma sırasını oku.`

## Neden böyle

- **Az oku, tam devral.** Her şeyi oturum başında okutursan ajan dikkatini kaybeder, büyük dosyayı atlar. Başta yalnız kısa dosyalar; gerisi iş gerektirince.
- **Bilgi tek yerde.** Aynı şey iki dosyada yazılırsa biri eskir. Diğer dosyalar numarayla (`K-03`) atıf yapar.
- **Karar yazılı.** "Bunu neden böyle yapmıştık?" sorusunun cevabı `KARARLAR.md`'de; ajan kapanmış kararı her oturumda yeniden tartışmaz.
- **Hata, işin talimatına yazılır.** Ajan bir hatayı bir kez yaşadıysa, o işin skill dosyasına kısa bir "desen" olarak eklenir; ayrı bir uzun "dersler" listesi kimse tarafından okunmaz.

## Büyütmek istersen

İş büyüdükçe bizim de yaptığımız gibi: `context/` içine dosya haritası (hangi dosya nerede, ne zaman okunur), yol haritası, kararları konu başına ayrı dosyalar, her tekrar eden iş için ayrı skill. Bir dosya her oturumda baştan sona okunmayacak kadar büyüdüyse bölme zamanı gelmiştir.

`.claude/skills/` klasörünü Claude Code okur. Başka bir araç kullanıyorsan talimat ve skill dosyalarını nerede aradığına o aracın belgesinden bak.
