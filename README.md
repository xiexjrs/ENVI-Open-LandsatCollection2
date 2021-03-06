# ENVI-Open-LandsatCollection2
A small plug-in developed based on ENVI5.3.1/IDL8.5.1 to open Landsat Collection 2 data released by USGS

# 工具中文说明
开发背景：Landsat Collection2 Level 2 数据是USGS在2020年基于Level1的数据以及其他辅助数据制作的地表温度以及反射率数据产品，可直接用于定性分类、定量评估以及时间序列分析等遥感实践，减少了预处理辐射矫正环节，大大提高了处理效率。所以，每到大学最后一个学期，有不少毕业班同学咨询该数据在ENVI5.3中如何使用的问题，为方便大家，编写并分享此插件。

## 插件下载：

  For ENVI5.3.1+： https://github.com/xiexjrs/ENVI-Open-LandsatCollection2/blob/main/Open_LandsatC2.sav
	
  For ENVI5.3： https://github.com/xiexjrs/ENVI-Open-LandsatCollection2/blob/main/ENVI5.3-Open-LandsatCollection2.zip

  Github Code: https://github.com/xiexjrs/ENVI-Open-LandsatCollection2.git

## 工具介绍	
1. 功能：
	通过ENVI打开USGS发布的Landsat Collection 2  数据（Level 2已经过定标和大气校正）。
	
2. 测试/适用平台：
	在ENVI5.3.1/IDL8.5.1上测试可用，一般适用于ENVI5.3.1及以上版本。
	
3. 测试/数据：
	在USGS/aliyun AI Earth等平台下载的Landsat Collection2 数据
	（如LC08_L2SP_129044_20150104_20200910_02_T1.tar;LC09_L2SP_136044_20220217_20220225_02_T1.tar）。

## 工具安装与使用
1. 安装：
	将压缩包中的Open_LandsatC2.sav文件拷贝到ENVI指定扩展目录下extensions文件夹中即可。
	
2. 使用：
	
	(1) 拷贝完成后，重启ENVI，双击右下角Open Landsat Collection 2插件;
	
	(2) 在弹出对话框中，选择数据目录下的_MTL.json文件（如LC08_L2SP_129044_20150104_20200910_02_T1_MTL.json）；
	
	(3) 如果没报错，工具自动加载Level 2缩放后的地表反射率影像集、地表温度影像和QA_Pixel质量影像或Level 1定标后的数据。
	
	(4) 如果报Json解析错误，请下载源码，在UTF-8编码格式下重新(编译调试无误后)构建项目，生成Open_LandsatC2.sav，并将其重新拷贝到相应目录。
	
3. 免责声明：
	本工具基于ENVI5.3.1/IDL8.5.1二次开发，不能保证与所有的软硬件系统完全兼容，在使用过程中遇到报错，可联系xiexj@ecut.edu.cn。
	对任何原因在使用此工具时可能对用户自己或他人造成的任何形式的损失和伤害不承担责任，如有侵权，可联系删除。

## 工具更新说明
1. ENVI_Read_MTL_json-v0.1 

  This version only supports the reading of the L2SP level data from Landsat 08/09 OLI_TIRS.	
  该版本只支持Landsat_08/09 OLI_TIRS的“L2SP”级别数据的读取。	
	
2. ENVI-Open-LandsatCollection2-v0.2 

  This version supports the reading of the L1TP/L2SP level data from Landsat TM/ETM/OLI_TIRS.	
  该版本同时支持Landsat_TM/ETM/OLI_TIRS的“L2SP”和“L1TP”级别数据的读取。

3. ENVI-Open-LandsatCollection2-v0.3 

  This version supports the reading and scaling of panchromatic channel from the Landsat ETM+/OLI Collection2 L1TP Data.	
  该版本同时支持Landsat_ETM/OLI “Collection2 L1TP” 全色通道数据的读取。
