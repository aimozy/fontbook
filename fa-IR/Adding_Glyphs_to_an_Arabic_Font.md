---
published: true
layout: bookpage_fa-IR
weight: 78
section: Workflow
title: افزودن گلیف‌ها به فونت عربی
---

## پیشگفتار

در برخی موارد، یک فونت ممکن است فاقد گلیفی باشد که برای استفاده در برنامهٔ شما حیاتی است.
فونت‌های عربی در اینجا مسائل خاصی را ایجاد می‌کنند زیرا شکل گلیف‌ها نه تنها وابسته به جایگاه‌شان در یک کلمه، بلکه وابسته به خصوصیاتی آن کلمه است.
در نتیجه، در سلسله حروف بی‌معنایی مثل *بباب* حرف *ب* بسته به این که در ابتدا، وسط و یا انتهای کلمه آماده باشد سه شکل مختلف به خود می‌گیرد.
با این حال، در سلسله حروف بی‌معنایی مثل *دداد*، حرف *دال* فارغ از این که کجا ظاهر شود، فقط یک شکل دارد.

فونت‌های تحت پروانه‌های آزاد (مثل
[GPL](http://gnu.org/copyleft/gpl.html)
یا
[OFL](http://scripts.sil.org/OFL-FAQ_web)
) به کاربر اجازهٔ ویرایش می‌دهند.
اگر فونتی را برای استفاده انتخاب کرده‌اید که تحت چنین پروانه‌هایی است و بخواهید آن را بازتوزیع کنید، می‌باست توضیحات حق تکثیر پدیدآور(ان) پیشین و اطلاعات پروانه‌شان را حفظ کنید؛ البته می‌توانید یادداشتی در انتهای توضیحات حق تکثیر بگذارید که مشارکت شما را پوشش دهد.

<img src="images/beh_dal.png" />

این فصل، مبحث افزودن گلیف به یک فونت عربی را پوشش می‌دند.
فونتی که استفاده می‌کنیم
[Graph](http://openfontlibrary.org/en/font/graph)
است و گلیفی که به آن اضافه خواهیم کرد، گلیف *پ* یا *peh* با شناسهٔ یونیکد U+067E است که در خود زبان عربی کاربرد ندارد اما در برخی زبان‌های دیگر (مثل فارسی) که از خط عربی استفاده می‌کنند استفاده می‌شود.
(برای دریافت فهرست کامل گلیف‌های موجود برای خط عربی
[جدول‌های یونیکد](http://www.unicode.org/charts)
را ببینید.)

<img src="images/peh.png" />

## ساختن یک نسخهٔ قابل استفاده از فونت

فونت را از وبگاه آن دریافت و از حالت فشرده خارج کنید.
فونت‌فورج را اجرا و فونت را وارد آن کنید.
پروژه را به عنوان یک پروندهٔ *sfd* ذخیره کنید.
بد نیست که نام پروژه با چیزی مثل **GraphNew.sfd** تغییر دهید.

## تغییر نام فونت

### چرا باید نام فونت را تغییر داد؟

اگر نام فونت را تغییر ندهید، فونت تغییر یافتهٔ شما، مجزا از فونت اصلی روی دستگاه‌تان نصب نمی‌شود و لازم است که فونت اصلی را حذف و سپس فونت‌تان را نصب کنید.
همچنین اگر بخواهید فونت‌تان را منتشر کنید، منطقی است که نامش را تغییر دهید.
چنانچه پدیدآورندهٔ اصلی نام فونت را تحت ساز و کاری به نام «نام فونت رزرو شده» یا RFN رزرو کرده باشد، نام اصلی فونت تنها توسط نسخه‌های پدیدآورندهٔ اصلی آن فونت قابل استفاده است.

### تغییر داده‌های فونت

به `Element > Font Info` رفته و در قسمت *PS Names*، مقادیر مربوط به نام فونت (Fontname)، نام خانواده (Family Name)، و نام مناسب انسان‌ها (Name For Humans) را به **GraphNew** تغییر دهید.

<img src="images/font_rename.png" />

اگر تمایل داشته باشید می‌توانید پیامی مثل «Additional glyphs added by» را در انتهای بخش *Copyright* اضافه کنید.

در بخش *TTF Names* نام‌های مربوط به *Family* و *Fullname* از مقادیر مربوط در بخش *PS Names* برداشته می‌شوند.
این مقادیر را نمی‌توانید مستقیما ویرایش کنید.
مقادیر مربوط به *Preferred Family* و *Compatible Full* را به **GraphNew** تغییر دهید.
اکنون، این تغییر نام‌ها به شما امکان می‌دهند که اگر بخواهید، فونت‌تان را در کنار فونت اصلی نصب کنید.

اگر تمایل داشته باشید نام‌تان در فهرست طراحان فونت آورده شود، می‌توانید پیامی مثل «Additional glyphs added by» را بعد از متنی که در بخش *Designer* است اضافه کنید.

دکمهٔ Ok را کلیک کنید تا تغییرات‌تان ذخیره شود.
پیامی درباره تولید یک شناسهٔ یکتا یا UniqueID (XUID) دریافت خواهید کرد. دکمهٔ Change را کلیک کنید تا شناسهٔ جدید ایجاد شود.


## افزودن گلیف برای شکل جدای «پ»

به بخش عربی جدول فونت بروید: به `View > Go to` رفته و از فهرست پایین‌افتادنی، گزینهٔ **Arabic** را انتخاب و نهایتا روی Ok کلیک کنید.

با کلیک کردن روی یک سلول در جدول فونت، نام و شمارهٔ یونیکد آن سلول به رنگ آبی در نوار بالای برنامه نمایش داده می‌شود.
به موقعیت ۱۶۶۲ بروید که در بخش آبی رنگ به صورت زیر نمایش داده می‌شود:

*‎1662 (0x67e) U+067E "uni067E" ARABIC LETTER PEH*

سلول زیر گلیف مرجع دارای یک X خاکستری است.
معنی این علامت این است که فونت هنوز شامل این گلیف نمی‌شود.

<img src="images/peh_blank.png" />

با رونوشت گرفتن از «ب» (U+0628) و جایگزین کردن تک نقطهٔ آن با سه‌نقطه، گلیف «پ» را می‌سازیم.

روی «ب» (در موقعیت ۱۵۷۶) کلیک کنید. سپس کلیک راست کرده و با **Copy** از آن رونوشت بگیرید.
سپس روی سلول «پ» کلیک کرده و با **Paste** گلیف رونوشت‌گرفته را جای‌گذاری کنید.
اکنون که «ب» روی «پ» رونوشت گرفته شده، به کار بعدی یعنی تغییر نقطه می‌پردازیم.

<img src="images/peh_with_beh.png" />

گلیفی با سه نقطه پیدا کنید.
«شین» (در موقعیت ۱۵۸۸ و با یونیکد U+0634) گزینهٔ خوبی است.
روی سلول دو بار کلیک کنید تا پنجرهٔ طراحی گلیف باز شود. دکمهٔ <kbd>V</kbd> را بفشارید تا مطمئن شوید که ابزار اشاره‌گر (با سر پیکان‌دار) در نوار ابزار فعال باشد.
سپس دکمهٔ <kbd>Z</kbd> را بفشارید تا نمای بزرگ‌تری از گلیف در اختیارتان قرار بگیرد.

نقاط را کلیک کرده و بکشید تا سه نقطهٔ بالای شین رنگ‌شان از صورتی به بژ تغییر کند.
اگر تصادفاً گره‌ای را اضافه‌تر انتخاب کردید یا گره‌ای از قلم افتاد، با کمک <kbd>Shift</kbd> و کلیک کردن، گره‌ها را اضافه یا کم کنید.
با فشردن <kbd>Ctrl</kbd> + <kbd>C</kbd> از آن‌ها یک رونوشت تهیه کنید.

<img src="images/sheen_dots.png" />

به جدول فونت برگردید و روی سلول «پ» دو بار کلیک کنید تا در زبانهٔ جدیدی کنار «شین» برای «پ» باز شود، 

با روش مشابهی که بالا گفته شد، گره‌های مربوط به نقطه را انتخاب و با فشردن <kbd>Delete</kbd> آن را پاک کنید.
با کمک <kbd>Ctrl</kbd> + <kbd>V</kbd>، سه نقطه‌ای را که از شین رونوشت گرفته بودید به «پ» اضافه کنید.
این کار باعث می‌شود که آن سه نقطه، بالای بدنهٔ اصلی «پ» قرار بگیرند.

<img src="images/peh_dots1.png" />

معکوس کردن نقطه‌ها: در حالی که گره‌های آن سه نقطه همچنان در حالت انتخاب قرار دارند، ابزار معکوس‌سازی (flip tool) را از نوارابزار انتخاب کنید.
همچنین می‌توانید وسط نقاط کلیک راست کرده و از فهرست نمایش داده شده، **Flip the selection** را انتخاب کنید.
روی یکی از گره‌های نقطه کلیک کرده و به آرامی آن را با موشواره به سمت راست یا چپ بکشید.

<img src="images/peh_dots2.png" />

جابجایی نقطه‌های معکوس‌شده:
دکمهٔ <kbd>V</kbd> را بفشارید تا ابزار اشاره‌گر مجددا انتخاب شود. روی یکی از گره‌ها کلیک کنید و آن‌ها را به زیر زیر بدنهٔ گلیف بکشید.
نقاط را به لحاظ افقی در وسط و بالاتر از نشان *ArabicBelow* قرار دهید.

<img src="images/peh_dots3.png" />

پنجرهٔ طراحی گلیف را ببندید.
اکنون باید یک گلیف برای «پ» در جدول فونت وجود داشته باشد.
فونت تغییر یافته را ذخیره کنید.

<img src="images/peh_new.png" />

## افزودن گلیف برای شکل متصل «پ»

چیزی که تا اینجا ساخته‌ایم، صرفا شکل جدا و منفصل این گلیف بوده است.
اگر بخواهید از این فونت استفاده کنید متوجه خواهید شد که شکل‌های آغازین، میانه و پایانی این حرف در دسترس نیستند.
این شکل‌ها باید جداگانه ساخته شوند.

> «این شکل‌ها به صورت گلیف‌های غیرکدگذاری‌شده (گلیف‌هایی که بنا به قرارداد، کدگذاری‌شان در فونت‌فورج منفی ۱ است) ساخته می‌شوند. شیار یا سلولی پیش‌تعریف‌شده‌ای برای آن‌ها وجود ندارد.» (خالد حسنی)

<p class="note">
<strong>تصحیح مترجم</strong>
<br/>
صحبت مطرح شده در نقل قول، اگر در زمان مطرح شدن درست بوده باشد، در حال حاضر اشتباه است. حرف پ (شامل هر چهار شکل آن) دارای جایگاه اختصاصی در جدول یونیکد (از <code>U+fb56</code> تا <code>U+fb59</code>) است. بنابراین، نیازی به ساختن شیارهای کدگذاری‌نشده برای سایر شکل‌های این حرف وجود ندارد.
</p>

به `Encoding > Add Encoding Slots` رفته و تعداد گلیف‌هایی را که می‌خواهید بسازید را وارد کنید؛ در این مورد، ۳.
فونت‌فورج به تعداد وارد شده، گلیف به پایین‌ترین قسمت جدول فونت اضافه می‌کند.
سه سلول آخر، به عنوان گلیف ارجاعی، دارای یک علامت سوال هستند.
در همین سه سلول است که گلیف‌های کدگذاری‌نشده را با تکرار مراحل پیش‌تر گفته شده، اضافه خواهید کرد.

<img src="images/peh_slots.png" />

<p class="note">
توجه داشته باشید که اگر در حالی که جدول فونت هنوز فعال است به اشتباه شروع به نوشتن کنید، به بخش اروپایی در بالای جدول منتقل خواهید شد.
برای بازگشت به پایین جدول به <code>View > Go to</code> رفته و گزینهٔ

<strong>Not a Unicode Character</strong>
را انتخاب و سپس روی Ok کلیک کنید.
</p>

### ساختن شکل پایانی

در جدول فونت قدری به پایین پیمایش کنید تا به مجموعه گلیف‌های عربی در موقعیت ۶۵۱۵۲ (`U+FE80`) به بعد برسید.
در موقعیت ۶۵۱۶۸ (`U+FE90`) گلیف «ب» پایانی یا *behfinal* را می‌بینید.
روی آن کلید کرده و با <kbd>Ctrl</kbd> + <kbd>C</kbd> از آن رونوشت تهیه کنید.
اکنون به انتهای جدول بروید، سومین سلول از آخر را (در موقعیت ۶۵۵۳۷) انتخاب و با <kbd>Ctrl</kbd> + <kbd>V</kbd>، گلیف *behfinal* رونوشت‌شده را در آن جای‌گذاری کنید.

<img src="images/beh_forms.png" />

روی سلول کلیک راست کرده و Glyph Info را انتخاب کنید.
قرارداد نام‌گذاری این است که شمارهٔ گلیف منفصل را نوشته و پسوندی برای شکل آن به انتهایش اضافه کنید.
بنابراین، نام گلیف را به `uni067E.fina` تغییر دهید.
علامت سوالی که پیش‌تر نمایش داده می‌شد جای خود را به *peh* خواهد داد.

<img src="images/peh_final.png" />

آوردن سه نقطه: روی «شین» (`U+FEB5`) دو بار کلیک کرده و از پنجرهٔ طراحی گلیف، از سه نقطهٔ آن رونوشت بگیرید.
به گلیف «پ» پایانی یا *pehfinal* رفته، تک نقطه را حذف، سه نقطهٔ رونوشت‌شده را وارد و معکوس کرده و در جای مناسب قرار دهید.

### ساختن شکل ابتدایی و میانه

فرایند بالا را تکرار کرده و گلیف‌های «پ» ابتدایی و میانه به ترتیب با نام‌های `uni067E.init` و `uni067E.medi` بسازید.

<img src="images/peh_forms.png" />

تغییرات خود را ذخیره کنید.

## افزودن مراجعات (Lookups)

شکل منفصل (isolated) بایستی به شکل‌های ابتدایی، میانه و پایانی نگاشت شود (یا پیوند داده شود).

به `Element > Font Info > Lookups` بروید.

روی `+` کنار *'init' Initial Forms in Arabic lookup 2* کلیک کنید.
با این کار، زیرفهرستی با این نام باز می‌شود.
روی این زیرفهرست کلیک کنید.
دکمهٔ Edit Data در نوار کناری فعال می‌شود.
روی آن کلیک کنید.

<img src="images/peh_lookups1.png" />

در پنجرهٔ **زیرجدول مراجعه** (Lookup Subtable) که ظاهر می‌شود اطمینان حاصل کنید که دکمهٔ Unicode در وضعیت انتخاب قرار داشته باشد.
به انتهای فهرست نویسه‌ها بروید.
در خانهٔ خالی‌ای که کنار Default Using Suffix قرار دارد رفته و پسوند مرتبط با وارد کنید (در این مورد: init)
و سپس دکمهٔ Default Using Suffix را بفشارید.

نگاشت جدیدی از `uni067E` (شکل منفصل «پ») به `uni067E.init` (شکل ابتدایی «پ») به فهرست نویسه‌ها اضافه می‌شود.
روی Ok کلیک کنید.

<img src="images/peh_lookups2.png" />

همین کار را در زیرفهرست *'medi' Medial Forms in Arabic lookup 2* با پسوند medi و سپس *'fina' Terminal Forms in Arabic lookup 2* با پسوند fina انجام دهید.

مجددا روی Ok کلیک کنید تا پنجره بسته شود.
نهایتا، جدول فونت را ذخیره کنید.

توجه داشته باشید که به نظر می‌رسد که Default Using Suffix تنها روی گلیف‌های موجود در بلوک Unicode 06 (*Arabic*) کار می‌کند. برای گلیف‌های Unicode 07 (*Arabic Supplement*) مثل *ain* با دو نقطه ممکن است لازم باشد به طور دستی مقادیر وارد جدول بشوند.

### تولید فونت تغییریافته

به `File > Generate Fonts` بروید.
در فهرست پایین‌افتادنی (که احتمالا PS Type 1 (Binary)) را نشان می‌دهد، TrueType را انتخاب کنید. این کار باعث می‌شود نام پرونده به شکل GraphNew.ttf درآید.

محل ذخیره فونت را انتخاب کرده و دکمهٔ **Generate** را بفشارید. در دو پنجره‌ای که بعد از این مرحله نشان داده می‌شوند، روی Yes و Generate کلیک کنید.

اکنون می‌توانید این فونت تولید شده را با روش استاندارد نصب فونت روی سیستم‌عامل‌تان نصب کنید.
اکنون، گلیف «پ» (peh) را در کنار سایر گلیف‌ها به کار برد.

<img src="images/beh_dal_peh.png" />

<p class="note">
توجه داشته باشید که اگر از فونتی در لیبره‌آفیس استفاده می‌کنید و آن فونت تغییر یابد، شما بایستی لیبره‌آفیس را بسته و دوباره باز کنید تا این تغییرات قابل مشاهده شوند.
در غیر این صورت، نرم‌افزار از همان نسخهٔ قبلی فونت استفاده می‌کند و نه نسخهٔ تغییر یافته.
</p>

با تشکر از
[خالد حُسنی](http://khaledhosny.org)
برای پیشنهاداتش در خصوص استفاده از فونت‌فورج برای ویرایش گلیف‌های عربی.

## مطالعهٔ بیشتر


* [این رشته بحث درباره auto-hinting بهبودیافتهٔ عربی](http://lists.nongnu.org/archive/html/freetype-devel/2015-08/msg00016.html) دارای نکته‌ای در خصوص رسم بخش‌های دارای هم‌پوشانی در گلیف‌های عربی است.
