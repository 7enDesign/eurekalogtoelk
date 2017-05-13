# eurekalogtoelk

This tool reads the logs generated by [EurekaLog](https://www.eurekalog.com) and sends to the [elasticsearch](http://www.elastic.co).

## eurekalogtoelk -h

	Usage:
	   eurekalogtoelk.py -p <path> -a <elastic host:port> [-f <file with field list>]
		   -p      Path with eureka log files in ".el" extension;
		   -a      Address with host (port is optional) for elasticsearch instalation. 
					Example: 192.168.0.2 or 10.0.100.20:9210;
		   -f      File in text format with fields list, one field by line (optional);
		   -c      number of threads whose callbacks will be read, default = 1;
	       -t      Use threads, one per file (experimental);
		   -h      This help information;

	Example:
	   eurekalogtoelk.py -p "c:\mylogs\eurekalog\" -a 10.100.0.10 -f field_list.txt -c 2

## installation

### How to install python into Windows

To install python into Windows I recommend to use [Chocolatey](http://chololatey.org/install).

You must execute this command line in your Command Prompt (as Administrator):

	@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin

	choco install python

### How to install the dependencies

This project uses Elasticsearch python module, you must install this module before running:

	pip install elasticsearch

### Remote installation with WGET

Use this commands to easily download the files:

	wget https://raw.githubusercontent.com/fabianobr/eurekalogtoelk/master/logeureka.py
	wget https://raw.githubusercontent.com/fabianobr/eurekalogtoelk/master/eurekalogtoelk.py
	wget https://raw.githubusercontent.com/fabianobr/eurekalogtoelk/master/field_list.txt

## TO-DO

* More technical details;

* Kibana visualizations who shows the power of analytics informations;

* Code tests!

Fork me and enjoy!

