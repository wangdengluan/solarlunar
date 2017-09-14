# solarlunar
[![Build Status](https://api.travis-ci.org/nosixtools/solarlunar.svg?branch=master)](https://api.travis-ci.org/nosixtools/solarlunar)

##### 1.阳历和阴历相互转化（支持1900~2049年）
##### 2.节假日计算

## 快速开始
#### 下载和安装
	go get -u github.com/wangdengluan/solarlunar
#### 创建 solarlunar.go  阳历和阴历转化
```
package main 


import (
	"github.com/wangdengluan/solarlunar" 
	"fmt"
)


func main() {
	solarDate := "1990-05-06"
	fmt.Println(solarlunar.SolarToChineseLuanr(solarDate))
	fmt.Println(solarlunar.SolarToSimpleLuanr(solarDate))
	
	lunarDate := 2017-07-17 00:00:00 +0000 UTC
	fmt.Println(solarlunar.LunarToSolar(lunarDate, false))
}

```
#### 创建 festival.go 节假日计算
```
package main


import (
"fmt"
"github.com/wangdengluan/solarlunar/festival"
)

func main() {
	festival := festival.NewFestival("./festival.json")
	fmt.Println(festival.GetFestivals("2017-08-28"))
	fmt.Println(festival.GetFestivals("2017-05-01"))
	fmt.Println(festival.GetFestivals("2017-04-05"))
	fmt.Println(festival.GetFestivals("2017-10-01"))
	fmt.Println(festival.GetFestivals("2018-02-15"))
	fmt.Println(festival.GetFestivals("2018-02-16"))
}
