Strom_CP
========

As per CP Requirement


Step 1



Mysql DB schema name "cpdb"

DROP TABLE IF EXISTS `cpdb`.`processed_data`;
CREATE TABLE  `cpdb`.`processed_data` (
  `id` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `type` varchar(10) DEFAULT NULL,
  `nid` varchar(10) DEFAULT NULL,
  `did` varchar(10) DEFAULT NULL,
  `s0` varchar(10) DEFAULT NULL,
  `s1` varchar(10) DEFAULT NULL,
  `s2` varchar(10) DEFAULT NULL,
  `s3` varchar(10) DEFAULT NULL,
  `datetime` varchar(25) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=10 DEFAULT CHARSET=latin1;

DROP TABLE IF EXISTS `cpdb`.`aggregate_data`;
CREATE TABLE  `cpdb`.`aggregate_data` (
  `datetime` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `nid` varchar(10) DEFAULT NULL,
  `did` varchar(10) DEFAULT NULL,
  `parametername` varchar(50) DEFAULT NULL,
  `sum` int(10) unsigned DEFAULT NULL,
  `numberof` int(10) unsigned DEFAULT NULL,
  `avg` float DEFAULT NULL,
  PRIMARY KEY (`datetime`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;




Step 2


Deploy JSONStream.war under tomcat running under port 8080

Step 3

Start tomcat server

Step 4

Start Storm service in netbeans

