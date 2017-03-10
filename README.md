Prepare folder, you must download MTK source code from internet and unpack into this place.
Make folder for source code of AOSP MTK
```
mkdir alps
cd alps
```
initialize REPO with sources 
```
repo init -u git@github.com:SnowCat6/DOOGEE-X5PRO-MTK-AOSP.git
repo sync -j4
```
make AOSP android 7.x - automatic detection settings
for x32 AOSP
```
. build/envsetup.sh
lunch full_X5PROx32-user && make -j4
```
for x64 AOSP
```
. build/envsetup.sh
lunch full_X5PROx64-user && make -j4
```
Good like!


If you have less than 15GB RAM you must execute script before any build step
```
export JACK_SERVER_VM_ARGUMENTS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx3500m"
```
