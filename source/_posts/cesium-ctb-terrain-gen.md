## 下载tif
### 可用网站
- [AIRBUS worldDEM-terrasar](https://worlddem-database.terrasar.com/)
- [srtm30m](http://dwtkns.com/srtm30m/)
- [srtm90m](http://dwtkns.com/srtm/)
- [ESA哥白尼计划](https://scihub.copernicus.eu/dhus/#/home)
- [USGS-earthexplorer](https://earthexplorer.usgs.gov/)
- [USGS-NED-1m-db in USA](https://prd-tnm.s3.amazonaws.com/index.html?prefix=StagedProducts/Elevation/1m/IMG/)
- [USGS-nationalmap-3DEP](https://viewer.nationalmap.gov/basic/?basemap=b1&category=ned,nedsrc&title=3DEP%20View)
- [earth observing system-landviewer](https://eos.com/landviewer/?lat=34.26368&lng=109.19109&z=11)
- [NASA阿拉斯加卫星设施](https://search.asf.alaska.edu)
- [NASA青藏高原8m](https://nsidc.org/data/highmountainasia/data-summaries)
- [AW3D30](https://www.eorc.jaxa.jp/ALOS/en/aw3d30/index.htm)

## 处理tif
使用ArcMap QGIS等工具，合成tif瓦片，设置pixeltype数据类型float为int，再设置nodata值为0。

## 生成terrain
### ctb下载编译
### 使用ctb生成terrain文件
注：生成时间长，数据量大。