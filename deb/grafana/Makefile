
# still must change the version in the control file
version=1.6.1

build: download-assets build-deb

download-assets:
	mkdir -p src/usr/share
	curl -L http://grafanarel.s3.amazonaws.com/grafana-${version}.tar.gz -o src/usr/share/grafana.tar.gz
	tar -C src/usr/share -zxvf src/usr/share/grafana.tar.gz
	mv src/usr/share/grafana-${version} src/usr/share/grafana
	rm src/usr/share/grafana.tar.gz

clean:
	rm -rf src/usr
	rm -rf out

build-deb:
	mkdir -p out
	dpkg-deb --build src out
