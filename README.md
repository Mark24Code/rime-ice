# 雾凇拼音

![demo](./others/demo.webp)

功能齐全，词库体验良好，长期更新修订。

详细介绍：[Rime 配置：雾凇拼音](https://dvel.me/posts/rime-ice/)

常见问题：[常见问题 #133](https://github.com/iDvel/rime-ice/issues/133)

## 基本套路

- 简体 | 全拼 | 双拼
- 主要功能
    -   [melt_eng](https://github.com/tumuyan/rime-melt) 英文输入
    -   [优化英文输入体验](https://dvel.me/posts/make-rime-en-better/)
    -   [两分输入法](http://cheonhyeong.com/Simplified/download.html) 拼字
    -   简繁切换
    -   日期、时间、星期
    -   自整理的 Emoji
    -   [以词定字](https://github.com/BlindingDark/rime-lua-select-character)
    -   [长词优先](https://github.com/tumuyan/rime-melt/blob/master/lua/melt.lua)
    -   [Unicode](https://github.com/shewer/librime-lua-script/blob/main/lua/component/unicode.lua)
    -   所有标点符号直接上屏，/ 模式改为 v 模式，/ 直接上屏
    -   增加了许多拼音纠错
- 简体字表、词库
    -   [《通用规范汉字表》](https://github.com/iDvel/The-Table-of-General-Standard-Chinese-Characters)
    -   [华宇野风系统词库](http://bbs.pinyin.thunisoft.com/forum.php?mod=viewthread&tid=30049)
    -   [清华大学开源词库](https://github.com/thunlp/THUOCL)
    -   [《现代汉语常用词表》](https://gist.github.com/indiejoseph/eae09c673460aa0b56db)
    -   [《现代汉语词典》](https://forum.freemdict.com/t/topic/12102)
    -   [《同义词词林》](https://forum.freemdict.com/t/topic/1211)
    -   [《新华成语大词典》](https://forum.freemdict.com/t/topic/11407)
    -   [搜狗网络流行新词](https://pinyin.sogou.com/dict/detail/index/4)
    -   [腾讯词向量](https://ai.tencent.com/ailab/nlp/en/download.html)
- 词库修订
    - 校对大量异形词、错别字、错误注音

<br>

## 长期维护词库

因为没有找到一份比较好的词库，干脆自己维护一个。综合了几个不错的词库，精心调教了很多。

主要维护的词库：

- `8105` 字表。
- `base` 基础词库。
- `sogou` 搜狗流行词。
- `ext` 扩展词库，小词库。
- `tencent` 扩展词库，大词库。
- Emoji

维护内容主要是异形词、错别字的校对，错误注音的修正，缺失的常用词汇的增添，词频的调整。

欢迎在词库方面提 issue，我会及时更新修正。

<br>

## 使用说明

建议备份原先配置，清空配置目录。

### 手动安装

将仓库所有文件复制粘贴进去就好了。

### 东风破 [plum](https://github.com/rime/plum)

所有配方（`others/recipes/*.recipe.yaml`）只是简单地更新覆盖文件，适合更新词库时使用。

后四个配方只是更新词库文件，并不更新 `rime_ice.dict.yaml` 和 `melt_eng.dict.yaml`，因为用户可能会挂载其他词库。

如果更新后部署时报错，可能是增、删、改了文件名，需要检查上面两个文件和词库的对应关系。

安装或更新：全部文件

```
bash rime-install iDvel/rime-ice:others/recipes/full
```

安装或更新：所有词库文件（包含下面三个）

```
bash rime-install iDvel/rime-ice:others/recipes/all_dicts
```

安装或更新：拼音词库文件

```
bash rime-install iDvel/rime-ice:others/recipes/cn_dicts
```

安装或更新：英文词库文件

```
bash rime-install iDvel/rime-ice:others/recipes/en_dicts
```

安装或更新：opencc(emoji)

```
bash rime-install iDvel/rime-ice:others/recipes/opencc
```

<br>

## 感谢 ❤️

上述用到的词库，及 [@Huandeep](https://github.com/Huandeep) 整理的多个词库。

上述提到的方案及功能参考。

搜狗转 Rime：[lewangdev/scel2txt](https://github.com/lewangdev/scel2txt)

大量参考[校对网](http://www.jiaodui.com/bbs/)。

Thanks to JetBrains for the OSS development license.

[![JetBrains](https://resources.jetbrains.com/storage/products/company/brand/logos/jb_beam.svg)](https://jb.gg/OpenSourceSupport)

<br>

## 赞助 ☕

如果觉得项目不错，可以请 Dvel 吃个煎饼馃子。

<img src="./others/sponsor.webp" alt="请 Dvel 吃个煎饼馃子" width=600 />
