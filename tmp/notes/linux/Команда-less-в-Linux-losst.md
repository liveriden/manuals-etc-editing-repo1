<article id="post-32429" class="post-32429 post type-post status-publish format-standard has-post-thumbnail hentry category-commands infinite-scroll-item" itemtype="https://schema.org/CreativeWork" itemscope="">
	<div class="inside-article">
					<header class="entry-header" aria-label="Содержимое">
				<span><span><a href="https://losst.pro/">Главная</a></span> &gt;&gt; <span><a href="https://losst.pro/commands">Команды</a></span> &gt;&gt; <span class="breadcrumb_last" aria-current="page">Команда less в Linux</span></span><h1 class="entry-title" itemprop="headline">Команда less в Linux</h1>		<div class="entry-meta">
			<span class="posted-on"> <span class="entry-date-label">Опубликовано:</span> <time class="entry-date published" datetime="2020-07-23T12:00:10+09:30" itemprop="datePublished">23 июля, 2020</time></span> <span class="byline">от <span class="author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope=""><a class="url fn n" href="https://losst.pro/author/ellado" title="Просмотр всех записей ellado" rel="author" itemprop="url"><span class="author-name" itemprop="name">ellado</span></a></span></span> , 3 комменариев,  время чтения: 6 минут 		</div>
					</header>
			
		<div class="entry-content" itemprop="text">
			<div id="extapp-report-message" style="color: gray; margin-top: 20px; margin-bottom: 20px;">Обнаружили ошибку в тексте? Сообщите мне об этом. Выделите текст с ошибкой и нажмите Ctrl+Enter.</div><p>Об утилите и команде more, которая предназначена для постраничного просмотра больших текстовых файлов, мы уже <a href="https://losst.pro/komanda-more-v-linux">писали</a>. А сегодня расскажем о более функциональной команде less — она позволяет перематывать текст не только вперёд, но и назад, осуществлять поиск в обоих направлениях, переходить сразу в конец или в начало файла.</p><div class="rath2aiD rath2aiD-1" style="margin: 8px auto; text-align: center; display: block; clear: both;">
<script async="" src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3031391294356171" crossorigin="anonymous"></script>
<!-- ArticleTop -->
<ins class="adsbygoogle" style="display:inline-block;width:336px;height:280px" data-ad-client="ca-pub-3031391294356171" data-ad-slot="3149139045"><iframe id="aswift_0" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;"><iframe id="google_ads_frame0"></iframe></iframe></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script></div>

<p>Особенность less заключается в том, что команда не считывает текст полностью, а загружает его небольшими фрагментами.<br>
<span id="more-32429"></span></p>
<br> <p>Содержание статьи</p>    <ul>
      <li data-toc-section="sintaksis-i-opcii-less" class="first">
        <a href="#sintaksis-i-opcii-less">Синтаксис и опции less</a>
      </li>
      <li data-toc-section="primery-ispolzovaniya-less">
        <a href="#primery-ispolzovaniya-less">Примеры использования less</a>
      </li>
      <li data-toc-section="vyvody" class="last">
        <a href="#vyvody">Выводы</a>
      </li>
    </ul>
<h2 id="sintaksis-i-opcii-less" data-toc-heading="true"><strong>Синтаксис и опции less</strong></h2>
<p>Запись команды less в терминале выглядит так:</p>
<p><strong><span style="color: #ff9900;">команда</span> <span style="color: #99cc00;">опции</span>&nbsp;</strong><span style="color: #3366ff;"><strong>файл</strong></span></p>
<p>Наиболее популярные опции:</p>
<ul>
<li><strong>-a</strong>, <strong>--search-skip-screen</strong> — не осуществлять поиск в тексте, который в данный момент отображен на экране;</li>
<li><strong>-bn</strong>, <strong>--buffers=n</strong> — задать размер буфера памяти;</li>
<li><strong>-c</strong>, <strong>--clear-screen</strong> — листать текст, полностью стирая содержимое экрана (построчная прокрутка работать не будет);</li>
<li><strong>-Dxcolor</strong>, <strong>--color=xcolor</strong> — задать цвет отображаемого текста;</li>
<li><strong>-E</strong>, <strong>--QUIT-AT-EOF</strong> — выйти, когда утилита достигнет конца файла;</li>
<li><strong>-e</strong>, <strong>--quit-at-eof</strong> — выйти, когда утилита второй раз достигнет конца файла;</li>
<li><strong>-F</strong>, <strong>--quit-if-one-screen</strong> — выйти, если содержимое файла помещается на одном экране;</li>
<li><strong>-f</strong>, <strong>--force</strong> — открыть специальный файл;</li>
<li><strong>-hn</strong>, <strong>--max-back-scroll=n</strong> — задать максимальное количество строк для прокрутки назад;</li>
<li><strong>-yn</strong>, <strong>--max-forw-scroll=n</strong> — задать максимальное количество строк для прокрутки вперёд;</li>
<li><strong>-i</strong>, <strong>--ignore-case</strong> — игнорировать регистр;</li>
<li><strong>-I</strong>, <strong>--IGNORE-CASE</strong> — игнорировать регистр, даже если паттерн для поиска содержит заглавные буквы;</li>
<li><strong>-jn</strong>, <strong>--jump-target=n</strong> — указать, в какой строке должна быть выведена искомая информация;</li>
<li><strong>-J, --status-column</strong> — пометить строки, соответствующие результатам поиска;</li>
<li><strong>-n</strong>, <strong>--line-numbers</strong> — не выводить номера строк;</li>
<li>-<strong>N</strong>, <strong>--LINE-NUMBERS</strong> — вывести номера строк;</li>
<li><strong>-s</strong>, <strong>--squeeze-blank-lines</strong> — заменить множество идущих подряд пустых строк одной пустой строкой;</li>
<li><strong>-w</strong>, <strong>--hilite-unread</strong> — выделить первую строку нового фрагмента текста.</li>
</ul>
<p>Во время просмотра текста утилитой можно управлять при помощи внутренних команд, набирая их на клавиатуре компьютера. Наиболее часто используемые из них:</p>
<ul>
<li><strong>h</strong>, <strong>H</strong> — справка;</li>
<li><strong>Space</strong>, <strong>Ctrl+V</strong>, <strong>f</strong>, <strong>Ctrl+F</strong> — прокрутить текст на один экран вперёд;</li>
<li><strong>Enter</strong>, <strong>Return</strong>, <strong>Ctrl+N</strong>, <strong>e</strong>, <strong>Ctrl+E</strong>, <strong>j</strong>, <strong>Ctrl+J</strong> — прокрутить текст на n строк вперед, по умолчанию n=1;</li>
<li><strong>y</strong>, <strong>Ctrl+Y</strong>, <strong>Ctrl+P</strong>, <strong>k</strong>, <strong>Ctrl+K</strong> — прокрутить текст на n строк назад, по умолчанию n=1;</li>
<li><strong>Ctrl+</strong><strong>→</strong> — прокрутить текст по горизонтали в конец строки;</li>
<li><strong>Ctrl+</strong><strong>←</strong> — прокрутить текст по горизонтали в начало строки;</li>
<li><strong>:d</strong> — удалить текущий файл из списка файлов;</li>
<li><strong>Ctrl+G, :f</strong> — вывести основную информацию о файле;</li>
<li><strong>q, Q, :q, :Q, ZZ</strong> — выход.</li>
</ul>
<p>Перечень всех опций и внутренних команд можно просмотреть в терминале, выполнив команду</p>
<p><code class="user">man less</code></p>
<h2 id="primery-ispolzovaniya-less" data-toc-heading="true"><strong>Примеры использования less</strong></h2>
<div class="rath2aiD rath2aiD-2" style="margin: 8px auto; text-align: center; display: block; clear: both;">

<div class="ai-dynamic" countries="RU, BY, NL" country-list="W" data-code=""><iframe data-aa="2155561" src="//ad.a-ads.com/2155561?size=336x280" style="width:336px; height:280px; border:0px; padding:0; overflow:hidden; background-color: transparent;" sz2qbeo2l=""></iframe>
</div>
</div>
<div class="rath2aiD rath2aiD-7" style="margin: 8px auto; text-align: center; display: none; clear: both;">

<div class="ai-dynamic" countries="RU, BY, NL" country-list="B" data-code="PHNjcmlwdCBhc3luYyBzcmM9Imh0dHBzOi8vcGFnZWFkMi5nb29nbGVzeW5kaWNhdGlvbi5jb20vcGFnZWFkL2pzL2Fkc2J5Z29vZ2xlLmpzP2NsaWVudD1jYS1wdWItMzAzMTM5MTI5NDM1NjE3MSIKICAgICBjcm9zc29yaWdpbj0iYW5vbnltb3VzIj48L3NjcmlwdD4KPGlucyBjbGFzcz0iYWRzYnlnb29nbGUiCiAgICAgc3R5bGU9ImRpc3BsYXk6YmxvY2s7IHRleHQtYWxpZ246Y2VudGVyOyIKICAgICBkYXRhLWFkLWxheW91dD0iaW4tYXJ0aWNsZSIKICAgICBkYXRhLWFkLWZvcm1hdD0iZmx1aWQiCiAgICAgZGF0YS1hZC1jbGllbnQ9ImNhLXB1Yi0zMDMxMzkxMjk0MzU2MTcxIgogICAgIGRhdGEtYWQtc2xvdD0iNzgzNzU0MTA3NSI+PC9pbnM+CjxzY3JpcHQ+CiAgICAgKGFkc2J5Z29vZ2xlID0gd2luZG93LmFkc2J5Z29vZ2xlIHx8IFtdKS5wdXNoKHt9KTsKPC9zY3JpcHQ+" style="display: none;"></div>
</div>
<p>Использование опций не является обязательным. Открыть файл можно, выполнив следующую команду:</p>
<p><code class="user">less filename.txt</code></p>
<p>Командная строка исчезнет, а в окне терминала откроется указанный вами документ. После этого его можно читать, пользуясь для прокручивания строк вперед и назад клавишами <strong>Enter</strong> и <strong>y</strong> либо другими.</p>
<p>Внизу окна вы увидите поле с мигающим курсором — здесь можно напечатать какую-либо внутреннюю команду, например, задать утилите паттерн поиска.</p>
<p><a href="https://losst.pro/wp-content/uploads/2020/07/1.png"><img fetchpriority="high" decoding="async" class="aligncenter size-large wp-image-32430" src="https://losst.pro/wp-content/uploads/2020/07/1-1024x576.png" alt="" width="806" height="453" srcset="https://losst.pro/wp-content/uploads/2020/07/1-1024x576.png 1024w, https://losst.pro/wp-content/uploads/2020/07/1-1536x864.png 1536w, https://losst.pro/wp-content/uploads/2020/07/1.png 1920w" sizes="(max-width: 806px) 100vw, 806px"></a></p>
<p>Опции нужны для того, чтобы оптимизировать отображение текста и сделать работу с утилитой более удобной. К примеру, в текстах часто встречаются множественные пустые строки. Они «съедают» место на экране, не принося никакой пользы. Поэтому к команде less стоит всегда добавлять опцию<strong> -s</strong> или <strong>--squeeze-blank-lines</strong> — она удаляет лишние пустые строки.</p>
<p><code class="user">less -s textfile.txt</code></p>
<p>Сравните как выглядит один и тот же текст с использованием опции -s (слева) и без неё (справа).</p>
<p><a href="https://losst.pro/wp-content/uploads/2020/07/2.png"><img decoding="async" class="aligncenter size-large wp-image-32431" src="https://losst.pro/wp-content/uploads/2020/07/2-1024x576.png" alt="" width="806" height="453" srcset="https://losst.pro/wp-content/uploads/2020/07/2-1024x576.png 1024w, https://losst.pro/wp-content/uploads/2020/07/2-1536x864.png 1536w, https://losst.pro/wp-content/uploads/2020/07/2.png 1920w" sizes="(max-width: 806px) 100vw, 806px"></a></p>
<p>Впрочем, утилиту less зачастую используют не для чтения текста, а для поиска определенных участков в больших документах. Если вам нужно найти то или иное слово, напечатайте в поле с мигающим курсором <strong>/текст</strong> (для поиска вниз по тексту) или <strong>?текст</strong> (чтобы выполнить поиск less вверх по тексту) и нажмите Enter. При необходимости используйте стандартные паттерны. Все участки текста, которые соответствуют заданным условиям поиска, будут подсвечены контрастным цветом.</p>
<p><a href="https://losst.pro/wp-content/uploads/2020/07/3.png"><img decoding="async" class="aligncenter size-large wp-image-32432" src="https://losst.pro/wp-content/uploads/2020/07/3-1024x576.png" alt="" width="806" height="453" srcset="https://losst.pro/wp-content/uploads/2020/07/3-1024x576.png 1024w, https://losst.pro/wp-content/uploads/2020/07/3-1536x864.png 1536w, https://losst.pro/wp-content/uploads/2020/07/3.png 1920w" sizes="(max-width: 806px) 100vw, 806px"></a></p>
<p>Если вас интересует как выйти из less, то для выхода из утилиты и возвращения к командной строке терминала нажмите <strong>q</strong>, <strong>ZZ</strong> или выполните другую команду, сигнализирующую о завершении работы.</p><div class="rath2aiD rath2aiD-4" style="margin: 8px 0; clear: both;">
<script async="" src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3031391294356171" crossorigin="anonymous"></script>
<ins class="adsbygoogle" style="display:block; text-align:center;" data-ad-layout="in-article" data-ad-format="fluid" data-ad-client="ca-pub-3031391294356171" data-ad-slot="6033613970"><iframe id="aswift_1" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;"><iframe id="google_ads_frame1"></iframe></iframe></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script></div>

<p>Следует заметить, что утилита less предназначена только для просмотра документов. Она не позволяет вносить в текст правки, форматировать или пересохранять его.</p>
<h2 id="vyvody" data-toc-heading="true"><strong>Выводы</strong></h2>
<p>Команда less в Linux пригодится для просмотра по-настоящему больших текстовых файлов, с которыми затруднительно работать в текстовых редакторах вроде vim или с помощью утилит, загружающих весь документ сразу. Если какие-то нюансы управления утилитой less остались вам непонятны, оставьте свой вопрос в комментариях и более опытные пользователи помогут решить проблему.</p>
<div id="extapp-feedback-container" style="position: sticky; bottom: 0px;">
<div class="sm-helpful-popup">
    <div class="sm-question-popup" id="sm-question-popup">
        <span class="close" id="sm-question-close-button">×</span>
        <span class="sm-question-label">Была ли эта информация полезной для вас?</span>
        <span class="sm-question-answers">
            <button class="sm-question-answer" id="sm-question-yes-answer" data-answer="yes">Да</button>
            <button class="sm-question-answer" id="sm-question-no-answer" data-answer="no">Нет</button>
        </span>
    </div>
    <div id="sm-extended-feedback-container"></div>
</div>
</div><div class="yarpp yarpp-related yarpp-related-website yarpp-template-thumbnails">
<!-- YARPP Thumbnails -->
<h3>Похожие записи</h3>
<div class="yarpp-thumbnails-horizontal">
<a class="yarpp-thumbnail" rel="norewrite" href="https://losst.pro/komanda-dd-linux" title="Команда dd Linux">
<img width="150" height="150" src="https://losst.pro/wp-content/uploads/2017/03/Snimok-ekrana-iz-2017-03-24-07-06-07-150x150.png" class="attachment-thumbnail size-thumbnail wp-post-image" alt="" data-pin-nopin="true" srcset="https://losst.pro/wp-content/uploads/2017/03/Snimok-ekrana-iz-2017-03-24-07-06-07-150x150.png 150w, https://losst.pro/wp-content/uploads/2017/03/Snimok-ekrana-iz-2017-03-24-07-06-07-100x100.png 100w, https://losst.pro/wp-content/uploads/2017/03/Snimok-ekrana-iz-2017-03-24-07-06-07-65x65.png 65w" sizes="(max-width: 150px) 100vw, 150px"><span class="yarpp-thumbnail-title">Команда dd Linux</span></a>
<a class="yarpp-thumbnail" rel="norewrite" href="https://losst.pro/komanda-tar-v-linux" title="Команда tar в Linux">
<img width="150" height="150" src="https://losst.pro/wp-content/uploads/2018/04/archive-150x150.png" class="attachment-thumbnail size-thumbnail wp-post-image" alt="Создание архива tar" data-pin-nopin="true" srcset="https://losst.pro/wp-content/uploads/2018/04/archive-150x150.png 150w, https://losst.pro/wp-content/uploads/2018/04/archive-115x115.png 115w" sizes="(max-width: 150px) 100vw, 150px"><span class="yarpp-thumbnail-title">Команда tar в Linux</span></a>
<a class="yarpp-thumbnail" rel="norewrite" href="https://losst.pro/komanda-sed-linux" title="Команда sed Linux">
<img width="150" height="150" src="https://losst.pro/wp-content/uploads/2019/08/Snimok-ekrana-ot-2019-08-18-18-57-31-150x150.png" class="attachment-thumbnail size-thumbnail wp-post-image" alt="" data-pin-nopin="true"><span class="yarpp-thumbnail-title">Команда sed Linux</span></a>
<a class="yarpp-thumbnail" rel="norewrite" href="https://losst.pro/komanda-su-v-linux" title="Команда su в Linux">
<img width="150" height="150" src="https://losst.pro/wp-content/uploads/2020/02/komanda-su-v-linux-5-150x150.jpg" class="attachment-thumbnail size-thumbnail wp-post-image" alt="" data-pin-nopin="true"><span class="yarpp-thumbnail-title">Команда su в Linux</span></a>
</div>
</div>
<div class="rath2aiD rath2aiD-3" style="margin: 8px auto; text-align: center; display: none; clear: both;">

<div class="ai-dynamic" countries="BY, NL, RU" country-list="B" data-code="PHNjcmlwdCBhc3luYyBzcmM9Ii8vcGFnZWFkMi5nb29nbGVzeW5kaWNhdGlvbi5jb20vcGFnZWFkL2pzL2Fkc2J5Z29vZ2xlLmpzIj48L3NjcmlwdD4KPCEtLSDQoNC10LrQvtC80LXQvdC00L7QstCw0L3QvdGL0Lkg0LrQvtC90YLQtdC90YIgLS0+CjxpbnMgY2xhc3M9ImFkc2J5Z29vZ2xlIgogICAgIHN0eWxlPSJkaXNwbGF5OmJsb2NrIgogICAgIGRhdGEtYWQtY2xpZW50PSJjYS1wdWItMzAzMTM5MTI5NDM1NjE3MSIKICAgICBkYXRhLWFkLXNsb3Q9IjE0NTQxNzg2NDgiCiAgICAgZGF0YS1hZC1mb3JtYXQ9ImF1dG9yZWxheGVkIj48L2lucz4KPHNjcmlwdD4KKGFkc2J5Z29vZ2xlID0gd2luZG93LmFkc2J5Z29vZ2xlIHx8IFtdKS5wdXNoKHt9KTsKPC9zY3JpcHQ+Cg==" style="display: none;"></div>
</div>
<!-- AI CONTENT END 1 -->
		</div>

		                <div class="postrating" style="margin-top: 20px;">
                    <h2>Оцените статью</h2>
                    <div id="post-ratings-32429" class="post-ratings" data-nonce="8790f95f08"><img id="rating_32429_1" src="https://losst.pro/wp-content/plugins/wp-postratings/images/stars_crystal/rating_on.gif" alt="Звёзд: 1" title="Звёзд: 1" onmouseover="current_rating(32429, 1, 'Звёзд: 1');" onmouseout="ratings_off(4.2, 0, 0);" onclick="rate_post();" onkeypress="rate_post();" style="cursor: pointer; border: 0px;"><img id="rating_32429_2" src="https://losst.pro/wp-content/plugins/wp-postratings/images/stars_crystal/rating_on.gif" alt="Звёзд: 2" title="Звёзд: 2" onmouseover="current_rating(32429, 2, 'Звёзд: 2');" onmouseout="ratings_off(4.2, 0, 0);" onclick="rate_post();" onkeypress="rate_post();" style="cursor: pointer; border: 0px;"><img id="rating_32429_3" src="https://losst.pro/wp-content/plugins/wp-postratings/images/stars_crystal/rating_on.gif" alt="Звёзд: 3" title="Звёзд: 3" onmouseover="current_rating(32429, 3, 'Звёзд: 3');" onmouseout="ratings_off(4.2, 0, 0);" onclick="rate_post();" onkeypress="rate_post();" style="cursor: pointer; border: 0px;"><img id="rating_32429_4" src="https://losst.pro/wp-content/plugins/wp-postratings/images/stars_crystal/rating_on.gif" alt="Звёзд: 4" title="Звёзд: 4" onmouseover="current_rating(32429, 4, 'Звёзд: 4');" onmouseout="ratings_off(4.2, 0, 0);" onclick="rate_post();" onkeypress="rate_post();" style="cursor: pointer; border: 0px;"><img id="rating_32429_5" src="https://losst.pro/wp-content/plugins/wp-postratings/images/stars_crystal/rating_off.gif" alt="Звёзд: 5" title="Звёзд: 5" onmouseover="current_rating(32429, 5, 'Звёзд: 5');" onmouseout="ratings_off(4.2, 0, 0);" onclick="rate_post();" onkeypress="rate_post();" style="cursor: pointer; border: 0px;"> (<strong>13</strong> оценок, среднее: <strong>4,23</strong> из 5)<br><span class="post-ratings-text" id="ratings_32429_text"></span></div><div id="post-ratings-32429-loading" class="post-ratings-loading"><img src="https://losst.pro/wp-content/plugins/wp-postratings/images/loading.gif" width="16" height="16" class="post-ratings-image"> Загрузка...</div>                </div>
                                    <div style="margin-top: 30px">
                        <a target="_blank" rel="license" href="https://losst.pro/content-policy">
                            <img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png"></a>
                        <br>
                        Статья распространяется под лицензией Creative Commons ShareAlike 4.0 при копировании материала ссылка на источник обязательна                        .
                    </div>
                		<footer class="entry-meta" aria-label="Entry meta">
			<span class="cat-links"><span class="gp-icon icon-categories"><svg viewBox="0 0 512 512" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em"><path d="M0 112c0-26.51 21.49-48 48-48h110.014a48 48 0 0143.592 27.907l12.349 26.791A16 16 0 00228.486 128H464c26.51 0 48 21.49 48 48v224c0 26.51-21.49 48-48 48H48c-26.51 0-48-21.49-48-48V112z"></path></svg></span><span class="screen-reader-text">Рубрики </span><a href="https://losst.pro/commands" rel="category tag">Команды</a></span> 		<nav id="nav-below" class="post-navigation" aria-label="Posts" style="display: none;">
			<div class="nav-previous"><span class="gp-icon icon-arrow-left"><svg viewBox="0 0 192 512" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" fill-rule="evenodd" clip-rule="evenodd" stroke-linejoin="round" stroke-miterlimit="1.414"><path d="M178.425 138.212c0 2.265-1.133 4.813-2.832 6.512L64.276 256.001l111.317 111.277c1.7 1.7 2.832 4.247 2.832 6.513 0 2.265-1.133 4.813-2.832 6.512L161.43 394.46c-1.7 1.7-4.249 2.832-6.514 2.832-2.266 0-4.816-1.133-6.515-2.832L16.407 262.514c-1.699-1.7-2.832-4.248-2.832-6.513 0-2.265 1.133-4.813 2.832-6.512l131.994-131.947c1.7-1.699 4.249-2.831 6.515-2.831 2.265 0 4.815 1.132 6.514 2.831l14.163 14.157c1.7 1.7 2.832 3.965 2.832 6.513z" fill-rule="nonzero"></path></svg></span><span class="prev"><a href="https://losst.pro/kak-polzovatsya-shotcut" rel="prev">Как пользоваться Shotcut</a></span></div><div class="nav-next"><span class="gp-icon icon-arrow-right"><svg viewBox="0 0 192 512" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" fill-rule="evenodd" clip-rule="evenodd" stroke-linejoin="round" stroke-miterlimit="1.414"><path d="M178.425 256.001c0 2.266-1.133 4.815-2.832 6.515L43.599 394.509c-1.7 1.7-4.248 2.833-6.514 2.833s-4.816-1.133-6.515-2.833l-14.163-14.162c-1.699-1.7-2.832-3.966-2.832-6.515 0-2.266 1.133-4.815 2.832-6.515l111.317-111.316L16.407 144.685c-1.699-1.7-2.832-4.249-2.832-6.515s1.133-4.815 2.832-6.515l14.163-14.162c1.7-1.7 4.249-2.833 6.515-2.833s4.815 1.133 6.514 2.833l131.994 131.993c1.7 1.7 2.832 4.249 2.832 6.515z" fill-rule="nonzero"></path></svg></span><span class="next"><a href="https://losst.pro/kak-sdelat-zagruzochnuyu-fleshku-ubuntu" rel="next">Как сделать загрузочную флешку Ubuntu</a></span></div>		</nav>
				</footer>
		    <div class="postauthor">
        <h2>Об авторе</h2>
        <div class="author-box">
            <img alt="" src="https://secure.gravatar.com/avatar/f8256cfd6902a4a216e6edb758ac79af?s=150&amp;d=mm&amp;r=g" srcset="https://secure.gravatar.com/avatar/f8256cfd6902a4a216e6edb758ac79af?s=300&amp;d=mm&amp;r=g 2x" class="avatar avatar-150 photo" height="150" width="150" loading="lazy" decoding="async">            <div class="author-box-content">
                <div class="vcard clearfix">
                                            <a href="https://losst.pro/author/ellado" class="fn">ellado</a>
                                    </div>
                                    <p>Больше восьми лет назад мною было принято решение объявить бойкот оконной монополии и установить на свой компьютер Ubuntu. С тех пор это моя основная ОС. Иногда в порядке эксперимента "подселяю" к ней собратьев из семьи Linux. Увлекаюсь фотографией и горным туризмом. В свободное от работы время пишу статьи для losst.ru.</p>
                            </div>
        </div>
    </div>
    <div class="clearpostauthor"></div>
    
<style>
.wplogout-social-wrapper {
	  text-align: center;
    display: flex;
    flex-wrap: wrap;
    margin: 30px 0;
    font-size: 0;
}

.wplogout-social-sharing {
    font-size: 17px;
    padding: 7px 20px;
	  flex: 1;
}

@media only screen and (max-width: 600px) {
    .wplogout-social-sharing {
        font-size: 17px;
        padding: 7px 12px;
        display: inline-block;
    }
}

.wplogout-social-sharing svg {
    position: relative;
    top: 0.15em;
    display: inline-block;
}

.wplogout-social-sharing:first-of-type {
    border-radius: 10px 0 0 10px;
}

.wplogout-social-sharing:last-of-type {
    border-radius: 0 10px 10px 0;
}

.wplogout-social-facebook {
    fill: #fff;
    background-color: rgba(59, 89, 152, 1);

}

.wplogout-social-facebook:hover {
    background-color: rgba(59, 89, 152, .8);
}

.wplogout-social-twitter {
    fill: #fff;
    background-color: rgba(29, 161, 242, 1);
}

.wplogout-social-twitter:hover {
    background-color: rgba(29, 161, 242, .8);
}

.wplogout-social-pinterest {
    fill: #fff;
    background-color: rgba(189, 8, 28, 1);
}

.wplogout-social-pinterest:hover {
    background-color: rgba(189, 8, 28, .8);
}

.wplogout-social-linkedin {
    fill: #fff;
    background-color: rgba(0, 119, 181, 1);
}

.wplogout-social-linkedin:hover {
    background-color: rgba(0, 119, 181, .8);
}
	
.wplogout-social-telegram{   
	  fill: #fff;
    background-color: rgba(0,136,204 ,1);
}

.wplogout-social-telegram:hover {    
    background-color: rgba(0,136,204 ,.8);
}

.wplogout-social-reddit {
    fill: #fff;
    background-color: rgba(255, 87, 0, 1);
}

.wplogout-social-reddit:hover {
    background-color: rgba(255, 87, 0, .8);
}
</style>

<div class="wplogout-social-wrapper">
		<a class="wplogout-social-sharing wplogout-social-facebook" href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Flosst.pro%2Fkomanda-less-v-linux" target="_blank" rel="nofollow"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"><path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"></path></svg></a>
	<a class="wplogout-social-sharing wplogout-social-twitter" href="https://twitter.com/intent/tweet?text=%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0+less+%D0%B2+Linux&amp;url=https%3A%2F%2Flosst.pro%2Fkomanda-less-v-linux&amp;via=losstoffiical" target="_blank" rel="nofollow"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"><path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"></path></svg></a>
	<a class="wplogout-social-sharing wplogout-social-pinterest" href="https://pinterest.com/pin/create/button/?url=https%3A%2F%2Flosst.pro%2Fkomanda-less-v-linux&amp;media=https%3A%2F%2Flosst.pro%2Fwp-content%2Fuploads%2F2020%2F07%2F2.png&amp;description=%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0+less+%D0%B2+Linux" target="_blank" rel="nofollow"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"><path d="M12 0c-6.627 0-12 5.372-12 12 0 5.084 3.163 9.426 7.627 11.174-.105-.949-.2-2.405.042-3.441.218-.937 1.407-5.965 1.407-5.965s-.359-.719-.359-1.782c0-1.668.967-2.914 2.171-2.914 1.023 0 1.518.769 1.518 1.69 0 1.029-.655 2.568-.994 3.995-.283 1.194.599 2.169 1.777 2.169 2.133 0 3.772-2.249 3.772-5.495 0-2.873-2.064-4.882-5.012-4.882-3.414 0-5.418 2.561-5.418 5.207 0 1.031.397 2.138.893 2.738.098.119.112.224.083.345l-.333 1.36c-.053.22-.174.267-.402.161-1.499-.698-2.436-2.889-2.436-4.649 0-3.785 2.75-7.262 7.929-7.262 4.163 0 7.398 2.967 7.398 6.931 0 4.136-2.607 7.464-6.227 7.464-1.216 0-2.359-.631-2.75-1.378l-.748 2.853c-.271 1.043-1.002 2.35-1.492 3.146 1.124.347 2.317.535 3.554.535 6.627 0 12-5.373 12-12 0-6.628-5.373-12-12-12z" fill-rule="evenodd" clip-rule="evenodd"></path></svg></a>
	<a class="wplogout-social-sharing wplogout-social-linkedin" href="https://www.linkedin.com/shareArticle?url=https%3A%2F%2Flosst.pro%2Fkomanda-less-v-linux&amp;title=%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0+less+%D0%B2+Linux&amp;mini=true" target="_blank" rel="nofollow"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"><path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"></path></svg></a>
<a class="wplogout-social-sharing wplogout-social-telegram" href="https://t.me/share/url?url=https%3A%2F%2Flosst.pro%2Fkomanda-less-v-linux&amp;text=%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0+less+%D0%B2+Linux" target="_blank" rel="nofollow"><svg width="24px" height="24px" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve" xmlns:serif="http://www.serif.com/" style="fill-rule:evenodd;clip-rule:evenodd;stroke-linejoin:round;stroke-miterlimit:1.41421;"><path id="telegram-1" d="M18.384,22.779c0.322,0.228 0.737,0.285 1.107,0.145c0.37,-0.141 0.642,-0.457 0.724,-0.84c0.869,-4.084 2.977,-14.421 3.768,-18.136c0.06,-0.28 -0.04,-0.571 -0.26,-0.758c-0.22,-0.187 -0.525,-0.241 -0.797,-0.14c-4.193,1.552 -17.106,6.397 -22.384,8.35c-0.335,0.124 -0.553,0.446 -0.542,0.799c0.012,0.354 0.25,0.661 0.593,0.764c2.367,0.708 5.474,1.693 5.474,1.693c0,0 1.452,4.385 2.209,6.615c0.095,0.28 0.314,0.5 0.603,0.576c0.288,0.075 0.596,-0.004 0.811,-0.207c1.216,-1.148 3.096,-2.923 3.096,-2.923c0,0 3.572,2.619 5.598,4.062Zm-11.01,-8.677l1.679,5.538l0.373,-3.507c0,0 6.487,-5.851 10.185,-9.186c0.108,-0.098 0.123,-0.262 0.033,-0.377c-0.089,-0.115 -0.253,-0.142 -0.376,-0.064c-4.286,2.737 -11.894,7.596 -11.894,7.596Z"></path></svg></a>
	<a class="wplogout-social-sharing wplogout-social-reddit" href="https://reddit.com/submit?url=https%3A%2F%2Flosst.pro%2Fkomanda-less-v-linux&amp;title=%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B0+less+%D0%B2+Linux" target="_blank" rel="nofollow"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"><path d="M24 11.779c0-1.459-1.192-2.645-2.657-2.645-.715 0-1.363.286-1.84.746-1.81-1.191-4.259-1.949-6.971-2.046l1.483-4.669 4.016.941-.006.058c0 1.193.975 2.163 2.174 2.163 1.198 0 2.172-.97 2.172-2.163s-.975-2.164-2.172-2.164c-.92 0-1.704.574-2.021 1.379l-4.329-1.015c-.189-.046-.381.063-.44.249l-1.654 5.207c-2.838.034-5.409.798-7.3 2.025-.474-.438-1.103-.712-1.799-.712-1.465 0-2.656 1.187-2.656 2.646 0 .97.533 1.811 1.317 2.271-.052.282-.086.567-.086.857 0 3.911 4.808 7.093 10.719 7.093s10.72-3.182 10.72-7.093c0-.274-.029-.544-.075-.81.832-.447 1.405-1.312 1.405-2.318zm-17.224 1.816c0-.868.71-1.575 1.582-1.575.872 0 1.581.707 1.581 1.575s-.709 1.574-1.581 1.574-1.582-.706-1.582-1.574zm9.061 4.669c-.797.793-2.048 1.179-3.824 1.179l-.013-.003-.013.003c-1.777 0-3.028-.386-3.824-1.179-.145-.144-.145-.379 0-.523.145-.145.381-.145.526 0 .65.647 1.729.961 3.298.961l.013.003.013-.003c1.569 0 2.648-.315 3.298-.962.145-.145.381-.144.526 0 .145.145.145.379 0 .524zm-.189-3.095c-.872 0-1.581-.706-1.581-1.574 0-.868.709-1.575 1.581-1.575s1.581.707 1.581 1.575-.709 1.574-1.581 1.574z"></path></svg></a>
</div>	</div>
</article>
