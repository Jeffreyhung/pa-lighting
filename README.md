# 聲光技術筆記 · Sound & Lighting Notes

音響（PA）與舞台燈光的技術筆記，中文與 English 兩個版本，內容整理自國立中興大學聲光工程社的研習營講義。
Technical notes on live sound (PA) and stage lighting, in 中文 and English, compiled from the training-camp handouts of the Sound & Lighting Engineering Club at National Chung Hsing University (NCHU).

網站 Site: <https://jeffreyhung.github.io/pa-lighting/> （English: `/en/`）

> 這是個人整理的筆記，不是社團或學校的官方網站。
> This is a personal compilation, not an official site of the club or the university.

## 關於中興大學聲光社

**國立中興大學聲光工程社**（聲光社）是負責校內活動音響與燈光的學生社團。依社課介紹，社團的宗旨是：

- 協助管理學務處課外活動指導組的聲光器材
- 培養對聲音、燈光工程有興趣的社員，組成共同維護與操作器材的團隊
- 協助校內各系學會、社團舉辦晚會等活動，讓活動更有聲光效果

社課內容包括燈光與 PA 大堂課、搭場、混音機操作、線材維修、燈光 Console 操作。要代表學務處大聲公器材管理委員會出借及操作器材，必須通過筆試與機台操作考，取得「聲光證」。

### 沿革

| 年份 | 事件 |
| --- | --- |
| 民國 74 年（1985） | 興大購置第一批聲光器材。講義記載，據說當時全國各大學只有中興大學有這樣的器材 |
| 民國 77 年（1988） | 器材數量增加到足以舉辦一場大型晚會或舞會 |
| 民國 79 年（1990） | 斥資約三百萬元購入一批聲光器材。當時 Bose 802 II 喇叭一組購價約十二萬元，24 軌混音機報價將近三十萬元 |
| 其後 | 歷屆器材室學長姐與課外活動指導組陸續增添器材；每年舉辦一次「聲光工程研習營」訓練校內聲光人才，至少辦到第二十八屆 |
| 民國 101 年（2012） | 器材室轉型為**聲光工程社**，目標是建立可長久運作的器材使用與管理制度，並有固定經費維修、汰換器材 |
| 民國 102 年（2013） | 學務處大聲公器材管理委員會於 12 月 24 日第一次會議通過聲光器材借用辦法，之後多次修正（最近一次見於 113 年，2024） |
| 民國 103 學年度（2014–15） | 社課介紹記載，學年末舉辦聲光證的筆試與操作考 |
| 約民國 104–106 年（2015–17） | 研習營改以「大聲公人才招募營」名稱舉辦；本站主講義為第一屆的講義 |

資料來源：主講義〈興大聲光器材與研習營的演進〉一節、〈聲光社社課介紹〉簡報，以及[國立中興大學學務處聲光器材借用辦法](https://www.osa.nchu.edu.tw/osa/act/rule/rule1/1-23_1130520.pdf)。講義之後的社團近況不在這些資料裡。

## About the NCHU Sound & Lighting Club

The **Sound & Lighting Engineering Club** (聲光工程社, usually 聲光社) at National Chung Hsing University in Taichung, Taiwan, is the student club that runs sound and lighting for campus events. According to the club's own course introduction, it exists to:

- help manage the sound and lighting equipment owned by the Office of Student Affairs
- train members who are interested in sound and lighting engineering to maintain and operate that equipment as a team
- support department associations and other clubs with their shows and events

Its classes cover PA and lighting fundamentals, load-in, mixer operation, cable repair and lighting consoles. To lend out and operate equipment on behalf of the university's equipment committee, a member must pass a written and hands-on test for a sound-and-lighting operator certificate (聲光證).

### History

| Year | Event |
| --- | --- |
| 1985 | NCHU buys its first sound and lighting equipment. The handout notes that, reportedly, no other university in Taiwan had such equipment at the time |
| 1988 | The inventory grows large enough to run a full-scale evening show or dance |
| 1990 | About NT$3 million is spent on new equipment. A pair of Bose 802 II speakers cost about NT$120,000 and a 24-channel mixer was quoted at nearly NT$300,000 |
| Afterwards | Successive students of the equipment room and the Extracurricular Activities Section keep adding equipment, and run an annual Sound & Lighting Engineering Workshop to train operators; it reached at least a 28th edition |
| 2012 | The equipment room becomes the **Sound & Lighting Engineering Club**, aiming for a lasting system for using and managing the equipment, with a regular budget for repair and replacement |
| 2013 | The Office of Student Affairs equipment committee adopts the equipment loan rules on 24 December; they have been amended several times since, most recently in 2024 |
| 2014–15 | The club's course introduction records operator-certificate exams at the end of the academic year |
| c. 2015–17 | The workshop is held under a new name, 大聲公人才招募營; the main handout on this site is from its first edition |

Sources: the history section of the main handout, the club's course-introduction slides, and the university's published [equipment loan rules](https://www.osa.nchu.edu.tw/osa/act/rule/rule1/1-23_1130520.pdf). These sources say nothing about the club after that period.

## Repository layout

```
docs/
  zh/            中文 pages (default language, served at /)
  en/            English pages (served at /en/)
  assets/img/    all figures, shared by both languages
                 name.png     = original figure
                 name-en.png  = English version of a figure
sources/         original handouts the notes were compiled from (not published on the site)
mkdocs.yml       site config and navigation
requirements.txt pinned build dependencies
```

Each page exists at the same path in `docs/zh/` and `docs/en/`; that is what lets the
language switcher jump between translations. When you add a page, add it in both folders
under the same file name and list it once in `nav:` in `mkdocs.yml`.

## Publishing

The site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).
The workflow in `.github/workflows/pages.yml` builds and deploys it on every push to `main`
(repository **Settings → Pages → Source** must be set to **GitHub Actions**).

## Preview locally

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve          # http://127.0.0.1:8000
```

## Security notes

- The site is fully static and makes no third-party requests: fonts are system fonts
  (`font: false`) and search runs in the browser from a local index.
- Build dependencies are pinned in `requirements.txt`; GitHub Actions are pinned to commit SHAs
  and the workflow uses least-privilege permissions. Update the pins deliberately.
