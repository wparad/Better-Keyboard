# Have A Better Keyboard

## Development

* Android studio, follow the instructions
	```bash
		add-apt-repository -y ppa:webupd8team/java
		apt-get update
	  	echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
		apt-get install -y oracle-java8-installer lib32z1 lib32ncurses5 lib32stdc++6 g++
		echo "JAVA_HOME=$(update-alternatives --query javac | sed -n -e 's/Best: *\(.*\)\/bin\/javac/\1/p')" >> /etc/environment
	```
* Load the emulator when missing libstdc++ `LD_PRELOAD='/usr/lib/x86_64-linux-gnu/libstdc++.so.6' ~/Android/Sdk/tools/emulator -netdelay none -netspeed full -avd Nexus_5X_API_23`