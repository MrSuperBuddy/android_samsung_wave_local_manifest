# android_samsung_wave_local_manifest
updated samsung wave manifest
# install and build custom rom
cd ~
mkdir wave
cd wave
repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0
cd .repo
wget https://github.com/MrSuperBuddy/android_samsung_wave_local_manifest/raw/local_manifest.xml
cd ..
repo sync -j8
cd vendor/cm/
./get-prebuilts
cd ../../
. build/envsetup.sh
brunch wave

device name is wave so the build invocation can be brunch wave
