<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.seni

Bagian tina kode ramatloka mangrupa open source, wilujeng sumping pikeun mantuan ngaoptimalkeun tarjamah.

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
