## s6笔记本，u盘启动，通过菜单选择是否开启smt

||关smt|开smt|
|-----|-----|-----|
|pcmark|9609|10998|
|3dmark|3036|3713|
|gfxbench|![](../picture/s6_nosmt_gfxbench1.png)|![](../picture/s6_smt_gfx1.png)|

***

## 清华同方t45笔记本，u盘启动，通过菜单选择是否开启smt

||关smt|开smt|
|-----|-----|-----|
|pcmark|7939|7952|
|3dmark|1855|2233|
|gfxbench|![](../picture/t45_nosmt_gfx1.png)|![](../picture/t45_smt_gfx1.png)|

***

## 清华同方台式机精锐X500-B107，u盘启动，通过菜单选择是否开启smt

||关smt|开smt|
|-----|-----|-----|
|pcmark|6873|6790|
|3dmark|4031 有异常亮点  ![](../picture/b107_nosmt_3dmarklight.png)|4032 正常  ![](../picture/b107_smt_pcmarknormal.png)|
|gfxbench|![](../picture/b107_nosmt_gfx1.png)|![](../picture/b107_smt_gfx1.png)|

***

## s1笔记本，硬盘启动，通过向内核传递参数选择是否开启smt

### 内核4.18
||关smt|开smt|
|-----|-----|-----|
|pcmark|9470|8741|
|3dmark|3434|3402|
|gfxbench|![](../picture/418-opensmp-closesmt-gfxbench-part1.png)|![](../picture/418-opensmpsmt-gfxbench-part1.png)|

### 内核4.19
||关smt|开smt|
|-----|-----|-----|
|pcmark|9610|10045|
|3dmark|3163|3325|
