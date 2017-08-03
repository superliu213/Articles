### 用MAC通过虚拟机连接oracle数据库
#### 一、安装oracle
  1. 密码管理
     设置成为统一密码 afcapp

#### 二、安装oracle客户端
  1. 下载并解压oracle客户端
  2. 拷贝 C:\app\Administrator\product\11.2.0\dbhome_1\Network
  目录到oralce客户端的
  C:\app\Administrator\product\instantclient-basic-win32-11.2.0.1.0\instantclient_11_2
  目录下
  3. 修改listener
  ```
  SID_LIST_LISTENER =
  (SID_LIST =
    (SID_DESC =
      (GLOBAL_DBNAME = ORCL)
      (ORACLE_HOME =C:\app\Administrator\product\11.2.0\dbhome_1)
      (SID_NAME = ORCL)
    )
    (SID_DESC =
      (SID_NAME = CLRExtProc)
      (ORACLE_HOME = C:\app\Administrator\product\11.2.0\dbhome_1)
      (PROGRAM = extproc)
      (ENVS = "EXTPROC_DLLS=ONLY:C:\app\Administrator\product\11.2.0\dbhome_1\bin\oraclr11.dll")
    )
  )

  LISTENER =
  (DESCRIPTION_LIST =
    (DESCRIPTION =
      (ADDRESS = (PROTOCOL = IPC)(KEY = EXTPROC1521))
      (ADDRESS = (PROTOCOL = TCP)(HOST = WIN-T0DVL226JUS)(PORT = 1521))
    )
  )
  ```
  4. tnsnames
  ```
  ORCL =
  (DESCRIPTION =
    (ADDRESS = (PROTOCOL = TCP)(HOST = WIN-T0DVL226JUS)(PORT = 1521))
    (CONNECT_DATA =
      (SERVER = DEDICATED)
      (SERVICE_NAME = orcl)
    )
  )
HZACCAFC =
  (DESCRIPTION =
    (ADDRESS_LIST =
      (ADDRESS = (PROTOCOL = TCP)(HOST = 192.168.140.100)(PORT = 1521))
    )
    (CONNECT_DATA =
      (SERVER = DEDICATED)
      (SERVICE_NAME = afcdb100)
    )
  )
  ```
  注意：使用本机电脑名
  5. 添加环境变量
  TNS_ADMIN=C:\app\Administrator\product\instantclient-basic-win32-11.2.0.1.0\instantclient_11_2\NETWORK\ADMIN
  指定listener和tnsnames的位置
  NLS_LANG=SIMPLIFIED CHINESE_CHINA.ZHS16GBK
  指定字符集
#### 三、安装pl/sql
  1. 配置客户端
  oracle主目录名
  C:\app\Administrator\product\instantclient-basic-win32-11.2.0.1.0\instantclient_11_2
  OCI库
  C:\app\Administrator\product\instantclient-basic-win32-11.2.0.1.0\instantclient_11_2\oci.dll
#### 四、配置连接
  1. 配置连接
