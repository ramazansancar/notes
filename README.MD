# Notlar

## Regex

```js
    regexOnlyLetter: /^([a-zA-ZğüşöçıİĞÜŞÖÇ]+\s?)*\s*$/,
    regexOnlyNumber: /^[0-9]*$/
    regexNameSurname: /^([a-zA-ZğüşöçıİĞÜŞÖÇ]{2,})+(?: [a-zA-ZğüşöçıİĞÜŞÖÇ]{2,})+(?:)$/,
    regexUrl: /^(?:(?:https?|ftp):\/\/)?(?:(?!(?:10|127)(?:\.\d{1,3}){3})(?!(?:169\.254|192\.168)(?:\.\d{1,3}){2})(?!172\.(?:1[6-9]|2\d|3[0-1])(?:\.\d{1,3}){2})(?:[1-9]\d?|1\d\d|2[01]\d|22[0-3])(?:\.(?:1?\d{1,2}|2[0-4]\d|25[0-5])){2}(?:\.(?:[1-9]\d?|1\d\d|2[0-4]\d|25[0-4]))|(?:(?:[a-z\u00a1-\uffff0-9]-*)*[a-z\u00a1-\uffff0-9]+)(?:\.(?:[a-z\u00a1-\uffff0-9]-*)*[a-z\u00a1-\uffff0-9]+)*(?:\.(?:[a-z\u00a1-\uffff]{2,})))(?::\d{2,5})?(?:\/\S*)?$/,
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

### Kullanılabilir Bildirimler

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

[Kaynak 1](https://github.com/orgs/community/discussions/16925)
[Kaynak 2](https://learn.microsoft.com/en-us/contribute/content/markdown-reference#alerts-note-tip-important-caution-warning)
[Kaynak 3](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)

### Github Emojilar :smile:

[Kaynak 1](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#using-emoji)
[Kaynak 2 - Emoji Listesi](https://github.com/ikatyang/emoji-cheat-sheet)