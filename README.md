firstly I created the Virtual machine and installed apache and PHP on linux operating system.
Here is how to install apache and PHP: https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04

<?php

/* counter */

//opens countlog.txt to read the number of hits
$datei = fopen("/countlog.txt","r");
$count = fgets($datei,1000);
fclose($datei);
$count=$count + 1 ;
echo "$count" ;
echo " hits" ;
echo "\n" ;

// opens countlog.txt to change new hit number
$datei = fopen("countlog.txt","w");
fwrite($datei, $count);
fclose($datei);

?>
<?php

include("counter.php");

?>
Her is the code for the hit counter that we use: http://justintadlock.com/web-design/counter

Docker

I installed docker using the commands on the following link
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04
I also created docker file  then created account on docker hub to to complete the docker installation
I also created dockerfile and info.php. here is the code for info.php
 <?php
phpinfo();
?>
and I ran PHP on docker
