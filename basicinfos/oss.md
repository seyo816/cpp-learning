nohup java -Dskip_exist_file=false -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties start > /disk/oss/logs/ossimport2.log 2>&1 &
java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties  submit /disk/oss/local_test.cfg

java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties stat detail


ps -ef |grep ossimport2

java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties clean sz-pics-10003
java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties clean sz-pics-10164

java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties clean sz_pics_10164

java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties clean local_test

java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties  submit /disk/oss/sz-pics-10003.cfg
java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties  submit /disk/oss/sz-pics-10004.cfg
java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties  submit /disk/oss/sz-pics-10164.cfg

java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties  submit /disk/oss/sz_pics_10164.cfg


java -jar /disk/oss/bin/ossimport2.jar -c /disk/oss/conf/sys.properties  retry /disk/oss/sz_pics_10164.cfg
