* 메모리 캐시 정리

  echo 2 > sudo /proc/sys/vm/drop_caches
  sysctl -w vm.drop_caches=2
----------------------------------------------------------------------
* Crontab에 등록 후 주기적으로 캐시 비우기

  0 * * * * sync && sudo echo 3 > sudo /proc/sys/vm/drop_caches
