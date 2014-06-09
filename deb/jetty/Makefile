
build: download-assets build-deb

download-assets:
	# download unzip the jetty binary
	mkdir -p src/usr/share/jetty-runner-9.1.0
	curl -L http://repo1.maven.org/maven2/org/eclipse/jetty/jetty-runner/9.1.0.v20131115/jetty-runner-9.1.0.v20131115.jar -o src/usr/share/jetty-runner-9.1.0/jetty.jar

clean:
	rm -rf src/usr
	rm -rf out

build-deb:
	mkdir -p out
	dpkg-deb --build src out
	# package can be tested with:
	# sudo dpkg -i out/jetty-runner_9.1.0_all.deb
	# sudo dpkg -r jetty-runner