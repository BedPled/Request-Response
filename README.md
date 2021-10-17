# Request-Response


# Протокол HTTP. Основы работы с консолью разработчика в браузере.

## Цель: 
получить практические навыки работы с HTTP протоколом. На практике отметить заголовки присущие Request и Response с помощью консоли разработчика в браузере в различных web-ресурсах.

## Постановка задачи: 
написать эссе, отражающее особенности как минимум 10 уникальных HTTP-заголовков для Request и Response.

## Эссе

В первую очередь я решил зайти на сайт https://www.freecodecamp.org/ и посмотреть какийе заголовки он получает и отправляет.
При входе на него я увидел следующие заголовки в консоле разработчика:

### Заголовки ответов
    :authority: mc.yandex.ru
    :method: POST
    :path: /webvisor/24049213?wmode=0&wv-part=1&wv-hit=946045803&page-url=https%3A%2F%2Fhabr.com%2Fru%2Fcompany%2Fmailru%2Fblog%2F450816%2F&rn=1056865860&wv-type=5&browser-info=gdpr%3A14%3Aet%3A1632994249%3Aw%3A2543x723%3Av%3A660%3Az%3A600%3Ai%3A20210930193049%3Au%3A1632994247558093422%3Avf%3A25rt5xty9ed9wej4vp%3Ati%3A2%3Ast%3A1632994249
    :scheme: https
    accept: */*
    accept-encoding: gzip, deflate, br
    accept-language: ru-RU,ru;q=0.9,en-GB;q=0.8,en;q=0.7,en-US;q=0.6
    content-length: 370
    content-type: text/plain
    cookie: yandexuid=9369757881602312145; yuidss=9369757881602312145; i=XZ1VWke84oS6Z6OS/yUvBUnT8SLKiimpj6V6jJG5H2YdX4MVSA5W7/5lSGKLiY4KCBUaYjfUpjsFyuLmMUKpzs2Dfa4=; ymex=1917672145.yrts.1602312145#1917672145.yrtsi.1602312145; is_gdpr=0; is_gdpr_b=CKuXThCdBw==; _ym_d=1602929690; _ym_uid=1602929690634968410; yabs-sid=2154580571632994247
    origin: https://habr.com
    referer: https://habr.com/
    sec-ch-ua: "Chromium";v="94", "Google Chrome";v="94", ";Not A Brand";v="99"
    sec-ch-ua-mobile: ?0
    sec-ch-ua-platform: "Windows"
    sec-fetch-dest: empty
    sec-fetch-mode: cors
    sec-fetch-site: cross-site
    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36
### Заголовки запросов
    :authority: www.freecodecamp.org
    :method: GET
    :path: /
    :scheme: https
    accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
    accept-encoding: gzip, deflate, br
    accept-language: ru-RU,ru;q=0.9,en-GB;q=0.8,en;q=0.7,en-US;q=0.6
    :scheme: https
    cookie: _ga=GA1.2.1696192664.1629215151; __stripe_mid=07a236e3-2ff9-47fd-b34b-db7282aa183715ede9; _csrf=9-HhgFKZ4ZrRFZs01Iil7C0e; csrf_token=jo4qpMqL-ehpeN0edX4LPAHxiHcz_s5oKrG8; jwt_access_token=s%3AeyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2Nlc3NUb2tlbiI6eyJpZCI6Im9DZTExVUc1bklXMTV4bUxWSm03UzM3T25oNjJqTXBwa3JlanJJbWFIVWxsU1ZhOE52aGtlUmJCd25iZEs4eEwiLCJ0dGwiOjc3NzYwMDAwMDAwLCJjcmVhdGVkIjoiMjAyMS0wOC0xN1QxNTo0Nzo1My4xMzNaIiwidXNlcklkIjoiNWRiY2YyYzQyNTI4OTNiY2I2NDAxZTE2In0sImlhdCI6MTYyOTIxNTI3M30.ieMTaOcP1NhsLKDGVTPSTRr-X5nbplfEhopc21Mbgd0.PaOl7YFU0jtmPU9BmVbdprOTBIUgSaAaLqZf9%2Bn7rco; _gid=GA1.2.1051290394.1634389767; _gat=1; __stripe_sid=a2b6742f-9886-4336-8e4e-2bbdb71f33c3cde180
    sec-ch-ua: "Chromium";v="94", "Google Chrome";v="94", ";Not A Brand";v="99"
    sec-ch-ua-mobile: ?0
    sec-ch-ua-platform: "Windows"
    sec-fetch-dest: document
    sec-fetch-mode: navigate
    sec-fetch-site: none
    sec-fetch-user: ?1
    upgrade-insecure-requests: 1
    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.81 Safari/537.36


Среди эти запросов меня заинтересовали следующие:<br/><br/>
**user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36**
Данный запрос передаёт информацию о моей системе и браузере, но мне стало интересно причём тут `Mozilla/5.0`. Как я узнал Mozilla/5.0 - это общий токен, который говорит о том,
что браузер совместим с Mozilla. По историческим причинам почти каждый браузер сегодня его отправляет.<br>

Следующим меня заинтересовал заголовок **content-security-policy:**. Из названия понятно что он связан с какой-то защитой. Поискав в интернете я узнал, что это дополнительный 
уровень защиты от Cross Site Scripting аттак и аттак внедрения данных. <br><br>
**upgrade-insecure-requests:** отправляет сигнал на сервер, выражающий предпочтение клиента в отношении зашифрованного и аутентифицированного ответа, и что он может успешно обработать директиву CSP .
<br><br>
Далее я обратил внимание на заголовок **accept-encoding:** заголовок указывает кодировку содержимого ( как правило, алгоритм сжатия) , что клиент может понять.<br><br>

Далее я пошёл на сайт https://www.edx.org/
### Заголовки ответов
    cache-control: public, max-age=0, must-revalidate
    cf-cache-status: REVALIDATED
    cf-ray: 69f8914218ec0c42-DME
    date: Sun, 17 Oct 2021 09:40:47 GMT
    etag: W/"6169ac1e-6613c"
    expect-ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
    last-modified: Fri, 15 Oct 2021 16:28:14 GMT
    server: cloudflare
    strict-transport-security: max-age=2592000
    vary: Accept-Encoding
    x-frame-options: DENY
### Заголовки запросов
    :authority: www.edx.org
    :method: GET
    :path: /
    :scheme: https
    accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
    accept-encoding: gzip, deflate, br
    accept-language: ru-RU,ru;q=0.9,en-GB;q=0.8,en;q=0.7,en-US;q=0.6
    cache-control: max-age=0
    cookie: sailthru_hid=2803488bf8ce8b33724f4ef7b0b8d5595dc037dffbd29740b311098e848c46a45093f2bf7fe6864b3d713f6a; prod-edx-csrftoken=QVoPZemIKy63XXAVmH9UZWwSTCny9PKkoWVMoGAjNf725cqTh0VDyFJO34zpbzy9; optimizelyEndUserId=oeu1626150127339r0.6518472145814225; _ga=GA1.2.995168510.1626150131; _gcl_au=1.1.1833435035.1626150131; _hjid=73d2f374-abab-47ed-b8d7-59d88b01626e; hubspotutk=8076f1129e7420caac60184db128657b; __hssrc=1; prod-edx-cf-loc=RU; ki_r=; prod.edx.utm={"utm_source":"braze","utm_medium":"email","utm_campaign":"Thursday_Programs_Promo_20210909","created_at":1631675719389}; prod-edx-cookie-policy-viewed=true; ab.storage.userId.dd7cff88-0bc3-4420-b72b-38f460473479=%7B%22g%22%3A%2225969223%22%2C%22c%22%3A1632202678311%2C%22l%22%3A1632202678311%7D; ab.storage.deviceId.dd7cff88-0bc3-4420-b72b-38f460473479=%7B%22g%22%3A%22c0c33a3f-9599-0ced-4bef-aa3d3cb4e1c5%22%2C%22c%22%3A1632202678326%2C%22l%22%3A1632202678326%7D; ajs_anonymous_id=%2258a6dbd3-3b96-4ba0-a5e8-f6ee5c56db2f%22; edxloggedin=true; prod-edx-user-info="{\"version\": 1\054 \"username\": \"alexander_vischnyakov\"\054 \"header_urls\": {\"logout\": \"https://courses.edx.org/logout\"\054 \"account_settings\": \"https://courses.edx.org/account/settings\"\054 \"learner_profile\": \"https://courses.edx.org/u/alexander_vischnyakov\"\054 \"resume_block\": \"https://courses.edx.org/courses/course-v1:MITx+18.01.1x+2T2020/jump_to/block-v1:MITx+18.01.1x+2T2020+type@html+block@lim_1-tab10-text1\"}\054 \"user_image_urls\": {\"full\": \"https://prod-edx-edxapp-assets.edx-cdn.org/static/edx.org-next/images/profiles/default_500.3292bbf079b8.png\"\054 \"large\": \"https://prod-edx-edxapp-assets.edx-cdn.org/static/edx.org-next/images/profiles/default_120.7c4c5c6b90a1.png\"\054 \"medium\": \"https://prod-edx-edxapp-assets.edx-cdn.org/static/edx.org-next/images/profiles/default_50.d29941819645.png\"\054 \"small\": \"https://prod-edx-edxapp-assets.edx-cdn.org/static/edx.org-next/images/profiles/default_30.ee82223aa027.png\"}}"; prod-edx-language-preference=ru; ajs_user_id=25969223; edx-jwt-cookie-header-payload=eyJhbGciOiJSUzUxMiIsImtpZCI6Imxtc3Byb2QwMDIifQ.eyJhdWQiOiAicmlubXlieWVkbnVhdzVwaGxpZENvY0R1ZGJ5bGJPYkRpYkpvZGJvc2dldHNFYmFsZDQiLCAiZXhwIjogMTYzNDQ2NjYyMywgImlhdCI6IDE2MzQ0NjMwMjMsICJpc3MiOiAiaHR0cHM6Ly9jb3Vyc2VzLmVkeC5vcmcvb2F1dGgyIiwgInByZWZlcnJlZF91c2VybmFtZSI6ICJhbGV4YW5kZXJfdmlzY2hueWFrb3YiLCAic2NvcGVzIjogWyJ1c2VyX2lkIiwgImVtYWlsIiwgInByb2ZpbGUiXSwgInZlcnNpb24iOiAiMS4yLjAiLCAic3ViIjogImI4Y2U5NGZjZjZjZDkyYzExMWM2Nzc0ZGQ2Y2IzZmZiIiwgImZpbHRlcnMiOiBbInVzZXI6bWUiXSwgImlzX3Jlc3RyaWN0ZWQiOiBmYWxzZSwgImVtYWlsX3ZlcmlmaWVkIjogdHJ1ZSwgInVzZXJfaWQiOiAyNTk2OTIyMywgImVtYWlsIjogImFsZXhhbmRlci52aXNjaG55YWtvdkBnbWFpbC5jb20iLCAibmFtZSI6ICJcdTA0MTBcdTA0M2JcdTA0MzVcdTA0M2FcdTA0NDFcdTA0MzBcdTA0M2RcdTA0MzRcdTA0NDAgXHUwNDEyXHUwNDM4XHUwNDQ4XHUwNDNkXHUwNDRmXHUwNDNhXHUwNDNlXHUwNDMyIiwgImZhbWlseV9uYW1lIjogIlx1MDQxMlx1MDQzOFx1MDQ0OFx1MDQzZFx1MDQ0Zlx1MDQzYVx1MDQzZVx1MDQzMiIsICJnaXZlbl9uYW1lIjogIlx1MDQxMFx1MDQzYlx1MDQzNVx1MDQzYVx1MDQ0MVx1MDQzMFx1MDQzZFx1MDQzNFx1MDQ0MCIsICJhZG1pbmlzdHJhdG9yIjogZmFsc2UsICJzdXBlcnVzZXIiOiBmYWxzZX0; edx-jwt-cookie-signature=1rOxlEea7Aa5AW-_1FvyWTMOi_WTYA5_Oka2BPe-HDOb3aTzyl0FECU0PxxWyPFUXjT71bsgwF3cu9OiT-ZHOrfEGSB0x0vW0DGcguk8T8wyB1Qt-wFNltv2GPGTy3DoWru_8y1uZDnLeuAkuUPZNCKcwaSxIrtFQuZ1MFTnnLkcdGAEMnPwnIlgGjG4SVYH9va07gkGTdxp6_OXRgAsjoyrwXF8n1_PrhxTBBQAgtduSHX2j3smpYWmrFuO3rZhy_BtXCcjNr_C1iY3ntTOa4mO-6ql-g1cXwkO-DCCeOdr9zEvZFDGnD4RkAlXwSloJOS7d8vErR4K9f3O05F50g; _gid=GA1.2.973770164.1634463027; ki_t=1631205973209%3B1634463040548%3B1634463040548%3B6%3B8; _hjAbsoluteSessionInProgress=0; __hstc=23171429.8076f1129e7420caac60184db128657b.1626150134429.1634086999717.1634463045431.20; ab.storage.sessionId.dd7cff88-0bc3-4420-b72b-38f460473479=%7B%22g%22%3A%2269968539-7728-d262-ca50-51a955ea67d1%22%2C%22e%22%3A1634463093013%2C%22c%22%3A1634463050011%2C%22l%22%3A1634463063013%7D; __hssc=23171429.2.1634463045431
    if-modified-since: Fri, 15 Oct 2021 16:28:14 GMT
    sec-ch-ua: "Chromium";v="94", "Google Chrome";v="94", ";Not A Brand";v="99"
    sec-ch-ua-mobile: ?0
    sec-ch-ua-platform: "Windows"
    sec-fetch-dest: document
    sec-fetch-mode: navigate
    sec-fetch-site: same-site
    sec-fetch-user: ?1
    upgrade-insecure-requests: 1
    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.81 Safari/537.36

Общий заголовок **Cache-Control** используется для задания инструкций кеширования<br><br>
Заголовок HTTP ответа **etag** является идентификатором специфической версии ресурса. Он позволяет более эффективно использовать кеш и сохраняет пропускную способность, позволяя серверу отправлять не весь ответ, если содержимое не изменилось.
<br><br>
**x-frame-options:** может использоваться для указания того, разрешено ли браузеру открывать страницу в frame или iframe. Это используется для защиты от Clickjacking аттак. <br><br>

Заголовок ответа **Vary** определяет, как сопоставить будущие заголовки запроса, чтобы решить, можно ли использовать кешированный ответ, а не запрашивать новый с исходного сервера. Он используется сервером для указания того, какие заголовки он использовал при выборе представления ресурса в алгоритме согласования контента.
<br><br>
Заголовок HTTP запроса **If-Modified-Since** делает запрос условным: сервер отправит обратно запрошенный ресурс с статусом 200, только если он был изменён после указанной даты. Если запрос не был изменён после указанной даты, ответ будет 304 без какого-либо тела
<br><br>
HTTP заголовок запроса **Accept** указывает, какие типы контента, выраженные как MIME типы, клиент может понять. Используя согласование контента, сервер затем выбирает одно из предложений, использует его и информирует клиента о своём выборе с помощью заголовка ответа **Content-Type**.
<br><br>
Таким образом, мы получили практические навыки работы с HTTP протоколом. На практике отметили заголовки присущие Request и Response с помощью консоли разработчика в браузере в различных web-ресурсах. 
