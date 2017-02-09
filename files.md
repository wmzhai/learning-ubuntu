# 文件相关处理

$ FULLPATH=/user/work/project/backup.tar.gz

## 取目录部分

```
$ dirname $FULLPATH
-> /user/work/project
或
$ echo ${FULLPATH%/*}  
-> /user/work/project
```

## 取文件名称
```
$ basename $FULLPATH  
-> backup.tar.gz
或者
$ echo FILE=${FULLPATH##*/}
-> backup.tar.gz
```

## 取基本名
```
$ FILE=${FULLPATH##*/}
$ echo ${FILE%%.*}
->
```

## 取最短扩展名
```
$ echo ${FILE##*.}
-> gz
```

## 取最长扩展名
```
$ echo ${FILE#*.}
-> tar.gz
```
