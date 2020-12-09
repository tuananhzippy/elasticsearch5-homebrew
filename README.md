# Elasticsearch 5.x for MacOS

Elasticsearch is written in Java so you need to install JDK version >= 8 before installing Elasticsearch. Installation instructions can be found here: https://www.java.com/en/download/

Make sure you have Homebrew installed on your operating system. Installation instructions can be found here: https://brew.sh/

## Install

After successful Homebrew installation. Download the **elasticsearch@5.rb** file and place it in ```/usr/local/Homebrew/Library/Taps/homebrew/homebrew-core/Formula/```.

Next, open Termial and type the following command:

```
$ brew search elasticsearch
```

to check which elasticsearch versions are available. Now choose the version you want to install.

```
$ brew install elasticsearch@5
```

Installation and download will take place, please wait a moment. After a successful installation use the following command to work with Elasticsearch.

```
$ brew services start|restart|stop elasticsearch@5
```

The config folders are stored in the following directories:

* Data: ```/usr/local/var/lib/elasticsearch/```
* Logs: ```/usr/local/var/log/elasticsearch/elasticsearch_macos.log```
* Plugins: ```/usr/local/var/elasticsearch/plugins/```
* Config: ```/usr/local/etc/elasticsearch/```

## Advanced

To customize the **Elasticsearch 5.x** version to your liking, modify the **elasticsearch@5** file a bit by changing the value:

```
url "https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-5.5.0.tar.gz"
sha256 "aa316b8a46b1daef9189090f41e4226794b4e4e8f361caa1be5ad6c4ed753f2e"
```

Where ```url``` is the path of the .tar.gz file.
      ```sha265``` is the hash of the .tar.gz file.

Elasticseach releases can be found here: https://www.elastic.co/downloads/past-releases#elasticsearch


## Test

Run the following command for information about the state of Elasticsearch:

```
$ curl 127.0.0.1:9200
```
