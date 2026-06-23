* 파일 내용 일괄 변경

  sed -i 's/기존 내용/변경할 내용/g' abc.php
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
*  여러개 변경 시

   sed -i 's/기존 내용/변경할 내용/g; s/기존 내용/변경할 내용/g' abc.php
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
* 해당 내용이 포함 된 줄을 삭제

  sed -i '/삭제 할 내용/d' abc.txt
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
* 특정 라인 문자열 추가

  sed -i'' -r -e "/Please Put it here/i\Some More Text is appended/" your_file.txt ("Some More Text is appended" Text 가 "Please Put it here" 있는 라인 위에 추가)

  sed -i'' -r -e "/Please Put it here/a\Some More Text is appended/" your_file.txt ("Some More Text is appended" Text 가 "Please Put it here" 있는 라인 아래에 추가)

  sed -i'' -r -e "/alias nmdown='stopNodeManager -host localhost -port 17730'\a/alias nmdown='stopNodeManager -properties $JEUS_HOME/nodemanager/jeusnm.xml'" (alias nmdown='stopNodeManager -host localhost -port 17730 밑에다가 추가)
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
* 특정 문구가 포함된 경로 변경 (바꿀 대상 / 바꿀 경로)

  sed -i '\/usr\/lib\/jvm\/jdk1.7.0_80/ c\/usr\/java\/jdk1.8.0_281' /home/user/.bash_profile
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
* #!/replace/with/path/to/perl/interpreter -w 를 #!/usr/bin/perl -w 로 치환

  sed -i 's/\#\!\/replace\/with\/path\/to\/perl\/interpreter \-w/\#\!\/usr\/bin\/perl \-w/g' test.sh
