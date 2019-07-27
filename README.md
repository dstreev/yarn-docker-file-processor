# yarn-image-processor
Process Images in YARN via Docker Containers

Usage:
======

### Unmanaged mode

$ bin/hadoop jar /usr/hdp/current/hadoop-yarn-client/hadoop-yarn-applications-unmanaged-am-launcher.jar Client -classpath yarn.docker.image.processor-1.0-SNAPSHOT.jar -cmd "java com.streever.hadoop.yarn.docker.image.processor.ApplicationMaster ... /bin/date 2"

### Managed mode

$ bin/hadoop fs -copyFromLocal yarn.docker.file.processor-1.0-SNAPSHOT.jar /apps/yarn-docker/yarn.docker.file.processor-1.0-SNAPSHOT.jar

$ bin/hadoop jar yarn.docker.file.processor-1.0-SNAPSHOT.jar com.streever.hadoop.yarn.docker.file.processor.Client ... /bin/date 2 /apps/yarn-docker/yarn.docker.image.processor-1.0-SNAPSHOT.jar
