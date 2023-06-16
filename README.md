<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Disarankeun pikeun masang nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) heula, lajeng `direnv allow` sanggeus ngasupkeun diréktori ( [nu .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) bakal dieksekusi otomatis sanggeus ngasupkeun diréktori).

Hartina nyaéta: Tarjamahan Cina ka Jepang, Korea, Inggris, Inggris tarjamahan ka sadaya basa séjén. Upami anjeun ngan ukur hoyong ngadukung Cina sareng Inggris, anjeun ngan ukur tiasa nyerat `zh: en` .

## kode hareup-tungtung

* [kode hareup-tungtung](https://github.com/xxai-art/web)
* [Bungkusan basa pikeun situs sacara gembleng](https://github.com/xxai-art/web/tree/main/i18n)
* [Bungkusan basa pikeun modul login](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Dokuméntasi Multilingual Website](https://github.com/xxai-doc)

Basa programming hareup-tungtung nyaeta [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , nu nambihan sababaraha fitur dumasar kana sintaksis coffeescript, tingali [./coffee_plus.md](./coffee_plus.md) .

## Internasionalisasi situs wéb sareng dokumén

Ngawangun dina 3 proyék di handap ieu

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Sufiksna nyaéta `.mdt` , anjeun tiasa nganggo sintaksis anu sami sareng `<+ ./coffee_plus/import.js>` pikeun ngarujuk kana file éksternal, sareng ngahasilkeun markdown sareng sufiks `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Tarjamahan Markdown moal narjamahkeun kodeu sareng tautan, sareng bakal nyéépkeun kalimat anu ditarjamahkeun. Lamun tarjamahan dirobah tapi téks aslina teu dirobah, ngajalankeun deui moal nimpa modifikasi tarjamahan.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  File basa pikeun narjamahkeun halaman wéb `yaml` .

### Dokumén Tarjamahan Automation Parentah

Tempo gudang kode [xxai-art/doc](https://github.com/xxai-art/doc)

Disarankeun pikeun masang nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) heula, lajeng `direnv allow` sanggeus ngasupkeun diréktori ( [nu .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) bakal dieksekusi otomatis sanggeus ngasupkeun diréktori).

Pikeun ngahindarkeun dasar kode anu ageung ditarjamahkeun kana ratusan basa, kuring nyiptakeun dasar kode anu misah pikeun unggal basa sareng nyiptakeun organisasi pikeun nyimpen basis kode.

Nyetél variabel lingkungan `GITHUB_ACCESS_TOKEN` teras ngajalankeun [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) bakal otomatis nyiptakeun gudang kode.

Tangtosna, anjeun ogé tiasa nempatkeun éta dina dasar kode.

Rujukan naskah tarjamah [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Kode naskah diinterpretasikeun kieu:

[bunx](https://bun.sh/docs/cli/bunx) mangrupakeun gaganti pikeun npx, nu leuwih gancang. Tangtosna, upami anjeun teu acan dipasang bun, anjeun tiasa nganggo `npx` .

`bunx mdt zh` renders `.mdt` dina diréktori zh salaku `.md` , tingali 2 file numbu handap

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` nyaéta kode inti pikeun tarjamahan (lamun ngan boga `nodejs` dipasang, tapi `bun` na `direnv` teu dipasang, anjeun ogé tiasa ngajalankeun `npx i18n` narjamahkeun).

Bakal parse [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , konfigurasi `i18n.yml` dina dokumén ieu nyaéta kieu:

```
en:
zh: ja ko en
```

Hartina nyaéta: Tarjamahan Cina ka Jepang, Korea, Inggris, Inggris tarjamahan ka sadaya basa séjén. Upami anjeun ngan ukur hoyong ngadukung Cina sareng Inggris, anjeun ngan ukur tiasa nyerat `zh: en` .

Panungtungan nyaéta [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , nu extracts eusi antara judul utama jeung subjudul kahiji `README.md` unggal basa pikeun ngahasilkeun entri `README.md` . Kodeu basajan pisan, anjeun tiasa ningali éta nyalira.

Google API dianggo pikeun tarjamahan gratis. Upami anjeun teu tiasa ngaksés Google, mangga konfigurasi sareng setel proxy, sapertos:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Skrip tarjamah bakal ngahasilkeun cache ditarjamahkeun dina diréktori `.i18n` , mangga parios deui kalawan `git status` tur tambahkeun ka Repository kode pikeun nyegah tarjamahan ulang.

Punten ngajalankeun `bunx i18n` unggal waktos anjeun ngarobih tarjamahan pikeun ngapdet cache.

Upami téks asli sareng tarjamahan dirobih sakaligus, cache bakal bingung, janten upami anjeun hoyong ngarobih, anjeun ngan ukur tiasa ngarobih hiji, teras ngajalankeun `bunx i18n` pikeun ngapdet cache.
