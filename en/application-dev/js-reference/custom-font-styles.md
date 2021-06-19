# Custom Font Styles<a name="EN-US_TOPIC_0000001162414611"></a>

-   [Defining @font-face](#en-us_topic_0000001059340506_section185107316712)
-   [Using font-face](#en-us_topic_0000001059340506_section713052011710)

**font-face**  is used to define the font style. You can define  **font-face**  in  **style**  to specify a font name and resource for your application and then reference this font from  **font-family**.

The custom font can be loaded from the font file in a project.

>![](public_sys-resources/icon-note.gif) **NOTE:** 
>The font format can be .ttf or .otf.

## Defining @font-face<a name="en-us_topic_0000001059340506_section185107316712"></a>

```
@font-face {   
  font-family: HWfont; 
  src: url('/common/HWfont.ttf'); 
}
```

**font-family**

Customize a font.

**src**

Supported sources of customized fonts:

-   Font file in the project: Specify the path of the font file in the project through  **url**. \(You can use absolute paths only. For details, see  [Resources and File Access Rules](file-organization.md#en-us_topic_0000001058830797_section6620355202117).\)

-   You can set only one  **src**  attribute.

## Using font-face<a name="en-us_topic_0000001059340506_section713052011710"></a>

You can set  **font-face**  in  **style**  and specify the name of the  **font-face**  using  **font-family**.

**Example**

Page layout:

```
<div>    
  <text class="demo-text">Test the customized font.</text>  
</div>
```

Page style:

```
@font-face {
  font-family: HWfont;
  src: url("/common/HWfont.ttf");
}
.demo-text {
  font-family: HWfont;
}
```

