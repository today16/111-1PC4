# 第4次練習題目-練習-PC4
[deadline 期末前兩周](#)
>撰寫前請注意

1. 請[點選](https://github.com/altoliaw3/111-1PC4.git)該連結連結至題目之倉庫，並對該倉庫進行fork
2. 再藉由上述所提供的連結，把該fork至自己帳號的倉庫clone至本機端，
再進行程式撰寫與文件撰寫

> 正題

請解決下面問題。
該出社會的新鮮人原本要完成程式判斷式片段如下：
```csharp
    if(i_Age >=50 && i_Sex == 1) {
      /*壯年男人的程式執行程式碼區域*/
    } else if(i_Age < 50 && i_Sex == 1) {
      /*年輕男人的程式執行程式碼區域*/
    } else if(i_Age >= 50 && i_Sex == 0) {
      /*壯年女人的程式執行程式碼區域*/
    } else if(i_Age < 50 && i_Sex == 0) {
      /*年輕女人的程式執行程式碼區域*/
    } else {
      /*其他*/
    }
```

但是不幸的是，該新鮮人的鍵盤無法打出`&`符號，請利用：

1. 巢狀控制項進行改寫程式碼。
(不需寫程式，但需於answer嘗試改寫程式片段，當然該程式片段可自行舉例，
若要撰寫(註解部分讓輸出註解內文字即可)，則請在專案(方案)下，建立一個Test1.aspx頁面，並在Test1.aspx.cs的page_load方法內，解決下面問題。)

2. 將原程式片段用笛摩根定律(De Morgan's laws)改寫程式碼。
笛摩根定律公式為如下
<?xml version="1.0" encoding="UTF-8" standalone="no" ?>
<svg xmlns="http://www.w3.org/2000/svg" width="170.488px" height="18.096px" viewBox="0 -750 9419.4 1000" xmlns:xlink="http://www.w3.org/1999/xlink" style=""><defs><path id="MJX-7-TEX-N-AC" d="M56 323T56 336T70 356H596Q603 353 611 343V102Q598 89 591 89Q587 89 584 90T579 94T575 98T572 102L571 209V316H70Q56 323 56 336Z"></path><path id="MJX-7-TEX-N-28" d="M94 250Q94 319 104 381T127 488T164 576T202 643T244 695T277 729T302 750H315H319Q333 750 333 741Q333 738 316 720T275 667T226 581T184 443T167 250T184 58T225 -81T274 -167T316 -220T333 -241Q333 -250 318 -250H315H302L274 -226Q180 -141 137 -14T94 250Z"></path><path id="MJX-7-TEX-I-50" d="M287 628Q287 635 230 637Q206 637 199 638T192 648Q192 649 194 659Q200 679 203 681T397 683Q587 682 600 680Q664 669 707 631T751 530Q751 453 685 389Q616 321 507 303Q500 302 402 301H307L277 182Q247 66 247 59Q247 55 248 54T255 50T272 48T305 46H336Q342 37 342 35Q342 19 335 5Q330 0 319 0Q316 0 282 1T182 2Q120 2 87 2T51 1Q33 1 33 11Q33 13 36 25Q40 41 44 43T67 46Q94 46 127 49Q141 52 146 61Q149 65 218 339T287 628ZM645 554Q645 567 643 575T634 597T609 619T560 635Q553 636 480 637Q463 637 445 637T416 636T404 636Q391 635 386 627Q384 621 367 550T332 412T314 344Q314 342 395 342H407H430Q542 342 590 392Q617 419 631 471T645 554Z"></path><path id="MJX-7-TEX-N-2227" d="M318 591Q325 598 333 598Q344 598 348 591Q349 590 414 445T545 151T611 -4Q609 -22 591 -22Q588 -22 586 -21T581 -20T577 -17T575 -13T572 -9T570 -4L333 528L96 -4Q87 -20 80 -21Q78 -22 75 -22Q57 -22 55 -4Q55 2 120 150T251 444T318 591Z"></path><path id="MJX-7-TEX-I-51" d="M399 -80Q399 -47 400 -30T402 -11V-7L387 -11Q341 -22 303 -22Q208 -22 138 35T51 201Q50 209 50 244Q50 346 98 438T227 601Q351 704 476 704Q514 704 524 703Q621 689 680 617T740 435Q740 255 592 107Q529 47 461 16L444 8V3Q444 2 449 -24T470 -66T516 -82Q551 -82 583 -60T625 -3Q631 11 638 11Q647 11 649 2Q649 -6 639 -34T611 -100T557 -165T481 -194Q399 -194 399 -87V-80ZM636 468Q636 523 621 564T580 625T530 655T477 665Q429 665 379 640Q277 591 215 464T153 216Q153 110 207 59Q231 38 236 38V46Q236 86 269 120T347 155Q372 155 390 144T417 114T429 82T435 55L448 64Q512 108 557 185T619 334T636 468ZM314 18Q362 18 404 39L403 49Q399 104 366 115Q354 117 347 117Q344 117 341 117T337 118Q317 118 296 98T274 52Q274 18 314 18Z"></path><path id="MJX-7-TEX-N-29" d="M60 749L64 750Q69 750 74 750H86L114 726Q208 641 251 514T294 250Q294 182 284 119T261 12T224 -76T186 -143T145 -194T113 -227T90 -246Q87 -249 86 -250H74Q66 -250 63 -250T58 -247T55 -238Q56 -237 66 -225Q221 -64 221 250T66 725Q56 737 55 738Q55 746 60 749Z"></path><path id="MJX-7-TEX-N-2261" d="M56 444Q56 457 70 464H707Q722 456 722 444Q722 430 706 424H72Q56 429 56 444ZM56 237T56 250T70 270H707Q722 262 722 250T707 230H70Q56 237 56 250ZM56 56Q56 71 72 76H706Q722 70 722 56Q722 44 707 36H70Q56 43 56 56Z"></path><path id="MJX-7-TEX-N-2228" d="M55 580Q56 587 61 592T75 598Q86 598 96 580L333 48L570 580Q579 596 586 597Q588 598 591 598Q609 598 611 580Q611 574 546 426T415 132T348 -15Q343 -22 333 -22T318 -15Q317 -14 252 131T121 425T55 580Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="mi"><use xlink:href="#MJX-7-TEX-N-AC"></use></g><g data-mml-node="mo" transform="translate(667, 0)"><use xlink:href="#MJX-7-TEX-N-28"></use></g><g data-mml-node="mi" transform="translate(1056, 0)"><use xlink:href="#MJX-7-TEX-I-50"></use></g><g data-mml-node="mo" transform="translate(2029.2, 0)"><use xlink:href="#MJX-7-TEX-N-2227"></use></g><g data-mml-node="mi" transform="translate(2918.4, 0)"><use xlink:href="#MJX-7-TEX-I-51"></use></g><g data-mml-node="mo" transform="translate(3709.4, 0)"><use xlink:href="#MJX-7-TEX-N-29"></use></g><g data-mml-node="mo" transform="translate(4376.2, 0)"><use xlink:href="#MJX-7-TEX-N-2261"></use></g><g data-mml-node="mi" transform="translate(5432, 0)"><use xlink:href="#MJX-7-TEX-N-AC"></use></g><g data-mml-node="mi" transform="translate(6099, 0)"><use xlink:href="#MJX-7-TEX-I-50"></use></g><g data-mml-node="mo" transform="translate(7072.2, 0)"><use xlink:href="#MJX-7-TEX-N-2228"></use></g><g data-mml-node="mi" transform="translate(7961.4, 0)"><use xlink:href="#MJX-7-TEX-N-AC"></use></g><g data-mml-node="mi" transform="translate(8628.4, 0)"><use xlink:href="#MJX-7-TEX-I-51"></use></g></g></g></svg>
<?xml version="1.0" encoding="UTF-8" standalone="no" ?>
<svg xmlns="http://www.w3.org/2000/svg" width="170.488px" height="18.096px" viewBox="0 -750 9419.4 1000" xmlns:xlink="http://www.w3.org/1999/xlink" style=""><defs><path id="MJX-8-TEX-N-AC" d="M56 323T56 336T70 356H596Q603 353 611 343V102Q598 89 591 89Q587 89 584 90T579 94T575 98T572 102L571 209V316H70Q56 323 56 336Z"></path><path id="MJX-8-TEX-N-28" d="M94 250Q94 319 104 381T127 488T164 576T202 643T244 695T277 729T302 750H315H319Q333 750 333 741Q333 738 316 720T275 667T226 581T184 443T167 250T184 58T225 -81T274 -167T316 -220T333 -241Q333 -250 318 -250H315H302L274 -226Q180 -141 137 -14T94 250Z"></path><path id="MJX-8-TEX-I-50" d="M287 628Q287 635 230 637Q206 637 199 638T192 648Q192 649 194 659Q200 679 203 681T397 683Q587 682 600 680Q664 669 707 631T751 530Q751 453 685 389Q616 321 507 303Q500 302 402 301H307L277 182Q247 66 247 59Q247 55 248 54T255 50T272 48T305 46H336Q342 37 342 35Q342 19 335 5Q330 0 319 0Q316 0 282 1T182 2Q120 2 87 2T51 1Q33 1 33 11Q33 13 36 25Q40 41 44 43T67 46Q94 46 127 49Q141 52 146 61Q149 65 218 339T287 628ZM645 554Q645 567 643 575T634 597T609 619T560 635Q553 636 480 637Q463 637 445 637T416 636T404 636Q391 635 386 627Q384 621 367 550T332 412T314 344Q314 342 395 342H407H430Q542 342 590 392Q617 419 631 471T645 554Z"></path><path id="MJX-8-TEX-N-2228" d="M55 580Q56 587 61 592T75 598Q86 598 96 580L333 48L570 580Q579 596 586 597Q588 598 591 598Q609 598 611 580Q611 574 546 426T415 132T348 -15Q343 -22 333 -22T318 -15Q317 -14 252 131T121 425T55 580Z"></path><path id="MJX-8-TEX-I-51" d="M399 -80Q399 -47 400 -30T402 -11V-7L387 -11Q341 -22 303 -22Q208 -22 138 35T51 201Q50 209 50 244Q50 346 98 438T227 601Q351 704 476 704Q514 704 524 703Q621 689 680 617T740 435Q740 255 592 107Q529 47 461 16L444 8V3Q444 2 449 -24T470 -66T516 -82Q551 -82 583 -60T625 -3Q631 11 638 11Q647 11 649 2Q649 -6 639 -34T611 -100T557 -165T481 -194Q399 -194 399 -87V-80ZM636 468Q636 523 621 564T580 625T530 655T477 665Q429 665 379 640Q277 591 215 464T153 216Q153 110 207 59Q231 38 236 38V46Q236 86 269 120T347 155Q372 155 390 144T417 114T429 82T435 55L448 64Q512 108 557 185T619 334T636 468ZM314 18Q362 18 404 39L403 49Q399 104 366 115Q354 117 347 117Q344 117 341 117T337 118Q317 118 296 98T274 52Q274 18 314 18Z"></path><path id="MJX-8-TEX-N-29" d="M60 749L64 750Q69 750 74 750H86L114 726Q208 641 251 514T294 250Q294 182 284 119T261 12T224 -76T186 -143T145 -194T113 -227T90 -246Q87 -249 86 -250H74Q66 -250 63 -250T58 -247T55 -238Q56 -237 66 -225Q221 -64 221 250T66 725Q56 737 55 738Q55 746 60 749Z"></path><path id="MJX-8-TEX-N-2261" d="M56 444Q56 457 70 464H707Q722 456 722 444Q722 430 706 424H72Q56 429 56 444ZM56 237T56 250T70 270H707Q722 262 722 250T707 230H70Q56 237 56 250ZM56 56Q56 71 72 76H706Q722 70 722 56Q722 44 707 36H70Q56 43 56 56Z"></path><path id="MJX-8-TEX-N-2227" d="M318 591Q325 598 333 598Q344 598 348 591Q349 590 414 445T545 151T611 -4Q609 -22 591 -22Q588 -22 586 -21T581 -20T577 -17T575 -13T572 -9T570 -4L333 528L96 -4Q87 -20 80 -21Q78 -22 75 -22Q57 -22 55 -4Q55 2 120 150T251 444T318 591Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="mi"><use xlink:href="#MJX-8-TEX-N-AC"></use></g><g data-mml-node="mo" transform="translate(667, 0)"><use xlink:href="#MJX-8-TEX-N-28"></use></g><g data-mml-node="mi" transform="translate(1056, 0)"><use xlink:href="#MJX-8-TEX-I-50"></use></g><g data-mml-node="mo" transform="translate(2029.2, 0)"><use xlink:href="#MJX-8-TEX-N-2228"></use></g><g data-mml-node="mi" transform="translate(2918.4, 0)"><use xlink:href="#MJX-8-TEX-I-51"></use></g><g data-mml-node="mo" transform="translate(3709.4, 0)"><use xlink:href="#MJX-8-TEX-N-29"></use></g><g data-mml-node="mo" transform="translate(4376.2, 0)"><use xlink:href="#MJX-8-TEX-N-2261"></use></g><g data-mml-node="mi" transform="translate(5432, 0)"><use xlink:href="#MJX-8-TEX-N-AC"></use></g><g data-mml-node="mi" transform="translate(6099, 0)"><use xlink:href="#MJX-8-TEX-I-50"></use></g><g data-mml-node="mo" transform="translate(7072.2, 0)"><use xlink:href="#MJX-8-TEX-N-2227"></use></g><g data-mml-node="mi" transform="translate(7961.4, 0)"><use xlink:href="#MJX-8-TEX-N-AC"></use></g><g data-mml-node="mi" transform="translate(8628.4, 0)"><use xlink:href="#MJX-8-TEX-I-51"></use></g></g></g></svg>

(不需寫程式，但需於answer嘗試改寫程式片段，當然該程式片段可自行舉例，
若要撰寫(註解部分讓輸出註解內文字即可)，則請在專案(方案)下，建立一個Test2.aspx頁面，並在Test2.aspx.cs的page_load方法內，解決下面問題。)

其中，<?xml version="1.0" encoding="UTF-8" standalone="no" ?>
<svg xmlns="http://www.w3.org/2000/svg" width="12.072px" height="4.832px" viewBox="0 -356 667 267" xmlns:xlink="http://www.w3.org/1999/xlink" style=""><defs><path id="MJX-9-TEX-N-AC" d="M56 323T56 336T70 356H596Q603 353 611 343V102Q598 89 591 89Q587 89 584 90T579 94T575 98T572 102L571 209V316H70Q56 323 56 336Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="mi"><use xlink:href="#MJX-9-TEX-N-AC"></use></g></g></g></svg>
代表not之義；<?xml version="1.0" encoding="UTF-8" standalone="no" ?>
<svg xmlns="http://www.w3.org/2000/svg" width="12.072px" height="11.224px" viewBox="0 -598 667 620" xmlns:xlink="http://www.w3.org/1999/xlink" style=""><defs><path id="MJX-14-TEX-N-2228" d="M55 580Q56 587 61 592T75 598Q86 598 96 580L333 48L570 580Q579 596 586 597Q588 598 591 598Q609 598 611 580Q611 574 546 426T415 132T348 -15Q343 -22 333 -22T318 -15Q317 -14 252 131T121 425T55 580Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="mo"><use xlink:href="#MJX-14-TEX-N-2228"></use></g></g></g></svg>
代表or之義；<?xml version="1.0" encoding="UTF-8" standalone="no" ?>
<svg xmlns="http://www.w3.org/2000/svg" width="12.072px" height="11.224px" viewBox="0 -598 667 620" xmlns:xlink="http://www.w3.org/1999/xlink" style=""><defs><path id="MJX-20-TEX-N-2227" d="M318 591Q325 598 333 598Q344 598 348 591Q349 590 414 445T545 151T611 -4Q609 -22 591 -22Q588 -22 586 -21T581 -20T577 -17T575 -13T572 -9T570 -4L333 528L96 -4Q87 -20 80 -21Q78 -22 75 -22Q57 -22 55 -4Q55 2 120 150T251 444T318 591Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="mo"><use xlink:href="#MJX-20-TEX-N-2227"></use></g></g></g></svg>
代表and之義；<?xml version="1.0" encoding="UTF-8" standalone="no" ?>
<svg xmlns="http://www.w3.org/2000/svg" width="14.080px" height="7.744px" viewBox="0 -464 778 428" xmlns:xlink="http://www.w3.org/1999/xlink" style=""><defs><path id="MJX-23-TEX-N-2261" d="M56 444Q56 457 70 464H707Q722 456 722 444Q722 430 706 424H72Q56 429 56 444ZM56 237T56 250T70 270H707Q722 262 722 250T707 230H70Q56 237 56 250ZM56 56Q56 71 72 76H706Q722 70 722 56Q722 44 707 36H70Q56 43 56 56Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="mo"><use xlink:href="#MJX-23-TEX-N-2261"></use></g></g></g></svg>
代表等價，即左式與右式意義相等。


> 補充說明 (以下各項全需滿足，才會進行評分)

1. 請將完成程式後，撰寫書面內容寫於answer.md
2. 將將該answer.md檔藉由markdown editor 顯示部分，按右鍵進行列印成pdf檔案，
檔名需為answer.md.pdf
3. 將answer.md.pdf檔於[CleverPDF](https://www.cleverpdf.com/zh-tw/encrypt-pdf)進行**防拷貝**，
並將防拷貝後的answer.md.pdf放置至專案下並拖入VS community IDE內的「**方案總管**」
4. 將answer.md使用winrar加密打包，請自己記住密碼，
並於VS community IDE內的「**方案總管**」刪除answer.md檔案
5. 將專案執行git add、commit、push至github後，並於
[google sheet(點我)](https://docs.google.com/spreadsheets/d/1x_GfVISrublmnrn1S43wtEt_XPEKV2AqirTlMZPLCK4/edit#gid=345458270)中找尋相對應之試算表，
並於該位同學位置註記同學之倉庫的url

>該次作業完成預計所需時間 (實作與文件撰寫所需要完成時間) 

* 70 mins 以下：專精
* 介於 70 至 100 mins：熟練
* 介於 100 至 180 mins：平均
* 超過 180 mins：不熟，請多花心思在課業上

