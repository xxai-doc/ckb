<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

بەشێک لە کۆدی ماڵپەڕەکە سەرچاوە کراوە، بەخێربێن بۆ یارمەتیدانی باشترکردنی وەرگێڕانەکە.

## کۆدی پێشەوە

* [کۆدی پێشەوە](https://github.com/xxai-art/web)
* [پاکێجی زمان بۆ سایتەکە بە گشتی](https://github.com/xxai-art/web/tree/main/i18n)
* [پاکێجی زمان بۆ مۆدیولەکانی چوونەژوورەوە](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [بەڵگەنامەی فرە زمانی ماڵپەڕ](https://github.com/xxai-doc)

زمانی بەرنامەسازی پێشەوە [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) ە، کە هەندێک تایبەتمەندی زیاد دەکات لەسەر بنەمای ڕستەسازی coffeescript، سەیری [./coffee_plus.md](./coffee_plus.md) بکە.

## بەنێودەوڵەتیکردنی ماڵپەڕ و بەڵگەنامەکان

لەسەر ئەم ٣ پڕۆژەیەی خوارەوە بنیات بنێن

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  پاشگرەکە `.mdt` ە، دەتوانیت ڕستەسازی هاوشێوەی `<+ ./coffee_plus/import.js>` بەکاربهێنیت بۆ ئاماژەدان بە پەڕگە دەرەکییەکان، و بە پاشگری `.md` markdown دروست بکەیت.

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  وەرگێڕانی مارکداون کۆد و بەستەرەکان وەرناگێڕێت، و ڕستە وەرگێڕدراوەکان لە کاشدا دەکات. ئەگەر وەرگێڕانەکە دەستکاری کرا بەڵام دەقی ئەسڵی دەستکاری نەکرا، دووبارە جێبەجێکردنی دەستکاریکردنی وەرگێڕانەکە نانووسێتەوە.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  فایلە زمانییەکان بۆ وەرگێڕانی ماڵپەڕە دروستکراوەکانی `yaml` .

### ڕێنماییەکانی ئۆتۆماتیکی وەرگێڕانی بەڵگەنامە

سەیری کۆگاکە بکە [xxai-art/doc](https://github.com/xxai-art/doc)

پێشنیار دەکرێت سەرەتا nodejs و [direnv](https://direnv.net) و [bun](https://github.com/oven-sh/bun) دابمەزرێنیت، پاشان `direnv allow` جێبەجێ بکەیت دوای چوونە ژوورەوەی ناوەڕۆکەکە.

بۆ ئەوەی کۆگای زۆر گەورە نەبێت کە وەرگێڕدرابێتە سەر سەدان زمان، کۆگایەکی کۆدی جیاوازم بۆ هەر زمانێک دروستکرد و ڕێکخراوێکم دروستکرد بۆ هەڵگرتنی ئەم کۆگایە

ڕێکخستنی گۆڕاوەی ژینگە `GITHUB_ACCESS_TOKEN` و پاشان بەڕێوەبردنی [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) بە شێوەیەکی ئۆتۆماتیکی کۆگاکە دروست دەکات.

بێگومان دەتوانیت بیخەیتە کۆگایەکیشەوە.

ئاماژەی سکریپتی وەرگێڕان [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

کۆدی سکریپتەکە بەم شێوەیە لێکدەدرێتەوە:

[bunx](https://bun.sh/docs/cli/bunx) جێگرەوەی npx ە کە خێراترە. بێگومان ئەگەر bun ـت دانەناوە، دەتوانیت لە جیاتی ئەوە `npx` بەکاربهێنیت.

`bunx mdt zh` `.mdt` لە ناوەڕۆکی zh بە `.md` پیشان دەدات، سەیری ٢ فایلە بەستراوەکەی خوارەوە بکە

* [قاوە_پلۆس.مد.ت](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [قاوە_پلۆس.مد](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` کۆدی سەرەکییە بۆ وەرگێڕان (ئەگەر تەنها `nodejs` ت داناوە، بەڵام `bun` و `direnv` دانەنراون، دەتوانیت `npx i18n` یش جێبەجێ بکەیت بۆ وەرگێڕان).

[i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) شی دەکاتەوە، ڕێکخستنی `i18n.yml` لەم بەڵگەنامەیەدا بەم شێوەیە:

```
en:
zh: ja ko en
```

واتاکەی ئەوەیە: وەرگێڕانی چینی بۆ زمانی ژاپۆنی، کۆری، ئینگلیزی، ئینگلیزی بۆ هەموو زمانەکانی تر. ئەگەر تەنها دەتەوێت پشتگیری چینی و ئینگلیزی بکەیت، دەتوانیت تەنها بنووسیت `zh: en` .

دواهەمینیان [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) ە کە ناوەڕۆکی نێوان ناونیشانی سەرەکی و ژێرنووسی یەکەمی `README.md` ی هەر زمانێک دەردەهێنێت بۆ دروستکردنی زانیاری `README.md` . کۆدەکە زۆر سادەیە، دەتوانیت خۆت سەیری بکەیت.

Google API بۆ وەرگێڕانی بێبەرامبەر بەکاردێت. ئەگەر ناتوانیت بچیتە ناو گووگڵەوە، تکایە پرۆکسییەک ڕێکبخە و ڕێکبخە، وەک:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

سکریپتی وەرگێڕان کاشێکی وەرگێڕان لە ناوەڕۆکی `.i18n` دروست دەکات، تکایە بە `git status` پشکنینی بۆ بکە و زیاد بکە بۆ کۆگای کۆدەکان بۆ ئەوەی وەرگێڕان دووبارە نەبێتەوە.
