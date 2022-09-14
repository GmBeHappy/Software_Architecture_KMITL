# Architectural Patterns/Styles

## Authors

[@gmbehappy](https://www.github.com/gmbehappy) วิชยุตม์ เกิดไชย 63010881


## Audacity

Audacity คือ **crossplatform multitrack audio editor and recorder**.

### architectural patterns/styles

![image](https://www.aosabook.org/images/audacity/Layers.png)

รูปแบบสถาปัตยกรรมที่ Audacity ใช้คือรูปแบบ **Layer architectural** 

**Layer ส่วนที่ติดต่อกับผู้ใช้งาน (GUI)** ใช้ Lib wxWidgets (GUI components in a cross-platform way) โดยในส่วน GUI ถูกแบ่งออกมาหลายๆส่วน เช่น Blockfiles, ShuttleGUI โดยในส่วนนี้ทำหน้าที่รับคำสั่งและแสดงผลต่อผู้ใช่งาน

**Layer ส่วนที่ติดต่อกับ Hardware** ใช้ Lib PortAudio (provides a low-level audio interface in a cross-platform way) โดยในส่วนนี้ทำหน้าที่ติดต่อกับ OS เพื่อใช้งาน Interface ต่างๆของ Hardwawre

### Quality attribute scenarios

#### Scenario 1: การเพิ่มเสียงให้กับไฟล์เสียง
```
Source(ผู้ใช้งาน) -> Stimulus(ต้องการเพิ่มเสียงในไฟล์เสียง) -> Environment() -> Response() -> Response Measure()
```

```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

## Matplotlib

Matplotlib คือ ไลบรารี่ที่ครอบคลุม creating static, animated, and interactive visualizations ด้วย Python.

### architectural patterns/styles

![image](https://miro.medium.com/max/700/1*-AodXsh3AIymW83WLPwYqw.png)

รูปแบบสถาปัตยกรรมที่ Matplotlib ใช้คือรูปแบบ **Layer architectural** 

**Scripting layer** เป็น layer ที่ใช้สำหรับการเขียนโปรแกรม โดยในส่วนนี้จะเป็นการเขียนโปรแกรมเพื่อใช้งานกับ Matplotlib โดยจะเขียนโปรแกรมเพื่อสร้างกราฟ และส่วนนี้จะเป็นส่วนที่ผู้ใช้งานสามารถเขียนโปรแกรมเพื่อใช้งานกับ Matplotlib ได้

**Artist Layer** เป็น layer ที่ช่วยให้ควบคุมและปรับจูนของ figure เช่น spines, tick direction, tick label size, tick label font, tick color. โดยในส่วนนี้จะเป็นการสร้าง figure และส่วนนี้จะเป็นส่วนที่ผู้ใช้งานสามารถเขียนโปรแกรมเพื่อใช้งานกับ Matplotlib ได้

**Backend Layer** เป็น layer ที่ใช้สำหรับการแสดงผลของ figure โดยในส่วนนี้จะเป็นการแสดงผลของ figure ที่สร้างขึ้นมา

### Quality attribute scenarios

#### Scenario 1: การเพิ่มเสียงให้กับไฟล์เสียง
```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

## Jitsi

Jitsi คือ open-source projects สำหรับการสร้าง video conference และ chat โดยใช้ WebRTC และ XMPP ซึ่งเป็นโปรเจคที่เปิดโอกาสให้ผู้ใช้งานสามารถเข้ามาเพิ่มเติม แก้ไข และปรับปรุงโปรเจคได้

### architectural patterns/styles

![image](https://raw.githubusercontent.com/jitsi/handbook/master/docs/assets/ArchitectureDiagram.png)

รูปแบบสถาปัตยกรรมที่ Jitsi ใช้คือรูปแบบ **Layer architectural**

**Jitsi Meet** WebRTC compatible JavaScript application that uses Jitsi Videobridge to provide high quality, scalable video conferences. Build upon React and React Native

**Jitsi Videobridge (jvb)** WebRTC compatible server designed to route video streams amongst participants in a conference

**Jitsi Conference Focus (jicofo)** server-side focus component used in Jitsi Meet conferences that manages media sessions between each of the participants and the videobridge

**Jitsi Gateway to SIP (jigasi)** server-side application that allows regular SIP clients to join Jitsi Meet conferences

**Jitsi Broadcasting Infrastructure (jibri)** tools for recording and/or streaming a Jitsi Meet conference that works by launching a Chrome instance rendered in a virtual framebuffer and capturing and encoding the output with ffmpeg

### Quality attribute scenarios

#### Scenario 1: การเพิ่มเสียงให้กับไฟล์เสียง
```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

```
Source() -> Stimulus() -> Environment() -> Response() -> Response Measure()
```

