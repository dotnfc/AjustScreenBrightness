c# 多种方法调整屏幕亮度 
=====================
## 方法一: 使用网上常说的 Gdi32.dll 下的 SetDeviceGammaRamp (修改系统Gamma)
## 方法二: 使用MSDN上的 dxva2.dll SetMonitorBrightness
## 方法三: 使用 C:\Windows\System32\DriverStore\FileRepository\igdlh64.inf_amd64_neutral_3daeca3838e011e0\igfxDHLib.dll (这是驱动的文件,不同机器有自己对应的驱动文件)
`注意事项` 该方法使用时请注意好参数的范围,比如说把对比度设置太低时屏幕会完全黑掉 什么都看不到,然后你就不能直接把对比度调回来了.
<br />
<hr />
完善一下，以解决 Thinkpad T550 上集成显卡无法调亮度的问题：FN+F5/F6, 或者 Win10/Win11 系统控制面板。
NVIDIA GeForce 940M + Intel HD Graphics 5500

基于 igfxDHLib.dll 的接口。
