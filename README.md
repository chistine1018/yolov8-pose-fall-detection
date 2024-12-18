# yolov8-pose-fall-detection


## 參考
https://github.com/zhahoi/yolov8-pose-fall-detection (yolov8 pose fall detection)  
https://blog.csdn.net/qq_41572755/article/details/143047191 (yolov8 pose fall detection)


Clone 後build folder先砍掉，自己照下術步驟重build

事前準備下載CMake (3.31.1)  
```
$ cmake /V
```

https://cmake.org/download/ 官網  
https://blog.csdn.net/qq_42598221/article/details/121952160 教學

事前準備下載opencv (3.4.2)  
https://opencv.org/releases/ 官網  
https://blog.csdn.net/maizousidemao/article/details/81474834 教學  

事情準備下載Visual Studio (2022)  
https://visualstudio.microsoft.com/zh-hans/ 官網  
https://blog.csdn.net/weixin_45725336/article/details/130754036?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_utm_term~default-0-130754036-blog-104966786.235%5Ev43%5Epc_blog_bottom_relevance_base1&spm=1001.2101.3001.4242.1&utm_relevant_index=3 教學 image

事前準備下載Eigen  
https://blog.csdn.net/OOFFrankDura/article/details/103586893


1. 開啟 X64 Native Tools Command Prompt for VS 2022

2. cd C:\Users\user\Downloads\OtherProject\DeepLearning\ncnn_windows_fall_detect_byAnson --> 到對應位置

3. mkdir build --> 建立一個資料夾等等用來放置編譯過後的相關檔案

4. cd build --> 進入資料夾

5. cmake -G "Visual Studio 17 2022" .. --> 指定cmake編譯工具 .. 是為了回上一層找到CMakeList.txt

6. 可能需要調整CMakeList中的opencv 位置 (調整成自己的)

7. msbuild yolov8-pose.sln /p:Configuration=Release --> 建置可執行exe檔案

8. yolov8-pose.exe.exe image test.jpg --> 成功預測跌倒圖片
9. yolov8-pose.exe.exe video test.mp4 --> 成功預測跌倒影片
10. yolov8-pose.exe camera -0 --> 開啟鏡頭

![output2](https://github.com/user-attachments/assets/0bab4251-be66-4f4c-94bc-d3d321074144)

![image](https://github.com/user-attachments/assets/5b4ef50e-78fb-43d9-a8de-3df7c2060948)

![image](https://github.com/user-attachments/assets/4fa8a2ae-0da2-422d-a205-08f0dccd214d)

![image](https://github.com/user-attachments/assets/6512c24d-fccc-4cae-b26b-8a994a9489a4)

