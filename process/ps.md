* 어떤 프로세스에서 가장 많은 메모리를 사용하는지 확인 ( 사용량이 많은 프로세스 10 개 )

  ps -eo user,pid,rss,size,vsize,pmem,pcpu,time,cmd --sort -rss | head -n 11
---------------------------------------------------------------------------------------------------------------
* 프로세스 한번에 kill

  ps -ef | grep find | awk {'print $2'}

  ps -ef | grep find | awk {'print $2'} | xargs kill -9
