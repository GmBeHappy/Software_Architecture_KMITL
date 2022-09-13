# Architectural Patterns/Styles

## Audacity

Audacity คือ **crossplatform multitrack audio editor and recorder**.

### architectural patterns/styles

![image](https://www.aosabook.org/images/audacity/Layers.png)

รูปแบบสถาปัตยกรรมที่ Audacity ใช้คือรูปแบบ **Layer architectural** 

**Layer ส่วนที่ติดต่อกับผู้ใช้งาน (GUI)** ใช้ Lib wxWidgets (GUI components in a cross-platform way) โดยในส่วน GUI ถูกแบ่งออกมาหลายๆส่วน เช่น Blockfiles, ShuttleGUI โดยในส่วนนี้ทำหน้าที่รับคำสั่งและแสดงผลต่อผู้ใช่งาน

**Layer ส่วนที่ติดต่อกับ Hardware** ใช้ Lib PortAudio (provides a low-level audio interface in a cross-platform way) โดยในส่วนนี้ทำหน้าที่ติดต่อกับ OS เพื่อใช้งาน Interface ต่างๆของ Hardwawre


### Quality attribute scenarios

```

```
## Authors

- [@gmbehappy](https://www.github.com/gmbehappy) วิชยุตม์ เกิดไชย 63010881

