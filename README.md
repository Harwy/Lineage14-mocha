# Mocha Flash
## Lineage OS 14
小米平板1在2014年5月15日推出的一款智能安卓平板电脑，由英华达代工生产，多彩后壳的生产商为富士康。NVIDIA Tegra K1处理器，192核心的NVIDIA Kepler™架构 GPU。基于Android深度定制MIUI操作系统。

搭载的 NVIDIA Tegra K1 四核 2.2GHz ARMCortex-A15处理器，放在今天仍然可以担当大任。但是受限于2GB内存和Android4.4，使得很多APP不能在该系统内安装或使用。

Lineage OS是国外民间大神开发的基于原生Android第三方OS，其v14版本基于Android7.x，可以大幅提升小米平板的流畅性以及应用的适配能力。

### 所需文件
附在/lineage14文件夹，部分过大文件需要在百度网盘或自行搜索下载  
这里附上的是我成功安装的文件，有部分文件可以互相替换，请自行测试，若变成砖头，本作者不负任何责任
> 第三方Recovery签名版：[miuies_TWRP_mocha_2.7.1_signed](lineage14/mipadrecovery/miuies_TWRP_mocha_2.7.1_signed.zip)  
> Recovery新版本：[twrp_3.1.0_mocha_cn.zip](lineage14/mipadrecovery/twrp_3.1.0_mocha_cn.zip)  
> 合并分区工具：[Repartition_MI_Pad_1_2GB_zardMi3](lineage14/分区工具/Repartition_MI_Pad_1_2GB_zardMi3.zip)  
> OS：lineage-14.1-20170911-UNOFFICIAL-mocha PS:[该文件过大，请在网盘下载](https://pan.baidu.com/s/1qXU7DVm) 密码:[hide] grck[/hide]  
> Root工具：[SuperSU](lineage14/root-solve-net/SR5-SuperSU-v2.82-SR5-20171001224502.zip)  
> 解决无法连接网络：[captivemgr](lineage14/root-solve-net/captivemgr-release-2.4.apk)

### 安装过程
1. 复制以上列举的所需文件至平板SD卡
2. 第三方Recovery签名版下载
   * 修改[miuies_TWRP_mocha_2.7.1_signed](lineage14/mipadrecovery/miuies_TWRP_mocha_2.7.1_signed.zip)为`update.zip`，并复制到平板SD卡根目录下
   * 平板接上电源，关机
   * 按住`电源键`和`音量+`开机，等白色的Mi图标消失后松开`电源键`，保持按住`音量+`，直到进去小米的Recovery
   * 保证进入的为`系统一`，若不是则选择进入系统一，重启后重复以上步骤
   * 选择`将update.zip安装到系统一`
   * 安装完成后，不要直接重新启动，选择关机，重复上述步骤进入Recovery
   * 看到TWRP则成功，若失败则重复关机，进入Recovery
3. 更新最新版TWRP
   * 在TWRP下进入`Install`选择路径至[twrp_3.1.0_mocha_cn.zip](lineage14/mipadrecovery/twrp_3.1.0_mocha_cn.zip)，安装，
   * 关机，重新进Recovery
4. 合并分区
    * 清除数据  
    TWRP下点`wipe`-`Advanced Wipe`，把`Dalvik/ART Cache` ，`System`，`Cache`，`Data`都选上，如果想彻底全新安装，把`Internal Storage`也选上（注意之前备份数据），然后`Swipe to Wipe`
5. 安装 Lineage OS
   * TWRP下选择`Install`，选择`lineage-14.1-20170911-UNOFFICIAL-mocha`，下方滑动刷机
6. 安装Root工具SuperSU
    * TWRP下`Install`安装[SuperSU](lineage14/root-solve-net/SR5-SuperSU-v2.82-SR5-20171001224502.zip)
7. 安装captivemgr
    * 进入Lineage OS，安装正常apk一样安装
    * SuperSU给权限
    * 按照app内指示将验证网络的原谷歌服务器切换

接下来，就可以开心的玩耍了。可以看到在安装了豌豆荚，QQ HD，腾讯视频，谷歌中文输入法下，内存占用0.98GB/1.7GB，但在使用内存占用严重的APP（UC浏览器）时还是十分卡顿的，毕竟内存限制了软件的狂放-_-！

### 效果展示
<img src="https://i.loli.net/2020/04/17/IQB1iMNa7FO65SJ.png" width="400" alt="主界面1.png" align="center">  
  
主界面可以看到是原生的Android系统，还是十分简洁的。  

<img src="https://i.loli.net/2020/04/17/i7ZemCJpGhzDqwL.png" width="400" alt="主界面2.png" align="center">

现在很多的音乐软件下载的音乐都是加密的了，需要自家播放器，SD卡内只剩下这么一首歌23333  

<img src="https://i.loli.net/2020/04/17/fJqKrOpjh7DGHFL.png" width="400" alt="🔋电池用量.png" align="center">

昨晚刷机成功，看了2集柯南，然后睡醒到现在11：20，还剩42%，待机能力大幅提升！！！  
原本的Android4.4+MIUI9实在吃不消，堪称吃电小老虎，一整天待机就待没了  

<img src="https://i.loli.net/2020/04/17/QVvP3rAFW9GgenT.png" width="400" alt="系统信息.png" align="center">

系统信息下可以看到，Android版本为7.1.2，很多软件都能装啦！不过还是要爱惜一点，毕竟老年机了，还是不要要求太高，好好做好“买后爱奇艺”就好了，虽然本人只看B站和腾讯视频(笑)

### 参考文献
1. [xda论坛-LineageOS贴](https://forum.xda-developers.com/mi-pad/development/unofficial-lineageos-14-1-xiami-mipad-t3557616)
2. [简书-小米平板刷lineage OS 14.1](https://www.jianshu.com/p/cc9d93eb909c)
3. [小米论坛-小米平板1安装lineage14.1详细](https://www.xiaomi.cn/post/1356206)
4. [小米论坛-小米平板1入坑Lineage OS 14小白教程](https://www.xiaomi.cn/post/1356206) && 该贴附上部分下载所需文件 https://pan.baidu.com/s/1qXU7DVm 密码:[hide] grck[/hide]
1. [酷安-CaptiveMgr清除x和! 2.4](https://www.coolapk.com/apk/tech.evlsoc.captivemgr)
2. [SuperSU](https://download.chainfire.eu/1220/SuperSU/SR5-SuperSU-v2.82-SR5-20171001224502.zip)

