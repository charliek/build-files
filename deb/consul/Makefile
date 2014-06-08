
# still must change the version in the control file
version=0.2.1
name=consul

# still must change paths in upstart file
bin_dir=usr/bin
assets_dir=usr/share/consul
data_dir=usr/lib/consul/data
config_dir=etc/consul.d

build: download-assets build-deb

download-assets:
	mkdir -p tmp

	# download and unzip consul binary
	curl -L https://dl.bintray.com/mitchellh/consul/${version}_linux_amd64.zip -o tmp/consul.zip
	unzip tmp/consul.zip -d tmp/
	mkdir -p src/$(bin_dir)
	mv tmp/consul src/$(bin_dir)/consul

	# download and unzip consul web ui
	curl -L https://dl.bintray.com/mitchellh/consul/${version}_web_ui.zip -o tmp/web_ui.zip
	unzip tmp/web_ui.zip -d tmp/
	mkdir -p src/$(assets_dir)
	mv tmp/dist src/$(assets_dir)/web

	mkdir -p src/$(data_dir)
	mkdir -p src/$(config_dir)

clean:
	rm -rf tmp
	rm -rf src/usr
	rm -rf src/etc/consul.d
	rm -rf out

build-deb:
	mkdir -p out
	dpkg-deb --build src out
