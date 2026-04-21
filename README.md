## Release
```bash
COPYFILE_DISABLE=1 zip -r ../kodi/skin.apollo/skin.apollo-0.1.0.zip skin.apollo -x "*.DS_Store*"

// verify no meta files within
unzip -l skin.apollo/skin.apollo-0.1.0.zip

printf $(md5 -q addons.xml) > addons.xml.md5

cat -e addons.xml.md5

git add --all && git commit -m "fix" && git push
```