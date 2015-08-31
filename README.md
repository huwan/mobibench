Mobile benchmark tool (mobibench) shell version
================================
**NOTE**

This repo copy the mobibench shell version from https://github.com/ESOS-Lab/Mobibench. See original repo for more information.

-----------------------------------


* Maintainer : Sooman Jeong (smartzzz77@gmail.com)
* Contributor : Kisung Lee (kisunglee@hanyang.ac.kr), Seongjin Lee (insight@hanyang.ac.kr), Dongil Park (idoitlpg@hanyang.ac.kr), Jungwoo Hwang (tearoses@hanyang.ac.kr), and Chanhyun Park (parkch0708@hanyang.ac.kr)

### Reference: 
 * Sooman Jeong, Kisung Lee, Jungwoo Hwang, Seongjin Lee, Youjip Won, "AndroStep: Android Storage Performance Analysis Tool", The 1st European Workshop on Mobile Engineering (ME'13), Feb. 26, 2013, Aachen, Germany 
<http://www.esos.hanyang.ac.kr/files/publication/conferences/international/AndroStep.pdf>

 * Sooman Jeong, Kisung Lee, Jungwoo Hwang, Seongjin Lee, Youjip Won, "Framework for Analyzing Android I/O Stack Behavior: from Generating the Workload to Analyzing the Trace", Future Internet 2013, 5(4), Special Issue for "Mobile Engineering², MDPI(ISSN 1999-5903), 591-610; doi:10.3390/fi5040591 
<http://www.mdpi.com/1999-5903/5/4/591/pdf>

### Acknowledgement:
 * This work is supported by IT R&D program MKE/KEIT (No. 10041608, Embedded System Software for New-memory based Smart Device). 

### Release
#####Version 1.04
Followings are updated for the performance rank system.
 * Customized benchmark results can be registered to the performance rank server.
 * Average performance of the users with the same device is shown in the rank page.
 * The best, median, and the worst performance of a device is shown in the details page under the rank.
 * eMMC serial number, memory size, and kernel version for each device is shown in the details page.


MobiBench (Application version)
-----------------------------------
See [ESOS-Lab/Mobibench](https://github.com/ESOS-Lab/Mobibench).                                     

Build shell version
--------------------
    # cd  Mobibench && make


Usage (shell version)
----------------------
	# mobibench [-p pathname] [-f file_size_Kb] [-r record_size_Kb] [-a access_mode] [-h]
                    [-y sync_mode] [-t thread_num] [-d db_mode] [-n db_transcations]
                    [-j SQLite_journalmode] [-s SQLite_syncmode] [-g replay_script] [-q]
                                     
                                     
* -p  set path name (default=./mobibench)
* -f  set file size in KBytes (default=1024)
* -r  set record size in KBytes (default=4)
* -a  set access mode (0=Write, 1=Random Write, 2=Read, 3=Random Read) (default=0)
* -y  set sync mode (0=Normal, 1=O_SYNC, 2=fsync, 3=O_DIRECT, 4=Sync+direct,
                     5=mmap, 6=mmap+MS_ASYNC, 7=mmap+MS_SYNC) (default=0)
* -t  set number of thread for test (default=1)
* -d  enable DB test mode (0=insert, 1=update, 2=delete)
* -n  set number of DB transaction (default=10)
* -j  set SQLite journal mode (0=DELETE, 1=TRUNCATE, 2=PERSIST, 3=WAL, 4=MEMORY, 
                               5=OFF) (default=1)
* -s  set SQLite synchronous mode (0=OFF, 1=NORMAL, 2=FULL) (default=2)
* -g  set replay script (output of MobiGen)
* -q  do not display progress(%) message                                                           			
