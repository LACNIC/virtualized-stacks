# Makefile for running and building fort

VERSION=1.1.2

lacnic: 
	docker run -v $$(pwd)/tal:/tal -v $$(pwd)/roas:/roas \
	   carlosm3012/fort-validator:1.1.2 \
	   fort --log.level=info --output.roa=/roas/lacnic.csv --tal=/tal/lacnic.tal --mode=standalone

apnic: 
	docker run -v $$(pwd)/tal:/tal -v $$(pwd)/roas:/roas \
	   carlosm3012/fort-validator:1.1.2 \
	   fort --log.level=info --output.roa=/roas/apnic.csv --tal=/tal/apnic.tal --mode=standalone

afrinic: 
	docker run -v $$(pwd)/tal:/tal -v $$(pwd)/roas:/roas \
	   carlosm3012/fort-validator:1.1.2 \
	   fort --log.level=info --output.roa=/roas/afrinic.csv --tal=/tal/afrinic.tal --mode=standalone

image: fort-1.1.2/Dockerfile
	docker build -t carlosm3012/fort-validator:1.1.2 fort-1.1.2
