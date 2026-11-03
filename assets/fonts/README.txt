Resource Han Rounded CN
=======================

字体：Resource Han Rounded（资源圆体）CN
作者：CyanoHao
来源：https://github.com/CyanoHao/Resource-Han-Rounded
许可：SIL Open Font License 1.1（可免费商用，保留本声明即可）

本目录的 RHR-CN.woff2 是 ResourceHanRoundedCN-VF.otf 的子集：
- 只保留了页面里用到的 406 个字符（中文、日文假名、拉丁、数字、标点）
- 保留 wght 200–900 可变轴，所以 400 / 500 / 600 / 700 都能用，一个文件搞定
- 体积约 235KB，没有网络请求到外部 CDN

如果之后要加新文字，需要重新做子集，否则新字会回退到系统字体：

  pyftsubset ResourceHanRoundedCN-VF.otf --text-file=chars.txt ^
    --flavor=woff2 --output-file=RHR-CN.woff2 --no-hinting