# Application Document Package Generator — User Guide

A document-organising tool usable by **any applicant** for application review (書審 / document screening) materials.
Pure local, offline-capable, usable from a single file.


<div align="center">

## Demo Preview

A 12-second walkthrough of the core workflow: create an application package, configure required items, drag files in for auto-categorisation, check for missing items, and export the submission checklist. The video is a canvas-rendered simulation; to try the real tool, double-click `index.html` in your browser.

<video controls width="640" src="assets/demo-preview.webm"></video>

</div>

---

## 1. What It Is

When applying to universities, graduate schools, or various programmes, each school requires different materials with
different deadlines — the worst fears are "missing one document" or "putting a file in the wrong place."

This tool helps you do these things:

1. **Inventory**: List exactly what each application package requires, item by item (required / optional separated).
2. **Categorise**: Drag files from a folder in; the system automatically suggests which item each file belongs to based on the filename.
3. **Check**: Missing items are flagged with a red light, and completion is calculated; files with duplicate content are caught via SHA-256.
4. **Export**: Generate a submission checklist (Markdown / CSV) and a suggested folder structure — just place the files accordingly.
5. **Handwriting**: Items that must be handwritten (e.g. autobiography, study plan) can be marked "需手寫" (needs handwriting) and typeset for printing with the built-in manuscript-paper generator.
6. **Bilingual**: The interface can switch between 繁體中文 (Traditional Chinese) / English, and the checklist can also be exported in a chosen language.

### Privacy & Security

- All computation happens **in your browser**; **files are never uploaded** to any server.
- **Offline usable**: `index.html` is a single file — no network needed, no external sites contacted.
- To protect privacy, the tool **does not save file contents** — it only keeps filenames, sizes, relative paths and SHA-256 hashes in the local browser.
- Text typed in the manuscript paper also stays only in your local browser (never uploaded), and you can delete it at any time with the "清空" (Clear) button.

---

## 2. Getting Started

1. Locate `index.html` and **double-click** to open it in a browser (Chrome, Edge, Safari, Firefox all work).
2. You can bookmark the tool on your desktop or put it on a USB drive — copying the whole `書審資料包產生器` folder is enough to use it.
3. On first use, try pressing **「載入示範」 (Load Demo)** to see what two application packages look like, then press **「清空全部資料」 (Clear All Data)** to start fresh.

---

## 3. Five Steps to Finish Your Application Package

### Step 1: Create an Application Package

In "① 申請包與應繳項目" (Application Packages & Required Items):

- Choose a template (**常見七項** "Common Seven Items" or **空白** "Blank"), then press "＋ 新增申請包" (＋ Add Package).
- Create one package per school / department, e.g. "○○大學｜△△學系" (○○ University | △△ Department).
- Fill in the school name and department; the note field can hold deadlines or special rules.

### Step 2: Configure Required Items

In each package's item list you can:

- **Rename**: Click the input box directly, e.g. change "學習計畫／讀書計畫" (Study Plan / Reading Plan) to "讀書計畫" (Reading Plan).
- **Set required / optional**: Tick "必繳" (Required) — completion only counts required items.
- **Mark as handwritten**: Tick "需手寫" (Needs Handwriting); a "稿紙" (Manuscript Paper) button then appears next to the item (usage in Section 5).
- **Set keywords**: Use the right-side "自動歸類關鍵字（逗號分隔）" (Auto-categorise keywords, comma-separated) to decide which item a file belongs to; e.g. for autobiography use "自傳, 自述".
- **Add / delete / reorder**: Adjust with the buttons on the right.
- Press "＋ 匯入預設範本項目" (＋ Import Default Template Items) to restore the common seven items in one click (existing ones are not duplicated).

> Please **configure items according to that school's prospectus** — neither add extra nor omit any; don't force in things the prospectus doesn't require.

### Step 3: Add Files

In "② 檔案歸類" (File Categorisation):

- Drag a **whole folder** or a batch of files **into the dashed box**; or press "選擇檔案" (Choose Files) / "選擇整個資料夾" (Choose Folder).
- The system **automatically suggests** an item for each file based on filename keywords. If a suggestion is wrong, you can change it in the next step.
- The "自動判斷／優先歸入" (Auto-judge / Prioritise Into) option above lets you decide which application package this round of imported files counts toward first.

### Step 4: Manually Adjust Categorisation

Each file row has two dropdowns on the right:

- The left selects the **application package**, the right selects the **item**.
- Leave uncertain files as "（未歸類）" (Uncategorised) for now and handle them at the end.
- Press "重新自動歸類未歸類檔" (Re-auto-categorise Uncategorised Files) to let the system guess again.
- The "內容重複" (Duplicate Content) tag means this file's content is identical to another file (same SHA-256).

### Step 5: Check Missing Items & Export the Checklist

In "③ 缺件檢查" (Missing-Item Check):

- 🟢 Ready　🔴 Missing (required)　⚪ Optional not attached
- The statistics row above shows required-item completion, number of missing items, and number of duplicate-content groups.

In "④ 匯出繳件清單" (Export Submission Checklist):

- **Download Markdown (.md)**: The full checklist, ready to paste into a note app.
- **Download CSV**: Opens directly in Excel / Numbers (Traditional Chinese encoding is handled).
- **Copy Suggested Folder Structure**: Paste it for yourself or hand it to an AI assistant to help move files.
- The preview area below shows the checklist content in sync; you can select and copy it manually.

---

## 4. Switching Language (繁體中文 / English)

1. After opening the page, look at the **top-right corner** — there are two buttons: `繁體中文` and `English`.
2. Press `English` and the whole interface (titles, buttons, hints, checklist columns) **instantly** becomes English; press `繁體中文` to switch back.
3. Your choice is **remembered automatically** — next time you open it, the same language is used (change it anytime with those two buttons).

**Exporting the checklist in a different language (independent of the interface)**

4. Go to "④ 匯出繳件清單" (Export Submission Checklist) and find the **export language** dropdown; select `繁體中文` or `English`.
5. Then press **Download Markdown** or **Download CSV** — the exported checklist is in that language (e.g. select English and the title becomes `# Application Document Checklist`).
6. The export-language choice is also **remembered automatically**.

> Use case: keep the interface in Chinese for your own convenience, and export the checklist in English to hand to an English-speaking recommender or a foreign school.

---

## 5. Handwriting Manuscript Paper (Mark as Handwritten → Generate Grid Paper → Print)

**First, mark the item**

1. In "① 申請包與應繳項目" (Application Packages & Required Items), find the item to be handwritten (e.g. "自傳" Autobiography) and tick **「需手寫」 (Needs Handwriting)** on the right.
2. After ticking, a **「稿紙」 (Manuscript Paper)** button appears on that item; this tick is saved, and will still be there next time you open the tool.

**Then generate the paper**

3. Press the **「稿紙」** button on that item — a "稿紙－（學校｜項目）" (Manuscript Paper – School | Item) window pops up.
4. **Type or paste** your content in the large box on the left (e.g. the full autobiography); grid paper grows **live** on the right.
5. The top shows **character count / line count / page count / character limit**; exceeding the limit shows a **red warning** (telling you how many characters over); raise the limit or trim the content and the warning disappears, showing "尚可再寫 N 字" (N characters left).

**Adjusting appearance (left panel)**

6. **Style**: `方格` (Grid — one character per cell, most common), `橫線` (Horizontal Lines), `空白` (Blank) — pick one.
7. **Characters per line**: 20–24, adjust per the prospectus (page count recalculates after changes).
8. **Line spacing**: 1.0–1.5×, so characters don't crowd together.
9. **Character limit**: enter 0 for unlimited; or enter the prospectus limit (e.g. 1000 characters for an autobiography).
10. **Font**: choose `標楷體／楷體（建議）` (BiauKai / Kai — recommended), `手寫體（行楷／手寫風）` (Handwriting style), `圓體` (Round), `黑體（對照用）` (Hei — for reference); after choosing, tick **「字型預覽」 (Font Preview)** and the screen displays in that font (unticked uses the normal system font, saving resources).
11. To start over, press **「清空」 (Clear)**.

**Printing**

12. Press **「列印」 (Print)** to open the browser print window; the print range is **the manuscript paper only** (buttons and panels are hidden automatically), one A4 sheet per page — print it out and write in the cells directly.
13. Close the window: press ✕ in the top-right corner or click outside the window; the `Esc` key also works.

> Tip: the manuscript paper exists to help you **align with the grid** — what's printed is blank grid lines plus the text you typed. If the prospectus requires **fully handwritten** content, treat the text as a "character count and layout rehearsal" and write the actual content by hand following the grid.

---

## 6. Suggested Physical Workflow

The tool only does planning and checking — it **cannot and will not** automatically move files on your computer (browser security restrictions; the tool also cannot read full disk paths). Suggested workflow:

1. Build all application packages and items in the tool.
2. Export the "suggested folder structure" and create folders on your computer accordingly, e.g.:

```
書審資料包/
├─ ○○大學｜△△學系/
│  ├─ 個人資料表（必繳）
│  ├─ 成績單（必繳）
│  ├─ 自傳（必繳）
│  ├─ 學習計畫（必繳）
│  ├─ 推薦函（必繳）
│  └─ 其他有利資料（選繳）
└─ □□大學｜◇◇學程/
   └─ ...
```

3. Put files into the corresponding folders (**copy** rather than cut — keep the originals as the safest option).
4. Return to the tool, press "選擇整個資料夾" (Choose Folder) and drag the organised folder in to re-check — confirm there are no red lights.

---

## 7. Saving Settings & Switching Devices

- Packages, items and categorisation results are **saved automatically in this device's browser** and resume automatically next time.
- Switching computers or phones: press **「匯出設定 JSON」 (Export Settings JSON)** on the original device, then **「匯入設定 JSON」 (Import Settings JSON)** on the new one.
- Settings may be lost when using incognito mode, clearing browser data, or when browser storage runs out — export JSON backups regularly for important progress.

---

## 8. FAQ

**Q: Do I need to be online?**
No. `index.html` references no external files — it works even in airplane mode.

**Q: Will my files be uploaded?**
No. All computation happens locally in the browser; there is no backend server.

**Q: Why do some files show "未計算雜湊" (Hash Not Calculated)?**
Files over 200 MB skip hashing (to avoid freezing); files without read permission may also fail. This does not affect the checklist or categorisation.

**Q: Why can't the tool read a file's full path (e.g. /Users/xxx/Documents/…)?**
For security reasons, browsers only provide filenames and relative paths. That is a protection for your computer, not a tool defect.

**Q: Can I use it on a phone?**
Yes, the interface is tuned for mobile. But "選擇整個資料夾" (Choose Folder) support is weaker on phones; do the main organising on a computer.

**Q: Can the same file be submitted to two schools?**
Yes, but first confirm each school's prospectus allows identical content (some schools require versions not to be identical). The tool flags files with identical content in the "內容重複提醒" (Duplicate Content Reminder) so you can verify.

**Q: Will pressing "清空全部資料" (Clear All Data) delete my files?**
No. It only clears the tool's records in the browser; files on your computer are completely unaffected. (Text typed in the manuscript paper is also cleared — copy it out first if needed.)

**Q: The manuscript font doesn't look like handwriting?**
Font preview uses fonts **already installed** on your computer; if the corresponding font is missing it falls back to the system default Chinese font (no garbled text, no blanks). The manuscript paper only aligns the grid for you — the handwriting is yours.

**Q: After switching to English, will my existing item names become English?**
No. Names **you entered yourself** — school names, departments, item names, notes — stay as they are; only the tool's fixed interface text and exported checklist column headers switch languages.

**Q: Printing the manuscript paper printed the whole website?**
Press the **「列印」 (Print)** button from inside the manuscript-paper window directly (don't use the browser menu's print) — that way only the manuscript paper is printed.

---

## 9. File List

| File | Description |
|---|---|
| `index.html` | The tool itself (single file, pure frontend, no install, opens offline) |
| `使用說明.md` | This user guide |
| `範例設定_四包.json` | Sample settings for four schools (清大 2301／交大 603／NVIDIA／Google), loadable via "匯入設定 JSON" (Import Settings JSON) |
| `範例設定_四包_操作說明.md` | Walkthrough for the sample settings above (which item maps to which document) |

---

*This tool is a pure local static web page — no tracking, no ads, and no uploads.*
