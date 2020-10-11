# Lab 2

    本节目标：
      1. 巩固算术运算有关知识
      2. 学会宏定义常量
      3. 熟练使用循环语句与判断语句
      4. 了解浮点数比较

## 获取及提交lab

**获取**：通过 `https://github.com/C-FUDAN-2020/lab4` 获取。

**提交物**：将你完成目标 1 思考题的文档和目标 2，3，4 的源代码文件作为 lab4 的提交物。

**提交**：将提交物文档命名为学号_姓名 （如20302010000_王明），提交至超星学习通对应的作业中。

**截止时间**：北京时间 2020年9月18日 23:59:59 

## 你真的会算术运算吗？（目标 1）

根据之前课程的学习和小学二年级的经验，大家一定能熟练使用算术运算符(`+`, `-`, `*`, `/`, `+=`, `-=`, `++`, `--`)进行整数、浮点数的运算了。但是，你真的学会使用算术运算符了吗？

如果你认为完全了解了算术运算，请回答助教提出的两个问题

> 这两个问题请提交书面答案的文档

### 问题一：自增

观察下面一段代码，思考控制台会有何种输出，并解释原因。

```c
#include <stdio.h>

int main() {
  int x = 1;
  // level 1
  x++;
  printf("%d\n", x);
  ++x;
  printf("%d\n", x);
  // level 2
  int a1 = x++;
  printf("%d\n", a1);
  int a2 = ++x;
  printf("%d\n", a2);
  // level 3
  int b1 = x++ + x++;
  printf("%d\n", b1);
  int b2 = x++ + ++x;
  printf("%d\n", b2);
  int b3 = ++x + ++x;
  printf("%d\n", b3);
  return 0; 
}
```

### 问题二：简单的类型转换

观察下面几段代码，它们能否通过编译，如果不能，请解释原因，如果能，x 的值为多少？并解释原因。

```c
char x = 'a';
x++;
```

```c
char x = 1;
x += 256;
```

```c
char x = 1.9f;
x = x * 1.9f;
```

```c
char a = 16.5f;
double PI = 3.14159;
short x = (float)(4 / 3) * PI * (int)a * a * (double)a;
```

## 编程题（目标 2, 3, 4）

Write a program to approximate the value of π using the following formula：

<svg xmlns="http://www.w3.org/2000/svg" width="39.477ex" height="4.663ex" viewBox="0 -1353 17448.9 2061" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" style=""><defs><path id="MJX-76-TEX-I-1D70B" d="M132 -11Q98 -11 98 22V33L111 61Q186 219 220 334L228 358H196Q158 358 142 355T103 336Q92 329 81 318T62 297T53 285Q51 284 38 284Q19 284 19 294Q19 300 38 329T93 391T164 429Q171 431 389 431Q549 431 553 430Q573 423 573 402Q573 371 541 360Q535 358 472 358H408L405 341Q393 269 393 222Q393 170 402 129T421 65T431 37Q431 20 417 5T381 -10Q370 -10 363 -7T347 17T331 77Q330 86 330 121Q330 170 339 226T357 318T367 358H269L268 354Q268 351 249 275T206 114T175 17Q164 -11 132 -11Z"></path><path id="MJX-76-TEX-N-3D" d="M56 347Q56 360 70 367H707Q722 359 722 347Q722 336 708 328L390 327H72Q56 332 56 347ZM56 153Q56 168 72 173H708Q722 163 722 153Q722 140 707 133H70Q56 140 56 153Z"></path><path id="MJX-76-TEX-N-34" d="M462 0Q444 3 333 3Q217 3 199 0H190V46H221Q241 46 248 46T265 48T279 53T286 61Q287 63 287 115V165H28V211L179 442Q332 674 334 675Q336 677 355 677H373L379 671V211H471V165H379V114Q379 73 379 66T385 54Q393 47 442 46H471V0H462ZM293 211V545L74 212L183 211H293Z"></path><path id="MJX-76-TEX-N-2212" d="M84 237T84 250T98 270H679Q694 262 694 250T679 230H98Q84 237 84 250Z"></path><path id="MJX-76-TEX-N-33" d="M127 463Q100 463 85 480T69 524Q69 579 117 622T233 665Q268 665 277 664Q351 652 390 611T430 522Q430 470 396 421T302 350L299 348Q299 347 308 345T337 336T375 315Q457 262 457 175Q457 96 395 37T238 -22Q158 -22 100 21T42 130Q42 158 60 175T105 193Q133 193 151 175T169 130Q169 119 166 110T159 94T148 82T136 74T126 70T118 67L114 66Q165 21 238 21Q293 21 321 74Q338 107 338 175V195Q338 290 274 322Q259 328 213 329L171 330L168 332Q166 335 166 348Q166 366 174 366Q202 366 232 371Q266 376 294 413T322 525V533Q322 590 287 612Q265 626 240 626Q208 626 181 615T143 592T132 580H135Q138 579 143 578T153 573T165 566T175 555T183 540T186 520Q186 498 172 481T127 463Z"></path><path id="MJX-76-TEX-N-2B" d="M56 237T56 250T70 270H369V420L370 570Q380 583 389 583Q402 583 409 568V270H707Q722 262 722 250T707 230H409V-68Q401 -82 391 -82H389H387Q375 -82 369 -68V230H70Q56 237 56 250Z"></path><path id="MJX-76-TEX-N-35" d="M164 157Q164 133 148 117T109 101H102Q148 22 224 22Q294 22 326 82Q345 115 345 210Q345 313 318 349Q292 382 260 382H254Q176 382 136 314Q132 307 129 306T114 304Q97 304 95 310Q93 314 93 485V614Q93 664 98 664Q100 666 102 666Q103 666 123 658T178 642T253 634Q324 634 389 662Q397 666 402 666Q410 666 410 648V635Q328 538 205 538Q174 538 149 544L139 546V374Q158 388 169 396T205 412T256 420Q337 420 393 355T449 201Q449 109 385 44T229 -22Q148 -22 99 32T50 154Q50 178 61 192T84 210T107 214Q132 214 148 197T164 157Z"></path><path id="MJX-76-TEX-N-37" d="M55 458Q56 460 72 567L88 674Q88 676 108 676H128V672Q128 662 143 655T195 646T364 644H485V605L417 512Q408 500 387 472T360 435T339 403T319 367T305 330T292 284T284 230T278 162T275 80Q275 66 275 52T274 28V19Q270 2 255 -10T221 -22Q210 -22 200 -19T179 0T168 40Q168 198 265 368Q285 400 349 489L395 552H302Q128 552 119 546Q113 543 108 522T98 479L95 458V455H55V458Z"></path><path id="MJX-76-TEX-N-39" d="M352 287Q304 211 232 211Q154 211 104 270T44 396Q42 412 42 436V444Q42 537 111 606Q171 666 243 666Q245 666 249 666T257 665H261Q273 665 286 663T323 651T370 619T413 560Q456 472 456 334Q456 194 396 97Q361 41 312 10T208 -22Q147 -22 108 7T68 93T121 149Q143 149 158 135T173 96Q173 78 164 65T148 49T135 44L131 43Q131 41 138 37T164 27T206 22H212Q272 22 313 86Q352 142 352 280V287ZM244 248Q292 248 321 297T351 430Q351 508 343 542Q341 552 337 562T323 588T293 615T246 625Q208 625 181 598Q160 576 154 546T147 441Q147 358 152 329T172 282Q197 248 244 248Z"></path><path id="MJX-76-TEX-N-31" d="M213 578L200 573Q186 568 160 563T102 556H83V602H102Q149 604 189 617T245 641T273 663Q275 666 285 666Q294 666 302 660V361L303 61Q310 54 315 52T339 48T401 46H427V0H416Q395 3 257 3Q121 3 100 0H88V46H114Q136 46 152 46T177 47T193 50T201 52T207 57T213 61V578Z"></path><path id="MJX-76-TEX-N-2026" d="M78 60Q78 84 95 102T138 120Q162 120 180 104T199 61Q199 36 182 18T139 0T96 17T78 60ZM525 60Q525 84 542 102T585 120Q609 120 627 104T646 61Q646 36 629 18T586 0T543 17T525 60ZM972 60Q972 84 989 102T1032 120Q1056 120 1074 104T1093 61Q1093 36 1076 18T1033 0T990 17T972 60Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="mi"><use xlink:href="#MJX-76-TEX-I-1D70B"></use></g><g data-mml-node="mo" transform="translate(847.8, 0)"><use xlink:href="#MJX-76-TEX-N-3D"></use></g><g data-mml-node="mn" transform="translate(1903.6, 0)"><use xlink:href="#MJX-76-TEX-N-34"></use></g><g data-mml-node="mo" transform="translate(2625.8, 0)"><use xlink:href="#MJX-76-TEX-N-2212"></use></g><g data-mml-node="mfrac" transform="translate(3626, 0)"><g data-mml-node="mn" transform="translate(220, 676)"><use xlink:href="#MJX-76-TEX-N-34"></use></g><g data-mml-node="mn" transform="translate(220, -686)"><use xlink:href="#MJX-76-TEX-N-33"></use></g><rect width="700" height="60" x="120" y="220"></rect></g><g data-mml-node="mo" transform="translate(4788.2, 0)"><use xlink:href="#MJX-76-TEX-N-2B"></use></g><g data-mml-node="mfrac" transform="translate(5788.4, 0)"><g data-mml-node="mn" transform="translate(220, 676)"><use xlink:href="#MJX-76-TEX-N-34"></use></g><g data-mml-node="mn" transform="translate(220, -686)"><use xlink:href="#MJX-76-TEX-N-35"></use></g><rect width="700" height="60" x="120" y="220"></rect></g><g data-mml-node="mo" transform="translate(6950.7, 0)"><use xlink:href="#MJX-76-TEX-N-2212"></use></g><g data-mml-node="mfrac" transform="translate(7950.9, 0)"><g data-mml-node="mn" transform="translate(220, 676)"><use xlink:href="#MJX-76-TEX-N-34"></use></g><g data-mml-node="mn" transform="translate(220, -686)"><use xlink:href="#MJX-76-TEX-N-37"></use></g><rect width="700" height="60" x="120" y="220"></rect></g><g data-mml-node="mo" transform="translate(9113.1, 0)"><use xlink:href="#MJX-76-TEX-N-2B"></use></g><g data-mml-node="mfrac" transform="translate(10113.3, 0)"><g data-mml-node="mn" transform="translate(220, 676)"><use xlink:href="#MJX-76-TEX-N-34"></use></g><g data-mml-node="mn" transform="translate(220, -686)"><use xlink:href="#MJX-76-TEX-N-39"></use></g><rect width="700" height="60" x="120" y="220"></rect></g><g data-mml-node="mo" transform="translate(11275.6, 0)"><use xlink:href="#MJX-76-TEX-N-2212"></use></g><g data-mml-node="mfrac" transform="translate(12275.8, 0)"><g data-mml-node="mn" transform="translate(470, 676)"><use xlink:href="#MJX-76-TEX-N-34"></use></g><g data-mml-node="mn" transform="translate(220, -686)"><use xlink:href="#MJX-76-TEX-N-31"></use><use xlink:href="#MJX-76-TEX-N-31" transform="translate(500, 0)"></use></g><rect width="1200" height="60" x="120" y="220"></rect></g><g data-mml-node="mo" transform="translate(13938, 0)"><use xlink:href="#MJX-76-TEX-N-2B"></use></g><g data-mml-node="mo" transform="translate(14938.2, 0)"><use xlink:href="#MJX-76-TEX-N-2026"></use></g><g data-mml-node="mo" transform="translate(16276.9, 0)"><use xlink:href="#MJX-76-TEX-N-2026"></use></g></g></g></svg>

Please answer how many items must the program calculate to get the values 3.14, 3.141, 3.1415, 3.14159.

> 注意：
> 1. 请使用宏定义（`#define`）定义以上数值常量
> 2. 浮点数并非真正意义上的实数，只是其在某个范围内的近似。因此两个浮点数比较大小时，不能简单地使用大于小于号进行比较，应该判断两个浮点数差值的绝对值是否近似为0。
> 3. 绝对值计算可以调用 `<math.h>` 的库函数 `fabs()`
