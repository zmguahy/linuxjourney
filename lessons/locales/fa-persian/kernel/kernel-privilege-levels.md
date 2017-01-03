# سطوح دسترسی

## محتویات درس

چند درس آینده بیشتر جنبه‌ی نظری دارد در نتیجه اگر به دنبال دروس عملی می‌گردید، شاید بد نباشد که بی‌خیال این درس‌ها شوید.

چرا ما لایه‌های انتزاعی مختلفی برای فضای کاربری و کرنل داریم؟ چرا هر دوی این‌ها را در یک لایه‌ی واحد نداریم؟ دلیل بسیار به جایی برای جدا بودن این دو لایه وجود دارد. این دو لایه در مُدهای مختلفی عمل می‌کنند. مثلاً کرنل در مد هسته و فضای کاربری در مد کاربر فعالیت می‌کند.

در مد کرنل، کرنل به تمام سخت‌افزار دسترسی دارد و همه چیز را کنترل می‌کند. در مد فضای کاربر، مقدار بسیار جزئی از پردازنده و حافظه‌ی امن در دسترس قرار دارد. در اصل وقتی ما قرار است کاری که با سخت‌افزار در ارتباط است را انجام دهیم مانند اینکه اطلاعات را از روی دیسک بخوانیم، یا بر روی دیسک بنویسیم، شبکه را کنترل کنیم و غیره، تمام این کارها از طریق مود کرنل صورت می‌پذیرد. چرا نیاز به این کار است؟ فرض کنید که یک دستگاهی به جاسوس‌افزار آلوده شده و شما نمی‌خواهید که این جاسوس‌افزار به سخت‌افزار سیستم شما دسترسی داشته باشد. اگه این مدها جدا نبود، این جاسوس‌افزار می‌توانست به کلیه‌ی اطلاعات شما، وب‌کم و غیره دسترسی داشته باشد که خب چیزی نیست که شما دوست داشته باشید.

این مدهای مختلف، سطوح دسترسی خوانده می‌شوند (و الحق که به درستی برای سطوحی از دسترسی که شما دارید نامگذاری شده‌اند) و اغلب به آن‌ها حلقه‌های حفظ امنیت گفته می‌شود. برای اینکه تصویر ساده‌تر از موضوع را برایتان به نمایش بگذارم اجازه دهید اینگونه مطلب رو بازگو کنم. فرض کنیم بریتنی اسپیرز در کلوپی در شهر شماست. بریتنی توسط دوستدارانِ همیشه همراهش محافظت می‌شود. بعد از آن توسط بادیگاردهای شخصی‌اش محافظت می‌شود و بعد از آن توسط بانسرهای کلوپ. حالا اگر بخواهید که یک امضا از او بگیرید اوضاع سخت می‌شود چرا که بریتنی به سختی در حال محافظت شدن است. اول باید از سد طرفداران همیشه همراهش رد شوید، سپس بادیگاردها و غیره. حلقه‌ها هم دقیقاً همینگونه کار می‌کنند. درونی‌ترین حلقه حکم بالاترین سطح دسترسی را دارد. دو سطح اصلی و یا مد در کامپیوترها با معماری x86 وجود دارد. حلقه‌ی ‎#3 دسترسی است که کاربران در آن برنامه‌ها را اجرا می‌کنند. حلقه‌ی ‎#0 دسترسی است که کرنل در آن اجرا می‌شود. حلقه‌ی شماره‌ی صفر تمام دسترسی‌های ممکن را دارد و می‌تواند هر چیزی در هر سطحی که خواست اجرا کند. حالا که می‌دانیم این سطوح دسترسی چگونه کار می‌کنند، چطور می‌توانیم چیزی بر روی سخت‌افزار بنویسیم؟ مگر نه اینکه ما همیشه در مد متفاوتی نسبت به کرنل هستیم؟

پاسخ، سیستم کال‌ها یا فراخوان‌های سیستمی هستند. سیستم‌کال‌ها یک دستور با سطح دسترسی لازم در مد کرنل را اجرا می‌کند و سیستم به مد کاربر باز می‌گردد.

## تمرین

تمرینی برای این درس وجود ندارد.

## سؤال آزمون

کدام شماره‌ی حلقه بالاترین سطح دسترسی را دارد؟

## پاسخ آزمون

0