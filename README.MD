# Notlar

## Regex

```js
regexOnlyLetter: /^([a-zA-ZğüşöçıİĞÜŞÖÇ]+\s?)*\s*$/,
regexOnlyNumber: /^[0-9]*$/
regexNameSurname: /^([a-zA-ZğüşöçıİĞÜŞÖÇ]{2,})+(?: [a-zA-ZğüşöçıİĞÜŞÖÇ]{2,})+(?:)$/,
email: /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/,
hex: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/i
regexUrl: /^https?:\/\/(?:www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b(?:[-a-zA-Z0-9()@:%_\+.~#?&\/=]*)$/
regexUrl2: new RegExp("^(?!mailto:)(?:(?:http|https|ftp)://|//)(?:\\S+(?::\\S*)?@)?(?:(?:(?:[1-9]\\d?|1\\d\\d|2[01]\\d|22[0-3])(?:\\.(?:1?\\d{1,2}|2[0-4]\\d|25[0-5])){2}(?:\\.(?:[0-9]\\d?|1\\d\\d|2[0-4]\\d|25[0-4]))|(?:(?:[a-z\\u00a1-\\uffff0-9]+-*)*[a-z\\u00a1-\\uffff0-9]+)(?:\\.(?:[a-z\\u00a1-\\uffff0-9]+-*)*[a-z\\u00a1-\\uffff0-9]+)*(?:\\.(?:[a-z\\u00a1-\\uffff]{2,})))|localhost)(?::\\d{2,5})?(?:(/|\\?|#)[^\\s]*)?$","i"),
regexUrlMixed: /^(?:(?:https?|ftp):\/\/)?(?:(?!(?:10|127)(?:\.\d{1,3}){3})(?!(?:169\.254|192\.168)(?:\.\d{1,3}){2})(?!172\.(?:1[6-9]|2\d|3[0-1])(?:\.\d{1,3}){2})(?:[1-9]\d?|1\d\d|2[01]\d|22[0-3])(?:\.(?:1?\d{1,2}|2[0-4]\d|25[0-5])){2}(?:\.(?:[1-9]\d?|1\d\d|2[0-4]\d|25[0-4]))|(?:(?:[a-z\u00a1-\uffff0-9]-*)*[a-z\u00a1-\uffff0-9]+)(?:\.(?:[a-z\u00a1-\uffff0-9]-*)*[a-z\u00a1-\uffff0-9]+)*(?:\.(?:[a-z\u00a1-\uffff]{2,})))(?::\d{2,5})?(?:\/\S*)?$/,
regexNickname: {
  default: {
    regex: /^[A-Za-z0-9]+([A-Za-z0-9]*|[._-]?[A-Za-z0-9]+)*$/,
    regexKey: null,
    idKey: null,
    hashLimit: [0, 0]
  },
  trdefault: {
    regex: /^([a-zA-ZğüşöçıİĞÜŞÖÇ]+\s?)*\s*$/,
    regexKey: null,
    idKey: null,
    hashLimit: [0, 1]
  },
  discord: { // Source: https://support.discord.com/hc/tr/articles/12620128861463#h_01H3WYG79F9Q5PTEZYMYM1A0GW
    regex: /^[a-zA-Z0-9\._-]{2,32}+#[0-9]{1,4}$/, 
    regexKey: /#[0-9]{1,4}$/,
    idKey: '#',
    hashLimit: [1, 4]
  },
  riot: { // Source: https://support-leagueoflegends.riotgames.com/hc/tr/articles/360041788533-Riot-ID-SSS
    regex: /^[a-zA-Z]+#[a-zA-Z0-9]{2,4}$/, 
    regexKey: /#[a-zA-Z0-9]{2,4}$/,
    idKey: '#',
    hashLimit: [2, 4]
  },
  pubg: { // Source: https://support.pubg.com/hc/tr/articles/360002193033-Nick-de%C4%9Fi%C5%9Ftirme
    regex: /[a-z]\$[0-9]{3,5}$/,
    regexKey: /\$[0-9]{3,5}$/,
    idKey: '$',
    hashLimit: [3, 5]
  },
  steamId: { // Source: https://help.steampowered.com/tr/faqs/view/2816-BE67-5B69-0FEC | https://stackoverflow.com/a/37018670/15030183
    regex: /^[0-9]{17}$/,
    regexKey: null,
    idKey: null,
    hashLimit: [0, 0]
  },
  epicgames: { // Source: https://www.epicgames.com/help/tr/epic-hesaplari-c5719348850459/hesap-guvenligi-c5719366891291/epic-hesabi-kimligi-nedir-ve-nerede-bulabilirim-a5720265298075
    regex: /^[a-fA-F0-9]{32}$/,
    regexKey: null,
    idKey: null,
    hashLimit: [0, 0]
  },
}
```

## Google Yardımcı Bağlantılar

- [Google UTM Etiketi (Kampanya Bağlantısı) Oluşturucu](https://ga-dev-tools.google/campaign-url-builder/)
- **Google Drive'da Dosya Önizlemesi**
  Web sitelerinde Google Drive'da bulunan dosyaların önizlemesini yapmak için aşağıdaki bağlantıları kullanabilirsiniz. Embed kodu olarak kullanabilirsiniz. [Kaynak 1](https://gist.github.com/tzmartin/1cf85dc3d975f94cfddc04bc0dd399be) | [Kaynak 2](https://gist.github.com/samuelkarani/d850971294629298d4a350d3913607dd) | [Kaynak 3 (Arşiv Bağlantısı)](https://web.archive.org/web/20161201144824/http://www.labnol.org/internet/google-docs-viewer-alternative/) | [Kaynak 4](https://www.labnol.org/internet/direct-links-for-google-drive/28356/) [Tarayıcı Eklentisi](https://dov.parishod.com/) | [Wordpress Eklentisi (Kaynak Kodu)](https://github.com/awsmin/Embed-Any-Documents) | [Wordpress Eklentisi](https://wordpress.org/plugins/embed-any-document/)
  - <https://docs.google.com/gview?embedded=true&url=[FILE_URL]>
  - <https://docs.google.com/viewer?url=[FILE_URL]>
  - <https://drive.google.com/viewerng/viewer?embedded=true&url=[FILE_URL]>
    - [FILE_URL]: .pdf|.doc|.docx|.ppt gibi dosya uzantıların bağlantısı olmalıdır.
  - <https://drive.usercontent.google.com/download?id=[DRIVE_ID]>

## Google Dorklar

- `site:ramazansancar.com.tr` - Site içerisinde arama yapar.
- `site:ramazansancar.com.tr text:"blog"` - Site içerisinde `blog` kelimesinin geçtiği açıklamaları arar.
- `site:ramazansancar.com.tr intitle:"blog"` - Site içerisinde başlıkta `blog` kelimesini arar.
- `site:ramazansancar.com.tr inurl:"blog"` - Site içerisinde `blog` kelimesi geçen bağlantıları arar.
- `site:google.com filetype:pdf` - Site içerisinde `.pdf` uzantılı dosyaları arar. (Genellikle e-kitaplar, dokümanlar için kullanılır. Özellikle üniversite web sitelerinde kullanılır.)
- `site:google.com ext:pdf` - Site içerisinde `.pdf` uzantılı dosyaları arar. (Genellikle e-kitaplar, dokümanlar için kullanılır. Özellikle üniversite web sitelerinde kullanılır.)
- `site:ramazansancar.com.tr -inurl:"www"` - Site içerisinde `www` kelimesi geçen bağlantıları aramaz! (`-` işareti ile kelime/cümleyi aramadan dışlarsınız.)
- `site:ramazansancar.com.tr -inurl:"www" -inurl:"blog"` - Site içerisinde `www` ve `blog` kelimelerinin geçtiği bağlantıları aramaz!
- `site:ramazansancar.com.tr -inurl:"www" -inurl:"blog" -inurl:"admin"` - Site içerisinde `www`, `blog` ve `admin` kelimelerinin geçtiği bağlantıları aramaz!

## Link Kısaltma Servisleri

- [l24.im](https://l24.im/)
- [4am.click](https://4am.click/)
- [t.ly](https://t.ly/)
  - [linkunshorten.com](https://linkunshorten.com/)

## Az Bilinen Mini Oyunlar

- [florr.io](https://florr.io/) powered by [m28 studio](https://m28.studio/)
- [digdig.io](https://digdig.io/) powered by [m28 studio](https://m28.studio/)
- [diep.io](http://diep.io/) powered by [m28 studio](https://m28.studio/)
- [agar.io](https://agar.io/) powered by [m28 studio](https://m28.studio/)

## Web Kontrol Panelleri

- [Hestia Control Panel](https://hestiacp.com/)

## Veriler

- [Kickstarter Veri Seti](https://webrobots.io/kickstarter-datasets/)
- [Indiegogo Veri Seti](https://webrobots.io/indiegogo-dataset/)
- [Data Hub](https://datahub.io/search)
- [Hugging Face](https://huggingface.co/datasets)

## 3D Tasarım Şablonları

- [Thingiverse](https://www.thingiverse.com/)
- [Printables](https://www.printables.com/)
- [Thangs](https://thangs.com/)
- [Pinshape](https://pinshape.com/)
- [Cults 3D](https://cults3d.com/)
- [Yeggi](https://www.yeggi.com/)
- [Creality Cloud](https://www.crealitycloud.com/)

## Windows Komutları

- Cihaazın maksimum desteklediği ram miktarını görme (kb cinsinden): `wmic memphysical get maxcapacity` [Kaynak 1](https://teknoseyir.com/durum/1617041#comment-5812149) | [Kaynak 2](https://www.timetecinc.com/dram/check-maximum-ram-capacity-computer/)

## İş İlanları

- [Jobs.lu](https://en.jobs.lu/)
- [ICTJob.lu](https://www.ictjob.lu/en/job-search/)
- [Monster.lu](https://www.monster.lu/en/)
- [Indeed.lu](https://lu.indeed.com/)
- [Jobfinder.lu](https://www.jobfinder.lu/)
- [Job Today](https://jobtoday.com/en/)
- [Work in Luxembourg](https://work-in-luxembourg.lu/offers)
- [Luxembourg Tech Jobs](https://www.luxembourgtechjobs.lu/)
- [Luxembourg Jobs](https://www.luxembourg-jobs.com/)
- [Moovijob](https://en.moovijob.com/job-offers/jobs-luxembourg)
- [Jobs in Luxembourg](https://www.jobsinluxembourg.eu/)

### Kullanılabilir Bildirimler

> [!NOTE]
> Information the user should notice even if skimming.

.

> [!IMPORTANT]
> Essential information required for user success.

.

> [!WARNING]
> Dangerous certain consequences of an action.

.

> [!TIP]
> Optional information to help a user be more successful.

.

> [!CAUTION]
> Negative potential consequences of an action.

- [Kaynak 1](https://github.com/orgs/community/discussions/16925)
- [Kaynak 2](https://learn.microsoft.com/en-us/contribute/content/markdown-reference#alerts-note-tip-important-caution-warning)
- [Kaynak 3](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)

### Github Emojilar :smile:

[Kaynak 1](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#using-emoji)
[Kaynak 2 - Emoji Listesi](https://github.com/ikatyang/emoji-cheat-sheet)
