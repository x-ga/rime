# 开始
我是一个学生,苦恼于选择好用的输入法,后来我看到了 Rime(小狼毫) 便觉得这是一个好用的输入法,这是我的配置过程

**本文参考了许多教程和 Rime Wiki**

# 配置文件

右键小狼毫

![图片](https://user-images.githubusercontent.com/77675898/161386027-57d02686-2631-47c1-bfd6-f6835f39de3d.png)

选择用户文件夹,在里面新建文件`weasel.custom.yaml`

里面写入这些内容

```yaml
customization:
  distribution_code_name: Weasel
  distribution_version: 0.14.3
  generator: "Weasel::UIStyleSettings"
  modified_time: "Sat Apr  2 19:41:13 2022"
  rime_version: 1.5.3
patch:
  "style/color_scheme": jeekme
  "style/horizontal": false
  "style/display_tray_icon": true
  "style/font_face": "PhigrosFont"
  "style/font_point": 13
  "style/inline_preedit": false
  "preset_color_schemes/jeekme":
    name: HajeeknThemes
    author: Hajeekn
    back_color: 0x252D80
    border_color: 0x3440B3
    text_color: 0x3F4DD9
    hilited_text_color: 0xFFFFFF
    hilited_back_color: 0x303AA6
    hilited_candidate_text_color: 0x303AA6
    hilited_candidate_back_color: 0x161B4D
    candidate_text_color: 0x4A66FF
    comment_text_color: 0x3852E0
 ```
 ## 内容解析
 ![图片](https://user-images.githubusercontent.com/77675898/161386127-113a2723-61d6-4e06-b3b5-a29e7485e45a.png)

`color_scheme` 项指定使用的主题

`horizontal` 项指定为横排显示还是竖排显示(`false`则为竖排;`true`则为横排)

`display_tray_icon` 项指定是否显示托盘图标

`font_face` 项指定字体

`font_point` 项指定字体的大小(字号)

`inline_preedit` 项指定是否不内嵌文字(`false`则内嵌文字;`true`则在文字编辑器内显示文字,具体对比如下图)

内嵌文字:
 ![图片](https://user-images.githubusercontent.com/77675898/161386280-2438e3c8-6690-423c-842e-fd2fce6f2a67.png)
不内嵌文字:
![图片](https://user-images.githubusercontent.com/77675898/161386300-3ff0488e-6308-46cb-994e-c14f330368b3.png)

我比较喜欢内嵌文字,所以这里我给的是`false`

接着编辑`default.custom.yaml`文件

```yaml
customization:
  distribution_code_name: Weasel
  distribution_version: 0.14.3
  generator: "Rime::SwitcherSettings"
  modified_time: "Sat Apr  2 19:30:43 2022"
  rime_version: 1.5.3
patch:
  schema_list:
    - {schema: luna_pinyin_simp}
    - {schema: easy_en}
    - {schema: terra_pinyin}
  "menu/page_size": 7
  "switcher/hotkeys":
    -"Control+Shift"
  "ascii_composer/switch_key":
    Shift_L: noop
    Shift_R: noop
    Caps_Lock: commit_code
```
这里我们设置了候选词为 7 个,切换输入法的热键为`Ctrl` + `Shift`(不过 Windows 自带的 `Ctrl` + `Space` 似乎已经够用了?)

还设置了大写直接提交文字，不过如果你不需要可以删除这部分

![图片](https://user-images.githubusercontent.com/77675898/161386461-b753d960-624a-4ca6-bbaa-718036b8c2a3.png)

# 暂时完结
搜狗词库导入这部分等下次更新罢😂
