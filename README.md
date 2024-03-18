# esp32-Marauder-mod-CYD
This is a tutorial on how you mod esp32 marauder
if you want to learn how to port marauder to your cyd devices go to [Marauder tutorial cyd-Cheap yellow display](https://github.com/smoochiee/MARAUDER-FOR-CYD---CHEAP-YELLOW-DISPLAY)
# SPLASH SCREEN OF MARAUDER
+ Repalcing original Splash screen.

  - ![marauder3L](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/178c255e-0ada-4f9d-b014-b0ef4215e69f)

- To This (or any jpeg picture format)

  - ![360_F_393641217_x8EFoYlz75eWnW8NJgCHjE766gdM5xys](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/a7e6372d-21fa-41b7-be60-9a2f8dd53cb5)

 ## DOWNLOADING AND RESIZING
1. Download some `.jpeg` format on internet OR make your own. in this tutorial i will use
- ![360_F_393641217_x8EFoYlz75eWnW8NJgCHjE766gdM5xys](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/a7e6372d-21fa-41b7-be60-9a2f8dd53cb5)

2. Right click your downloaded or made `jpeg` and select `Edit with Paint 3d`
![3d](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/f4b0fadb-948b-4885-8e27-9d6f74b402de)

3. Inside Paint 3d Click `Canvas` tab on top then on the right side panel set width `240px` and height `320px` uncheck lock aspect ratio.

![canvas tab](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/f424f450-5393-4b4e-a4d2-a92a1a623c9c)

4. Saving edited jpeg Click Menu on left corner save as then `click image` then  `save as 2D-jpeg` any name is okay
   
  - ![save](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/b3f1880f-912a-4ae1-9d65-5a92ab07e333)
  - ![as](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/d775353b-99f7-4065-a5f8-0f0c0e8d9de3)

## CONVERTING JPEG TO HEX 

1. Open your Favorite browser then go to [Hex converter](https://tomeko.net/online_tools/file_to_hex.php?lang=en) click `choose file` and add you `jpeg`
![hex](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/e499fb43-6bed-4843-ba92-b8804b979772)

2. Click `Copy output to clipboard`

![o](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/ddca97e1-f225-4084-9fdd-eab65c21e088)


3. Open `esp32 marauder folder` from your downloaded source code then open `assets.h` file with your note pad or [note++](https://notepad-plus-plus.org/) , if you dont know go to [marauder tutorial](https://github.com/smoochiee/MARAUDER-FOR-CYD---CHEAP-YELLOW-DISPLAY) 
    
![assets](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/7ee0bed5-0c88-4f05-8665-ef4b8a3aa6a6)


4. On assets.h file go to line 210 and delete from `Oxff` to line 1059 `0xD9` the ouput should look like this

![de](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/ccc12157-da49-4536-bae1-c242cf91bf95)


5. Paste your output from converted jpeg to hex on (#2 instruction)  to   static const uint8_t MarauderTitle[] PROGMEM = {`PASTE HEX HERE`};  

![l](https://github.com/smoochiee/esp32-Marauder-mod-CYD/assets/30816448/435c3a75-b476-44f6-859b-4444533ff4ad)

6. Save then open `esp32_marauder.ino` then compile.








