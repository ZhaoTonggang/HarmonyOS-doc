# Audio Management<a name="EN-US_TOPIC_0000001162414649"></a>

-   [Modules to Import](#en-us_topic_0000001149807881_s56d19203690d4782bfc74069abb6bd71)
-   [Required Permissions](#en-us_topic_0000001149807881_section11257113618419)
-   [Functions](#en-us_topic_0000001149807881_section1580114415416)
-   [getAudioManager\(\)](#en-us_topic_0000001149807881_section84581011418)
-   [Enums](#en-us_topic_0000001149807881_section115029181495)
-   [AudioVolumeType](#en-us_topic_0000001149807881_section92261857172218)
-   [DeviceFlag](#en-us_topic_0000001149807881_section11285183164210)
-   [DeviceRole](#en-us_topic_0000001149807881_section380038142619)
-   [DeviceType](#en-us_topic_0000001149807881_section11727420122710)
-   [Appendixes](#en-us_topic_0000001149807881_section1933416317165)
-   [AudioManager](#en-us_topic_0000001149807881_section8265143814015)
    -   [setVolume\(AudioVolumeType, number, AsyncCallback<void\>\)](#en-us_topic_0000001149807881_section189141826104616)
    -   [setVolume\(AudioVolumeType, number\)](#en-us_topic_0000001149807881_section102021249114612)
    -   [getVolume\(AudioVolumeType, AsyncCallback<number\>\)](#en-us_topic_0000001149807881_section4387320194714)
    -   [getVolume\(AudioVolumeType\)](#en-us_topic_0000001149807881_section04121965119)
    -   [getMinVolume\(AudioVolumeType, AsyncCallback<number\>\)](#en-us_topic_0000001149807881_section188714283511)
    -   [getMinVolume\(AudioVolumeType\)](#en-us_topic_0000001149807881_section41556389511)
    -   [getMaxVolume\(AudioVolumeType, AsyncCallback<number\>\)](#en-us_topic_0000001149807881_section690395418516)
    -   [getMaxVolume\(AudioVolumeType\)](#en-us_topic_0000001149807881_section155151345217)
    -   [getDevices\(DeviceFlag, AsyncCallback<AudioDeviceDescriptors\>\)](#en-us_topic_0000001149807881_section11536182020523)
    -   [getDevices\(DeviceFlag\)](#en-us_topic_0000001149807881_section181733125210)

-   [AudioDeviceDescriptor](#en-us_topic_0000001149807881_section17427121913310)
-   [AudioDeviceDescriptors](#en-us_topic_0000001149807881_section5181155710523)

>![](public_sys-resources/icon-note.gif) **NOTE:** 
>Due to permission issues, these feature are temporarily unavailable for the standard system.

## Modules to Import<a name="en-us_topic_0000001149807881_s56d19203690d4782bfc74069abb6bd71"></a>

```
import audio from '@ohos.multimedia.audio';
```

## Required Permissions<a name="en-us_topic_0000001149807881_section11257113618419"></a>

None

## Functions<a name="en-us_topic_0000001149807881_section1580114415416"></a>

## getAudioManager\(\)<a name="en-us_topic_0000001149807881_section84581011418"></a>

Obtains an  **AudioManager**  instance.

**Return Values**

<a name="en-us_topic_0000001149807881_table16391145317913"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row2391145319910"><th class="cellrowborder" valign="top" width="17.01%" id="mcps1.1.3.1.1"><p id="en-us_topic_0000001149807881_p13911353991"><a name="en-us_topic_0000001149807881_p13911353991"></a><a name="en-us_topic_0000001149807881_p13911353991"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="82.99%" id="mcps1.1.3.1.2"><p id="en-us_topic_0000001149807881_p193911531395"><a name="en-us_topic_0000001149807881_p193911531395"></a><a name="en-us_topic_0000001149807881_p193911531395"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row1339114531391"><td class="cellrowborder" valign="top" width="17.01%" headers="mcps1.1.3.1.1 "><p id="en-us_topic_0000001149807881_p1338931454713"><a name="en-us_topic_0000001149807881_p1338931454713"></a><a name="en-us_topic_0000001149807881_p1338931454713"></a><a href="#en-us_topic_0000001149807881_section8265143814015">AudioManager</a></p>
</td>
<td class="cellrowborder" valign="top" width="82.99%" headers="mcps1.1.3.1.2 "><p id="en-us_topic_0000001149807881_p1039217531898"><a name="en-us_topic_0000001149807881_p1039217531898"></a><a name="en-us_topic_0000001149807881_p1039217531898"></a>Audio manager</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
var audioManager = audio.getAudioManager();
```

## Enums<a name="en-us_topic_0000001149807881_section115029181495"></a>

## AudioVolumeType<a name="en-us_topic_0000001149807881_section92261857172218"></a>

Enumerates audio stream types.

<a name="en-us_topic_0000001149807881_table689215633911"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row19892165613399"><th class="cellrowborder" valign="top" width="30.380000000000003%" id="mcps1.1.4.1.1"><p id="en-us_topic_0000001149807881_p148924564394"><a name="en-us_topic_0000001149807881_p148924564394"></a><a name="en-us_topic_0000001149807881_p148924564394"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="9.950000000000001%" id="mcps1.1.4.1.2"><p id="en-us_topic_0000001149807881_aace9cae4ba0d4939bfa048460f61c3c7"><a name="en-us_topic_0000001149807881_aace9cae4ba0d4939bfa048460f61c3c7"></a><a name="en-us_topic_0000001149807881_aace9cae4ba0d4939bfa048460f61c3c7"></a>Default Value</p>
</th>
<th class="cellrowborder" valign="top" width="59.67%" id="mcps1.1.4.1.3"><p id="en-us_topic_0000001149807881_p19892145616392"><a name="en-us_topic_0000001149807881_p19892145616392"></a><a name="en-us_topic_0000001149807881_p19892145616392"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row1389215612395"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p52851329122117"><a name="en-us_topic_0000001149807881_p52851329122117"></a><a name="en-us_topic_0000001149807881_p52851329122117"></a>MEDIA</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p2282152962115"><a name="en-us_topic_0000001149807881_p2282152962115"></a><a name="en-us_topic_0000001149807881_p2282152962115"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p328012293211"><a name="en-us_topic_0000001149807881_p328012293211"></a><a name="en-us_topic_0000001149807881_p328012293211"></a>Audio streams for media purpose</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row6892145616397"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p027662952110"><a name="en-us_topic_0000001149807881_p027662952110"></a><a name="en-us_topic_0000001149807881_p027662952110"></a>RINGTONE</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p17273229192113"><a name="en-us_topic_0000001149807881_p17273229192113"></a><a name="en-us_topic_0000001149807881_p17273229192113"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p182452299212"><a name="en-us_topic_0000001149807881_p182452299212"></a><a name="en-us_topic_0000001149807881_p182452299212"></a>Audio streams for ring tones</p>
</td>
</tr>
</tbody>
</table>

## DeviceFlag<a name="en-us_topic_0000001149807881_section11285183164210"></a>

Enumerates audio device flags.

<a name="en-us_topic_0000001149807881_table162856320422"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row928593124213"><th class="cellrowborder" valign="top" width="30.380000000000003%" id="mcps1.1.4.1.1"><p id="en-us_topic_0000001149807881_p628553124216"><a name="en-us_topic_0000001149807881_p628553124216"></a><a name="en-us_topic_0000001149807881_p628553124216"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="9.950000000000001%" id="mcps1.1.4.1.2"><p id="en-us_topic_0000001149807881_p1828512314213"><a name="en-us_topic_0000001149807881_p1828512314213"></a><a name="en-us_topic_0000001149807881_p1828512314213"></a>Default Value</p>
</th>
<th class="cellrowborder" valign="top" width="59.67%" id="mcps1.1.4.1.3"><p id="en-us_topic_0000001149807881_p1228612334216"><a name="en-us_topic_0000001149807881_p1228612334216"></a><a name="en-us_topic_0000001149807881_p1228612334216"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row2286435427"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p19184101242511"><a name="en-us_topic_0000001149807881_p19184101242511"></a><a name="en-us_topic_0000001149807881_p19184101242511"></a>OUTPUT_DEVICES_FLAG</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p172861314213"><a name="en-us_topic_0000001149807881_p172861314213"></a><a name="en-us_topic_0000001149807881_p172861314213"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p5286133134212"><a name="en-us_topic_0000001149807881_p5286133134212"></a><a name="en-us_topic_0000001149807881_p5286133134212"></a>Output devices</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row2286163194220"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p5514162412251"><a name="en-us_topic_0000001149807881_p5514162412251"></a><a name="en-us_topic_0000001149807881_p5514162412251"></a>INPUT_DEVICES_FLAG</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p112863354219"><a name="en-us_topic_0000001149807881_p112863354219"></a><a name="en-us_topic_0000001149807881_p112863354219"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p1328617334214"><a name="en-us_topic_0000001149807881_p1328617334214"></a><a name="en-us_topic_0000001149807881_p1328617334214"></a>Input devices</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row10631228192520"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p1731716317259"><a name="en-us_topic_0000001149807881_p1731716317259"></a><a name="en-us_topic_0000001149807881_p1731716317259"></a>ALL_DEVICES_FLAG</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p1364628102517"><a name="en-us_topic_0000001149807881_p1364628102517"></a><a name="en-us_topic_0000001149807881_p1364628102517"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p1864182814256"><a name="en-us_topic_0000001149807881_p1864182814256"></a><a name="en-us_topic_0000001149807881_p1864182814256"></a>All devices</p>
</td>
</tr>
</tbody>
</table>

## DeviceRole<a name="en-us_topic_0000001149807881_section380038142619"></a>

Enumerates device roles.

<a name="en-us_topic_0000001149807881_table48001786268"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row138007814267"><th class="cellrowborder" valign="top" width="30.380000000000003%" id="mcps1.1.4.1.1"><p id="en-us_topic_0000001149807881_p1980068112616"><a name="en-us_topic_0000001149807881_p1980068112616"></a><a name="en-us_topic_0000001149807881_p1980068112616"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="9.950000000000001%" id="mcps1.1.4.1.2"><p id="en-us_topic_0000001149807881_p28003819263"><a name="en-us_topic_0000001149807881_p28003819263"></a><a name="en-us_topic_0000001149807881_p28003819263"></a>Default Value</p>
</th>
<th class="cellrowborder" valign="top" width="59.67%" id="mcps1.1.4.1.3"><p id="en-us_topic_0000001149807881_p3800118112615"><a name="en-us_topic_0000001149807881_p3800118112615"></a><a name="en-us_topic_0000001149807881_p3800118112615"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row98008816264"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p1542334211265"><a name="en-us_topic_0000001149807881_p1542334211265"></a><a name="en-us_topic_0000001149807881_p1542334211265"></a>INPUT_DEVICE</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p98008852610"><a name="en-us_topic_0000001149807881_p98008852610"></a><a name="en-us_topic_0000001149807881_p98008852610"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p118009817260"><a name="en-us_topic_0000001149807881_p118009817260"></a><a name="en-us_topic_0000001149807881_p118009817260"></a>Input role</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row680018802618"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p2011710479267"><a name="en-us_topic_0000001149807881_p2011710479267"></a><a name="en-us_topic_0000001149807881_p2011710479267"></a>OUTPUT_DEVICE</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p08009812613"><a name="en-us_topic_0000001149807881_p08009812613"></a><a name="en-us_topic_0000001149807881_p08009812613"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p380020842611"><a name="en-us_topic_0000001149807881_p380020842611"></a><a name="en-us_topic_0000001149807881_p380020842611"></a>Output role</p>
</td>
</tr>
</tbody>
</table>

## DeviceType<a name="en-us_topic_0000001149807881_section11727420122710"></a>

Enumerates device types.

<a name="en-us_topic_0000001149807881_table67271020132718"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row4727122012711"><th class="cellrowborder" valign="top" width="30.380000000000003%" id="mcps1.1.4.1.1"><p id="en-us_topic_0000001149807881_p157271520152715"><a name="en-us_topic_0000001149807881_p157271520152715"></a><a name="en-us_topic_0000001149807881_p157271520152715"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="9.950000000000001%" id="mcps1.1.4.1.2"><p id="en-us_topic_0000001149807881_p187271620152719"><a name="en-us_topic_0000001149807881_p187271620152719"></a><a name="en-us_topic_0000001149807881_p187271620152719"></a>Default Value</p>
</th>
<th class="cellrowborder" valign="top" width="59.67%" id="mcps1.1.4.1.3"><p id="en-us_topic_0000001149807881_p772720201277"><a name="en-us_topic_0000001149807881_p772720201277"></a><a name="en-us_topic_0000001149807881_p772720201277"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row572714205272"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p1895057192713"><a name="en-us_topic_0000001149807881_p1895057192713"></a><a name="en-us_topic_0000001149807881_p1895057192713"></a>INVALID</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p772892012273"><a name="en-us_topic_0000001149807881_p772892012273"></a><a name="en-us_topic_0000001149807881_p772892012273"></a>0</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p137281920172712"><a name="en-us_topic_0000001149807881_p137281920172712"></a><a name="en-us_topic_0000001149807881_p137281920172712"></a>Invalid device</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row16728520192714"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p4753161132815"><a name="en-us_topic_0000001149807881_p4753161132815"></a><a name="en-us_topic_0000001149807881_p4753161132815"></a>SPEAKER</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p3728920162713"><a name="en-us_topic_0000001149807881_p3728920162713"></a><a name="en-us_topic_0000001149807881_p3728920162713"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p17728112062715"><a name="en-us_topic_0000001149807881_p17728112062715"></a><a name="en-us_topic_0000001149807881_p17728112062715"></a>Speaker</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row1758117472814"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p74802011112815"><a name="en-us_topic_0000001149807881_p74802011112815"></a><a name="en-us_topic_0000001149807881_p74802011112815"></a>WIRED_HEADSET</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p35820462819"><a name="en-us_topic_0000001149807881_p35820462819"></a><a name="en-us_topic_0000001149807881_p35820462819"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p155821548285"><a name="en-us_topic_0000001149807881_p155821548285"></a><a name="en-us_topic_0000001149807881_p155821548285"></a>Wired headset</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row1335108192818"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p107521514142811"><a name="en-us_topic_0000001149807881_p107521514142811"></a><a name="en-us_topic_0000001149807881_p107521514142811"></a>BLUETOOTH_SCO</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p18335108112819"><a name="en-us_topic_0000001149807881_p18335108112819"></a><a name="en-us_topic_0000001149807881_p18335108112819"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p193351683289"><a name="en-us_topic_0000001149807881_p193351683289"></a><a name="en-us_topic_0000001149807881_p193351683289"></a>Bluetooth device using the synchronous connection oriented link (SCO)</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row1649111617286"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p10784017102818"><a name="en-us_topic_0000001149807881_p10784017102818"></a><a name="en-us_topic_0000001149807881_p10784017102818"></a>BLUETOOTH_A2DP</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p849110610286"><a name="en-us_topic_0000001149807881_p849110610286"></a><a name="en-us_topic_0000001149807881_p849110610286"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p549117620284"><a name="en-us_topic_0000001149807881_p549117620284"></a><a name="en-us_topic_0000001149807881_p549117620284"></a>Bluetooth device using advanced audio distribution profile (A2DP)</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row81701220112812"><td class="cellrowborder" valign="top" width="30.380000000000003%" headers="mcps1.1.4.1.1 "><p id="en-us_topic_0000001149807881_p168642028152812"><a name="en-us_topic_0000001149807881_p168642028152812"></a><a name="en-us_topic_0000001149807881_p168642028152812"></a>MIC</p>
</td>
<td class="cellrowborder" valign="top" width="9.950000000000001%" headers="mcps1.1.4.1.2 "><p id="en-us_topic_0000001149807881_p517062012812"><a name="en-us_topic_0000001149807881_p517062012812"></a><a name="en-us_topic_0000001149807881_p517062012812"></a>5</p>
</td>
<td class="cellrowborder" valign="top" width="59.67%" headers="mcps1.1.4.1.3 "><p id="en-us_topic_0000001149807881_p5170520112813"><a name="en-us_topic_0000001149807881_p5170520112813"></a><a name="en-us_topic_0000001149807881_p5170520112813"></a>Microphone</p>
</td>
</tr>
</tbody>
</table>

## Appendixes<a name="en-us_topic_0000001149807881_section1933416317165"></a>

## AudioManager<a name="en-us_topic_0000001149807881_section8265143814015"></a>

Manages audio volume and audio device information.

### setVolume\(AudioVolumeType, number, AsyncCallback<void\>\)<a name="en-us_topic_0000001149807881_section189141826104616"></a>

Sets volume for a stream. This method uses an asynchronous callback to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table11004831415"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row1510164861414"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p171154819142"><a name="en-us_topic_0000001149807881_p171154819142"></a><a name="en-us_topic_0000001149807881_p171154819142"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p121164815148"><a name="en-us_topic_0000001149807881_p121164815148"></a><a name="en-us_topic_0000001149807881_p121164815148"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p1351547105313"><a name="en-us_topic_0000001149807881_p1351547105313"></a><a name="en-us_topic_0000001149807881_p1351547105313"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p131114812144"><a name="en-us_topic_0000001149807881_p131114812144"></a><a name="en-us_topic_0000001149807881_p131114812144"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row911124881410"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p11184811420"><a name="en-us_topic_0000001149807881_p11184811420"></a><a name="en-us_topic_0000001149807881_p11184811420"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p91134810142"><a name="en-us_topic_0000001149807881_p91134810142"></a><a name="en-us_topic_0000001149807881_p91134810142"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p1751247115312"><a name="en-us_topic_0000001149807881_p1751247115312"></a><a name="en-us_topic_0000001149807881_p1751247115312"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p151134811149"><a name="en-us_topic_0000001149807881_p151134811149"></a><a name="en-us_topic_0000001149807881_p151134811149"></a>Audio stream type</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row1811164871417"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p141114817144"><a name="en-us_topic_0000001149807881_p141114817144"></a><a name="en-us_topic_0000001149807881_p141114817144"></a>volume</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p1511648151417"><a name="en-us_topic_0000001149807881_p1511648151417"></a><a name="en-us_topic_0000001149807881_p1511648151417"></a>number</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p151947175314"><a name="en-us_topic_0000001149807881_p151947175314"></a><a name="en-us_topic_0000001149807881_p151947175314"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p16111548121411"><a name="en-us_topic_0000001149807881_p16111548121411"></a><a name="en-us_topic_0000001149807881_p16111548121411"></a>Volume to set</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row85121563158"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p175121965154"><a name="en-us_topic_0000001149807881_p175121965154"></a><a name="en-us_topic_0000001149807881_p175121965154"></a>callback</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p1851220691518"><a name="en-us_topic_0000001149807881_p1851220691518"></a><a name="en-us_topic_0000001149807881_p1851220691518"></a>AsyncCallback&lt;void&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p15134711532"><a name="en-us_topic_0000001149807881_p15134711532"></a><a name="en-us_topic_0000001149807881_p15134711532"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p751211651512"><a name="en-us_topic_0000001149807881_p751211651512"></a><a name="en-us_topic_0000001149807881_p751211651512"></a>Callback used to return whether the setting is successful</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.setVolume(audio.AudioVolumeType.MEDIA, 30, (err)=>{
   if (err) {
	   console.error(`failed to set volume ${err.message}`);
	   return;
   }
   console.log(`Media setVolume successful callback`);
})
```

### setVolume\(AudioVolumeType, number\)<a name="en-us_topic_0000001149807881_section102021249114612"></a>

Sets volume for a stream. This method uses a promise to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table20688181818176"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row1368810188176"><th class="cellrowborder" valign="top" width="17.599999999999998%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p5688818171712"><a name="en-us_topic_0000001149807881_p5688818171712"></a><a name="en-us_topic_0000001149807881_p5688818171712"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.49%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p8688118111719"><a name="en-us_topic_0000001149807881_p8688118111719"></a><a name="en-us_topic_0000001149807881_p8688118111719"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p1994792215711"><a name="en-us_topic_0000001149807881_p1994792215711"></a><a name="en-us_topic_0000001149807881_p1994792215711"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p12688151816173"><a name="en-us_topic_0000001149807881_p12688151816173"></a><a name="en-us_topic_0000001149807881_p12688151816173"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row0688518171714"><td class="cellrowborder" valign="top" width="17.599999999999998%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p1368820182174"><a name="en-us_topic_0000001149807881_p1368820182174"></a><a name="en-us_topic_0000001149807881_p1368820182174"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.49%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p116881518111712"><a name="en-us_topic_0000001149807881_p116881518111712"></a><a name="en-us_topic_0000001149807881_p116881518111712"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p2094702218579"><a name="en-us_topic_0000001149807881_p2094702218579"></a><a name="en-us_topic_0000001149807881_p2094702218579"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p1688131812176"><a name="en-us_topic_0000001149807881_p1688131812176"></a><a name="en-us_topic_0000001149807881_p1688131812176"></a>Audio stream type</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row5688218131711"><td class="cellrowborder" valign="top" width="17.599999999999998%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p176881618181715"><a name="en-us_topic_0000001149807881_p176881618181715"></a><a name="en-us_topic_0000001149807881_p176881618181715"></a>volume</p>
</td>
<td class="cellrowborder" valign="top" width="19.49%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p5688201811720"><a name="en-us_topic_0000001149807881_p5688201811720"></a><a name="en-us_topic_0000001149807881_p5688201811720"></a>number</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p79472226579"><a name="en-us_topic_0000001149807881_p79472226579"></a><a name="en-us_topic_0000001149807881_p79472226579"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p2688718171716"><a name="en-us_topic_0000001149807881_p2688718171716"></a><a name="en-us_topic_0000001149807881_p2688718171716"></a>Volume to set</p>
</td>
</tr>
</tbody>
</table>

**Return Values**

<a name="en-us_topic_0000001149807881_table106721328171713"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row9672122817176"><th class="cellrowborder" valign="top" width="26.06%" id="mcps1.1.3.1.1"><p id="en-us_topic_0000001149807881_p106728288171"><a name="en-us_topic_0000001149807881_p106728288171"></a><a name="en-us_topic_0000001149807881_p106728288171"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="73.94%" id="mcps1.1.3.1.2"><p id="en-us_topic_0000001149807881_p5672112817178"><a name="en-us_topic_0000001149807881_p5672112817178"></a><a name="en-us_topic_0000001149807881_p5672112817178"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row06721528191711"><td class="cellrowborder" valign="top" width="26.06%" headers="mcps1.1.3.1.1 "><p id="en-us_topic_0000001149807881_p107821612171919"><a name="en-us_topic_0000001149807881_p107821612171919"></a><a name="en-us_topic_0000001149807881_p107821612171919"></a>Promise&lt;void&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="73.94%" headers="mcps1.1.3.1.2 "><p id="en-us_topic_0000001149807881_p4672828141718"><a name="en-us_topic_0000001149807881_p4672828141718"></a><a name="en-us_topic_0000001149807881_p4672828141718"></a>Promise used to return whether the setting is successful</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.setVolume(audio.AudioVolumeType.MEDIA, 30).then(()=>
    console.log(`Media setVolume successful callback`);
)
```

### getVolume\(AudioVolumeType, AsyncCallback<number\>\)<a name="en-us_topic_0000001149807881_section4387320194714"></a>

Obtains volume of a stream. This method uses an asynchronous callback to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table44323134204"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row16433171322017"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p1943319132201"><a name="en-us_topic_0000001149807881_p1943319132201"></a><a name="en-us_topic_0000001149807881_p1943319132201"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p143314139203"><a name="en-us_topic_0000001149807881_p143314139203"></a><a name="en-us_topic_0000001149807881_p143314139203"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p1540765014581"><a name="en-us_topic_0000001149807881_p1540765014581"></a><a name="en-us_topic_0000001149807881_p1540765014581"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p10433181362011"><a name="en-us_topic_0000001149807881_p10433181362011"></a><a name="en-us_topic_0000001149807881_p10433181362011"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row4433913122010"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p54331513192018"><a name="en-us_topic_0000001149807881_p54331513192018"></a><a name="en-us_topic_0000001149807881_p54331513192018"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p182075544714"><a name="en-us_topic_0000001149807881_p182075544714"></a><a name="en-us_topic_0000001149807881_p182075544714"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p3407185013588"><a name="en-us_topic_0000001149807881_p3407185013588"></a><a name="en-us_topic_0000001149807881_p3407185013588"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p44331613142018"><a name="en-us_topic_0000001149807881_p44331613142018"></a><a name="en-us_topic_0000001149807881_p44331613142018"></a>Audio stream type</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row743331372014"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p143341319205"><a name="en-us_topic_0000001149807881_p143341319205"></a><a name="en-us_topic_0000001149807881_p143341319205"></a>callback</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p1043316137200"><a name="en-us_topic_0000001149807881_p1043316137200"></a><a name="en-us_topic_0000001149807881_p1043316137200"></a>AsyncCallback&lt;number&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p12659352195818"><a name="en-us_topic_0000001149807881_p12659352195818"></a><a name="en-us_topic_0000001149807881_p12659352195818"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p3433161313204"><a name="en-us_topic_0000001149807881_p3433161313204"></a><a name="en-us_topic_0000001149807881_p3433161313204"></a>Callback used to return the volume</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getVolume(audio.AudioVolumeType.MEDIA, (err, value)=>{
   if (err) {
	   console.error(`failed to get volume ${err.message}`);
	   return;
   }
   console.log(`Media getVolume successful callback`);
})
```

### getVolume\(AudioVolumeType\)<a name="en-us_topic_0000001149807881_section04121965119"></a>

Obtains the volume of a stream. This method uses a promise to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table174341113202016"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row843416136203"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p143410134207"><a name="en-us_topic_0000001149807881_p143410134207"></a><a name="en-us_topic_0000001149807881_p143410134207"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p6434813182016"><a name="en-us_topic_0000001149807881_p6434813182016"></a><a name="en-us_topic_0000001149807881_p6434813182016"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p418721165918"><a name="en-us_topic_0000001149807881_p418721165918"></a><a name="en-us_topic_0000001149807881_p418721165918"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p943491320207"><a name="en-us_topic_0000001149807881_p943491320207"></a><a name="en-us_topic_0000001149807881_p943491320207"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row5434181312207"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p144343134206"><a name="en-us_topic_0000001149807881_p144343134206"></a><a name="en-us_topic_0000001149807881_p144343134206"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p121741711487"><a name="en-us_topic_0000001149807881_p121741711487"></a><a name="en-us_topic_0000001149807881_p121741711487"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p118791205914"><a name="en-us_topic_0000001149807881_p118791205914"></a><a name="en-us_topic_0000001149807881_p118791205914"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p6434613122010"><a name="en-us_topic_0000001149807881_p6434613122010"></a><a name="en-us_topic_0000001149807881_p6434613122010"></a>Audio stream type</p>
</td>
</tr>
</tbody>
</table>

**Return Values**

<a name="en-us_topic_0000001149807881_table11435101313201"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row9435191332013"><th class="cellrowborder" valign="top" width="25.97%" id="mcps1.1.3.1.1"><p id="en-us_topic_0000001149807881_p7435131352019"><a name="en-us_topic_0000001149807881_p7435131352019"></a><a name="en-us_topic_0000001149807881_p7435131352019"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="74.03%" id="mcps1.1.3.1.2"><p id="en-us_topic_0000001149807881_p343521362017"><a name="en-us_topic_0000001149807881_p343521362017"></a><a name="en-us_topic_0000001149807881_p343521362017"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row1143515137209"><td class="cellrowborder" valign="top" width="25.97%" headers="mcps1.1.3.1.1 "><p id="en-us_topic_0000001149807881_p3435171318201"><a name="en-us_topic_0000001149807881_p3435171318201"></a><a name="en-us_topic_0000001149807881_p3435171318201"></a>Promise&lt;number&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="74.03%" headers="mcps1.1.3.1.2 "><p id="en-us_topic_0000001149807881_p17435513102016"><a name="en-us_topic_0000001149807881_p17435513102016"></a><a name="en-us_topic_0000001149807881_p17435513102016"></a>Promise used to return stream volume</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getVolume(audio.AudioVolumeType.MEDIA).then((data)=>
    console.log(`Media getVolume successful callback`);
)
```

### getMinVolume\(AudioVolumeType, AsyncCallback<number\>\)<a name="en-us_topic_0000001149807881_section188714283511"></a>

Obtains the minimum volume allowed for a stream. This method uses an asynchronous callback to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table9585157122219"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row95857713228"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p1358510710223"><a name="en-us_topic_0000001149807881_p1358510710223"></a><a name="en-us_topic_0000001149807881_p1358510710223"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p958577152214"><a name="en-us_topic_0000001149807881_p958577152214"></a><a name="en-us_topic_0000001149807881_p958577152214"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p12979171810590"><a name="en-us_topic_0000001149807881_p12979171810590"></a><a name="en-us_topic_0000001149807881_p12979171810590"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p85851579221"><a name="en-us_topic_0000001149807881_p85851579221"></a><a name="en-us_topic_0000001149807881_p85851579221"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row7585373227"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p105852712216"><a name="en-us_topic_0000001149807881_p105852712216"></a><a name="en-us_topic_0000001149807881_p105852712216"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p1862714319487"><a name="en-us_topic_0000001149807881_p1862714319487"></a><a name="en-us_topic_0000001149807881_p1862714319487"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p59791018125916"><a name="en-us_topic_0000001149807881_p59791018125916"></a><a name="en-us_topic_0000001149807881_p59791018125916"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p758517710222"><a name="en-us_topic_0000001149807881_p758517710222"></a><a name="en-us_topic_0000001149807881_p758517710222"></a>Audio stream type</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row165851718222"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p115866772214"><a name="en-us_topic_0000001149807881_p115866772214"></a><a name="en-us_topic_0000001149807881_p115866772214"></a>callback</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p558614719222"><a name="en-us_topic_0000001149807881_p558614719222"></a><a name="en-us_topic_0000001149807881_p558614719222"></a>AsyncCallback&lt;number&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p89791518185916"><a name="en-us_topic_0000001149807881_p89791518185916"></a><a name="en-us_topic_0000001149807881_p89791518185916"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p1958614711221"><a name="en-us_topic_0000001149807881_p1958614711221"></a><a name="en-us_topic_0000001149807881_p1958614711221"></a>Callback used to return the minimum volume</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getMinVolume(audio.AudioVolumeType.MEDIA, (err, value)=>{
   if (err) {
	   console.error(`failed to get minvolume ${err.message}`);
	   return;
   }
   console.log(`Media getMinVolume successful callback`);
})
```

### getMinVolume\(AudioVolumeType\)<a name="en-us_topic_0000001149807881_section41556389511"></a>

Obtains the minimum volume allowed for a stream. This method uses a promise to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table558627102215"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row175868714227"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p1758619712217"><a name="en-us_topic_0000001149807881_p1758619712217"></a><a name="en-us_topic_0000001149807881_p1758619712217"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p12586776227"><a name="en-us_topic_0000001149807881_p12586776227"></a><a name="en-us_topic_0000001149807881_p12586776227"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p94861627165914"><a name="en-us_topic_0000001149807881_p94861627165914"></a><a name="en-us_topic_0000001149807881_p94861627165914"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p85862711223"><a name="en-us_topic_0000001149807881_p85862711223"></a><a name="en-us_topic_0000001149807881_p85862711223"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row65861477221"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p5586167172217"><a name="en-us_topic_0000001149807881_p5586167172217"></a><a name="en-us_topic_0000001149807881_p5586167172217"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p592519511485"><a name="en-us_topic_0000001149807881_p592519511485"></a><a name="en-us_topic_0000001149807881_p592519511485"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p2048622713593"><a name="en-us_topic_0000001149807881_p2048622713593"></a><a name="en-us_topic_0000001149807881_p2048622713593"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p135871079226"><a name="en-us_topic_0000001149807881_p135871079226"></a><a name="en-us_topic_0000001149807881_p135871079226"></a>Audio stream type</p>
</td>
</tr>
</tbody>
</table>

**Return Values**

<a name="en-us_topic_0000001149807881_table35874718223"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row1558718715227"><th class="cellrowborder" valign="top" width="26.02%" id="mcps1.1.3.1.1"><p id="en-us_topic_0000001149807881_p75871715226"><a name="en-us_topic_0000001149807881_p75871715226"></a><a name="en-us_topic_0000001149807881_p75871715226"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="73.98%" id="mcps1.1.3.1.2"><p id="en-us_topic_0000001149807881_p85871720225"><a name="en-us_topic_0000001149807881_p85871720225"></a><a name="en-us_topic_0000001149807881_p85871720225"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row1458710714221"><td class="cellrowborder" valign="top" width="26.02%" headers="mcps1.1.3.1.1 "><p id="en-us_topic_0000001149807881_p558737142218"><a name="en-us_topic_0000001149807881_p558737142218"></a><a name="en-us_topic_0000001149807881_p558737142218"></a>Promise&lt;number&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="73.98%" headers="mcps1.1.3.1.2 "><p id="en-us_topic_0000001149807881_p05878717229"><a name="en-us_topic_0000001149807881_p05878717229"></a><a name="en-us_topic_0000001149807881_p05878717229"></a>Promise used to return the minimum volume</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getMinVolume(audio.AudioVolumeType.MEDIA).then((data)=>
    console.log(`Media getMinVolume successful callback`);
)
```

### getMaxVolume\(AudioVolumeType, AsyncCallback<number\>\)<a name="en-us_topic_0000001149807881_section690395418516"></a>

Obtains the maximum volume allowed for a stream. This method uses an asynchronous callback to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table7210144262214"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row7210104242215"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p521018428221"><a name="en-us_topic_0000001149807881_p521018428221"></a><a name="en-us_topic_0000001149807881_p521018428221"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p102107424223"><a name="en-us_topic_0000001149807881_p102107424223"></a><a name="en-us_topic_0000001149807881_p102107424223"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p167531439593"><a name="en-us_topic_0000001149807881_p167531439593"></a><a name="en-us_topic_0000001149807881_p167531439593"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p1521054292218"><a name="en-us_topic_0000001149807881_p1521054292218"></a><a name="en-us_topic_0000001149807881_p1521054292218"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row321010428228"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p5210642132212"><a name="en-us_topic_0000001149807881_p5210642132212"></a><a name="en-us_topic_0000001149807881_p5210642132212"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p35691288487"><a name="en-us_topic_0000001149807881_p35691288487"></a><a name="en-us_topic_0000001149807881_p35691288487"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p14753114317590"><a name="en-us_topic_0000001149807881_p14753114317590"></a><a name="en-us_topic_0000001149807881_p14753114317590"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p8210242112217"><a name="en-us_topic_0000001149807881_p8210242112217"></a><a name="en-us_topic_0000001149807881_p8210242112217"></a>Audio stream type</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row82115429227"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p4211842132218"><a name="en-us_topic_0000001149807881_p4211842132218"></a><a name="en-us_topic_0000001149807881_p4211842132218"></a>callback</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p8211114232217"><a name="en-us_topic_0000001149807881_p8211114232217"></a><a name="en-us_topic_0000001149807881_p8211114232217"></a>AsyncCallback&lt;number&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p1275384315910"><a name="en-us_topic_0000001149807881_p1275384315910"></a><a name="en-us_topic_0000001149807881_p1275384315910"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p1621114282212"><a name="en-us_topic_0000001149807881_p1621114282212"></a><a name="en-us_topic_0000001149807881_p1621114282212"></a>Callback used to return the maximum volume</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getMaxVolume(audio.AudioVolumeType.MEDIA, (err, value)=>{
   if (err) {
	   console.error(`failed to get maxvolume ${err.message}`);
	   return;
   }
   console.log(`Media getMaxVolume successful callback`);
})
```

### getMaxVolume\(AudioVolumeType\)<a name="en-us_topic_0000001149807881_section155151345217"></a>

Obtains the maximum volume allowed for a stream. This method uses a promise to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table11211104210226"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row42111424228"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p14211842162217"><a name="en-us_topic_0000001149807881_p14211842162217"></a><a name="en-us_topic_0000001149807881_p14211842162217"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p7211184211223"><a name="en-us_topic_0000001149807881_p7211184211223"></a><a name="en-us_topic_0000001149807881_p7211184211223"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p165812523592"><a name="en-us_topic_0000001149807881_p165812523592"></a><a name="en-us_topic_0000001149807881_p165812523592"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p821164232217"><a name="en-us_topic_0000001149807881_p821164232217"></a><a name="en-us_topic_0000001149807881_p821164232217"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row22111742112216"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p152121542152218"><a name="en-us_topic_0000001149807881_p152121542152218"></a><a name="en-us_topic_0000001149807881_p152121542152218"></a>audioType</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p9479411164814"><a name="en-us_topic_0000001149807881_p9479411164814"></a><a name="en-us_topic_0000001149807881_p9479411164814"></a><a href="#en-us_topic_0000001149807881_section92261857172218">AudioVolumeType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p45811752165910"><a name="en-us_topic_0000001149807881_p45811752165910"></a><a name="en-us_topic_0000001149807881_p45811752165910"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p1021294292216"><a name="en-us_topic_0000001149807881_p1021294292216"></a><a name="en-us_topic_0000001149807881_p1021294292216"></a>Audio stream type</p>
</td>
</tr>
</tbody>
</table>

**Return Values**

<a name="en-us_topic_0000001149807881_table621215425220"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row3212842112215"><th class="cellrowborder" valign="top" width="26.02%" id="mcps1.1.3.1.1"><p id="en-us_topic_0000001149807881_p521274272216"><a name="en-us_topic_0000001149807881_p521274272216"></a><a name="en-us_topic_0000001149807881_p521274272216"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="73.98%" id="mcps1.1.3.1.2"><p id="en-us_topic_0000001149807881_p1121214215221"><a name="en-us_topic_0000001149807881_p1121214215221"></a><a name="en-us_topic_0000001149807881_p1121214215221"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row12121442192216"><td class="cellrowborder" valign="top" width="26.02%" headers="mcps1.1.3.1.1 "><p id="en-us_topic_0000001149807881_p72128426221"><a name="en-us_topic_0000001149807881_p72128426221"></a><a name="en-us_topic_0000001149807881_p72128426221"></a>Promise&lt;number&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="73.98%" headers="mcps1.1.3.1.2 "><p id="en-us_topic_0000001149807881_p4212114210226"><a name="en-us_topic_0000001149807881_p4212114210226"></a><a name="en-us_topic_0000001149807881_p4212114210226"></a>Promise used to return the maximum volume</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getMaxVolume(audio.AudioVolumeType.MEDIA).then((data)=>
    console.log(`Media getMaxVolume successful callback`);
)
```

### getDevices\(DeviceFlag, AsyncCallback<AudioDeviceDescriptors\>\)<a name="en-us_topic_0000001149807881_section11536182020523"></a>

Obtains the audio devices of a specified flag. This method uses an asynchronous callback to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table8653191616249"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row165412169245"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p1665412161243"><a name="en-us_topic_0000001149807881_p1665412161243"></a><a name="en-us_topic_0000001149807881_p1665412161243"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="26.26%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p1765491672417"><a name="en-us_topic_0000001149807881_p1765491672417"></a><a name="en-us_topic_0000001149807881_p1765491672417"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p113067111209"><a name="en-us_topic_0000001149807881_p113067111209"></a><a name="en-us_topic_0000001149807881_p113067111209"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="48.65%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p765431682419"><a name="en-us_topic_0000001149807881_p765431682419"></a><a name="en-us_topic_0000001149807881_p765431682419"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row1654191652419"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p126549165241"><a name="en-us_topic_0000001149807881_p126549165241"></a><a name="en-us_topic_0000001149807881_p126549165241"></a>deviceFlag</p>
</td>
<td class="cellrowborder" valign="top" width="26.26%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p8654141622416"><a name="en-us_topic_0000001149807881_p8654141622416"></a><a name="en-us_topic_0000001149807881_p8654141622416"></a><a href="#en-us_topic_0000001149807881_section11285183164210">DeviceFlag</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p830651111019"><a name="en-us_topic_0000001149807881_p830651111019"></a><a name="en-us_topic_0000001149807881_p830651111019"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="48.65%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p10654131616248"><a name="en-us_topic_0000001149807881_p10654131616248"></a><a name="en-us_topic_0000001149807881_p10654131616248"></a>Audio device flag</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row16544162243"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p176541316122412"><a name="en-us_topic_0000001149807881_p176541316122412"></a><a name="en-us_topic_0000001149807881_p176541316122412"></a>callback</p>
</td>
<td class="cellrowborder" valign="top" width="26.26%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p1565461620244"><a name="en-us_topic_0000001149807881_p1565461620244"></a><a name="en-us_topic_0000001149807881_p1565461620244"></a>AsyncCallback&lt;<a href="#en-us_topic_0000001149807881_section5181155710523">AudioDeviceDescriptors</a>&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p2307711908"><a name="en-us_topic_0000001149807881_p2307711908"></a><a name="en-us_topic_0000001149807881_p2307711908"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="48.65%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p19654141672416"><a name="en-us_topic_0000001149807881_p19654141672416"></a><a name="en-us_topic_0000001149807881_p19654141672416"></a>Callback used to return the device list</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getDevices(audio.DeviceFlag.OUTPUT_DEVICES_FLAG, (err, value)=>{
   if (err) {
	   console.error(`failed to get getdevices ${err.message}`);
	   return;
   }
   console.log(`Media getDevices successful callback`);
})
```

### getDevices\(DeviceFlag\)<a name="en-us_topic_0000001149807881_section181733125210"></a>

Obtains the audio devices with a specified flag. This method uses a promise to return the execution result.

**Parameters**

<a name="en-us_topic_0000001149807881_table17655516132411"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row4655616192414"><th class="cellrowborder" valign="top" width="17.57%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p1465518164247"><a name="en-us_topic_0000001149807881_p1465518164247"></a><a name="en-us_topic_0000001149807881_p1465518164247"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="19.52%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p196551316172415"><a name="en-us_topic_0000001149807881_p196551316172415"></a><a name="en-us_topic_0000001149807881_p196551316172415"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p13161629902"><a name="en-us_topic_0000001149807881_p13161629902"></a><a name="en-us_topic_0000001149807881_p13161629902"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p17655616102417"><a name="en-us_topic_0000001149807881_p17655616102417"></a><a name="en-us_topic_0000001149807881_p17655616102417"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row13656111662415"><td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p2092935211270"><a name="en-us_topic_0000001149807881_p2092935211270"></a><a name="en-us_topic_0000001149807881_p2092935211270"></a>deviceFlag</p>
</td>
<td class="cellrowborder" valign="top" width="19.52%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p88719299489"><a name="en-us_topic_0000001149807881_p88719299489"></a><a name="en-us_topic_0000001149807881_p88719299489"></a><a href="#en-us_topic_0000001149807881_section11285183164210">DeviceFlag</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p12161129209"><a name="en-us_topic_0000001149807881_p12161129209"></a><a name="en-us_topic_0000001149807881_p12161129209"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p1692985222710"><a name="en-us_topic_0000001149807881_p1692985222710"></a><a name="en-us_topic_0000001149807881_p1692985222710"></a>Audio device flag</p>
</td>
</tr>
</tbody>
</table>

**Return Values**

<a name="en-us_topic_0000001149807881_table565618166249"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row19656151662410"><th class="cellrowborder" valign="top" width="26.02%" id="mcps1.1.3.1.1"><p id="en-us_topic_0000001149807881_p15656916152415"><a name="en-us_topic_0000001149807881_p15656916152415"></a><a name="en-us_topic_0000001149807881_p15656916152415"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="73.98%" id="mcps1.1.3.1.2"><p id="en-us_topic_0000001149807881_p365641616247"><a name="en-us_topic_0000001149807881_p365641616247"></a><a name="en-us_topic_0000001149807881_p365641616247"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row665681617243"><td class="cellrowborder" valign="top" width="26.02%" headers="mcps1.1.3.1.1 "><p id="en-us_topic_0000001149807881_p5673192162816"><a name="en-us_topic_0000001149807881_p5673192162816"></a><a name="en-us_topic_0000001149807881_p5673192162816"></a>Promise&lt;<a href="#en-us_topic_0000001149807881_section5181155710523">AudioDeviceDescriptors</a>&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="73.98%" headers="mcps1.1.3.1.2 "><p id="en-us_topic_0000001149807881_p765751610249"><a name="en-us_topic_0000001149807881_p765751610249"></a><a name="en-us_topic_0000001149807881_p765751610249"></a>Promise used to return the obtained device list</p>
</td>
</tr>
</tbody>
</table>

**Example**

```
audioManager.getDevices(audio.DeviceFlag.OUTPUT_DEVICES_FLAG).then((data)=>
    console.log(`Media getDevices successful callback`);
)
```

## AudioDeviceDescriptor<a name="en-us_topic_0000001149807881_section17427121913310"></a>

Describes audio devices.

<a name="en-us_topic_0000001149807881_table5702164473415"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row97021944203413"><th class="cellrowborder" valign="top" width="17.378262173782623%" id="mcps1.1.5.1.1"><p id="en-us_topic_0000001149807881_p1610322561817"><a name="en-us_topic_0000001149807881_p1610322561817"></a><a name="en-us_topic_0000001149807881_p1610322561817"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="21.547845215478453%" id="mcps1.1.5.1.2"><p id="en-us_topic_0000001149807881_p177024446340"><a name="en-us_topic_0000001149807881_p177024446340"></a><a name="en-us_topic_0000001149807881_p177024446340"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="7.519248075192481%" id="mcps1.1.5.1.3"><p id="en-us_topic_0000001149807881_p1103172518188"><a name="en-us_topic_0000001149807881_p1103172518188"></a><a name="en-us_topic_0000001149807881_p1103172518188"></a>Mandatory</p>
</th>
<th class="cellrowborder" valign="top" width="53.554644535546444%" id="mcps1.1.5.1.4"><p id="en-us_topic_0000001149807881_p570274410345"><a name="en-us_topic_0000001149807881_p570274410345"></a><a name="en-us_topic_0000001149807881_p570274410345"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row1770204412344"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p116764916367"><a name="en-us_topic_0000001149807881_p116764916367"></a><a name="en-us_topic_0000001149807881_p116764916367"></a>deviceRole</p>
</td>
<td class="cellrowborder" valign="top" width="21.547845215478453%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p1710432543618"><a name="en-us_topic_0000001149807881_p1710432543618"></a><a name="en-us_topic_0000001149807881_p1710432543618"></a><a href="#en-us_topic_0000001149807881_section380038142619">DeviceRole</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.519248075192481%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p14435512251"><a name="en-us_topic_0000001149807881_p14435512251"></a><a name="en-us_topic_0000001149807881_p14435512251"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="53.554644535546444%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p8703114411348"><a name="en-us_topic_0000001149807881_p8703114411348"></a><a name="en-us_topic_0000001149807881_p8703114411348"></a>Audio device role</p>
</td>
</tr>
<tr id="en-us_topic_0000001149807881_row370314447340"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.1.5.1.1 "><p id="en-us_topic_0000001149807881_p32441814173618"><a name="en-us_topic_0000001149807881_p32441814173618"></a><a name="en-us_topic_0000001149807881_p32441814173618"></a>deviceType</p>
</td>
<td class="cellrowborder" valign="top" width="21.547845215478453%" headers="mcps1.1.5.1.2 "><p id="en-us_topic_0000001149807881_p654132923620"><a name="en-us_topic_0000001149807881_p654132923620"></a><a name="en-us_topic_0000001149807881_p654132923620"></a><a href="#en-us_topic_0000001149807881_section11727420122710">DeviceType</a></p>
</td>
<td class="cellrowborder" valign="top" width="7.519248075192481%" headers="mcps1.1.5.1.3 "><p id="en-us_topic_0000001149807881_p44475515256"><a name="en-us_topic_0000001149807881_p44475515256"></a><a name="en-us_topic_0000001149807881_p44475515256"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="53.554644535546444%" headers="mcps1.1.5.1.4 "><p id="en-us_topic_0000001149807881_p207031344133411"><a name="en-us_topic_0000001149807881_p207031344133411"></a><a name="en-us_topic_0000001149807881_p207031344133411"></a>Audio device type</p>
</td>
</tr>
</tbody>
</table>

## AudioDeviceDescriptors<a name="en-us_topic_0000001149807881_section5181155710523"></a>

<a name="en-us_topic_0000001149807881_table169751229266"></a>
<table><thead align="left"><tr id="en-us_topic_0000001149807881_row169757224268"><th class="cellrowborder" valign="top" width="19.7%" id="mcps1.1.3.1.1"><p id="en-us_topic_0000001149807881_p19975182202612"><a name="en-us_topic_0000001149807881_p19975182202612"></a><a name="en-us_topic_0000001149807881_p19975182202612"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="80.30000000000001%" id="mcps1.1.3.1.2"><p id="en-us_topic_0000001149807881_p109751622132611"><a name="en-us_topic_0000001149807881_p109751622132611"></a><a name="en-us_topic_0000001149807881_p109751622132611"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001149807881_row169751322182613"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.1.3.1.1 "><p id="en-us_topic_0000001149807881_p139751522182616"><a name="en-us_topic_0000001149807881_p139751522182616"></a><a name="en-us_topic_0000001149807881_p139751522182616"></a>Device property queue</p>
</td>
<td class="cellrowborder" valign="top" width="80.30000000000001%" headers="mcps1.1.3.1.2 "><p id="en-us_topic_0000001149807881_p597532272616"><a name="en-us_topic_0000001149807881_p597532272616"></a><a name="en-us_topic_0000001149807881_p597532272616"></a>A queue of <strong id="en-us_topic_0000001149807881_b12615715612"><a name="en-us_topic_0000001149807881_b12615715612"></a><a name="en-us_topic_0000001149807881_b12615715612"></a>AudioDeviceDescriptor</strong>, which is read-only.</p>
</td>
</tr>
</tbody>
</table>

