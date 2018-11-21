# docker-compose-Apache-with-MariaDB
Creating a docker-compose file which links Apache and MariaDB images

##### Features

- Creating docker-HTTPD image 
- Creating an HTML file which will be presented on our web-page
- Using docker-compose for linking MariaDB image to

## Prerequisites

- Install DockerCE according to instructions
- Install docker-compose according to instructions
- Install git according to instructions
- Make sure port 2000 

## Getting Started

### Instruction

1. Clone project using git clone
2. Change directory to the project
3. docker-compose up 

```
ubuntu@ip-172-31-38-60:~/apache_v1$ sudo docker-compose up
Starting apache_v1_db_1_f0d2b7292575 ... done
Starting apache_v1_web_1_56b835b88dc7 ... done
Attaching to apache_v1_db_1_f0d2b7292575, apache_v1_web_1_56b835b88dc7
web_1_56b835b88dc7 | AH00558: httpd: Could not reliably determine the server's f                                                                                                             ully qualified domain name, using 172.18.0.3. Set the 'ServerName' directive glo                                                                                                             bally to suppress this message
web_1_56b835b88dc7 | AH00558: httpd: Could not reliably determine the server's f                                                                                                             ully qualified domain name, using 172.18.0.3. Set the 'ServerName' directive glo                                                                                                             bally to suppress this message
web_1_56b835b88dc7 | [Wed Nov 21 13:13:22.990812 2018] [mpm_event:notice] [pid 1                                                                                                             :tid 139858433414336] AH00489: Apache/2.4.37 (Unix) configured -- resuming norma                                                                                                             l operations
web_1_56b835b88dc7 | [Wed Nov 21 13:13:22.995989 2018] [core:notice] [pid 1:tid                                                                                                              139858433414336] AH00094: Command line: 'httpd -D FOREGROUND'
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] mysqld (mysqld 10.4.0-MariaDB-1                                                                                                             :10.4.0+maria~bionic) starting as process 1 ...
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Using Linux native AIO
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Mutexes and rw_locks us                                                                                                             e GCC atomic builtins
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Uses event mutexes
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Compressed tables use z                                                                                                             lib 1.2.11
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Number of pools: 1
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Using SSE2 crc32 instru                                                                                                             ctions
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] mysqld: O_TMPFILE is not suppor                                                                                                             ted on /tmp (disabling future attempts)
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Initializing buffer poo                                                                                                             l, total size = 256M, instances = 1, chunk size = 128M
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Completed initializatio                                                                                                             n of buffer pool
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: If the mysqld execution                                                                                                              user is authorized, page cleaner thread priority can be changed. See the man pa                                                                                                             ge of setpriority().
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: 128 out of 128 rollback                                                                                                              segments are active.
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Creating shared tablesp                                                                                                             ace for temporary tables
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Setting file './ibtmp1'                                                                                                              size to 12 MB. Physically writing the file full; Please wait ...
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: File './ibtmp1' size is                                                                                                              now 12 MB.
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Waiting for purge to st                                                                                                             art
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: 10.4.0 started; log seq                                                                                                             uence number 139830; transaction id 21
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Loading buffer pool(s)                                                                                                              from /var/lib/mysql/ib_buffer_pool
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] Plugin 'FEEDBACK' is disabled.
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] InnoDB: Buffer pool(s) load com                                                                                                             pleted at 181121 13:13:23
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] Server socket created on IP: ':                                                                                                             :'.
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Warning] 'proxies_priv' entry '@% roo                                                                                                             t@0d4f369281e3' ignored in --skip-name-resolve mode.
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] Reading of all Master_info entr                                                                                                             ies succeded
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] Added new Master_info '' to has                                                                                                             h table
db_1_f0d2b7292575 | 2018-11-21 13:13:23 0 [Note] mysqld: ready for connections.
db_1_f0d2b7292575 | Version: '10.4.0-MariaDB-1:10.4.0+maria~bionic'  socket: '/v                        
```

## Built With

* [Docker](https://www.python.org/) -  Build, Manage and secure business-critical applications without the fear of technology or infrastructure lock-in.
* HTML -  Hypertext Markup Language is the standard markup language for creating web pages and web applications

## Versioning

* [Git](https://git-scm.com/) -  free and open source distributed version control system.

## Authors

* [Yam Peled](https://github.com/yampeled1)
