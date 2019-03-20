## HOW TO INSTALL THRIFT
I spent a night to clariry how to compile `thrift`. So much challenge because every dependent libraries have beed updated.


Requirements
=============
1. Compile and install Thrift v0.9.3:

    `git clone https://github.com/apache/thrift`
    
    `git checkout -f 0.9.3`

    `cd thrift && mkdir build && cd build`

    `cmake .. && make -j4` -- number 4 is n_cpu_cores used to compile

    `sudo make install`

To Compile Bin file
==========

For compiling the HaHs server 

    g++ -DHAVE_INTTYPES_H -DHAVE_NETINET_IN_H -Wall -I/usr/local/include/thrift *.cpp -L/usr/local/lib -lthrift -lthriftnb -levent -o server

or run

    make

To Run
========
    ./server



References
========

1. Require openssl < 1.1: `https://github.com/ptrkrysik/gr-gsm/issues/283`
2. Copy linked file: `https://superuser.com/questions/216919/how-to-copy-symlinks-to-target-as-normal-folders`
3. Install openssl: `https://www.howtoforge.com/tutorial/how-to-install-openssl-from-source-on-linux/`
4. `http://thachleblog.com/apache-thrift-gioi-thieu-va-cai-dat/`