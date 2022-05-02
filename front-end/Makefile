help: 
	@echo 'Usage:'
	@sed -n 's/^##//p' ${MAKEFILE_LIST} | column -t -s ':' |  sed -e 's/^/ /'

## 'make run' will start the process on port 8080 and open the default xorg browser with it you need to run 'make kill' to stop the process started with run
run:
	go run ./cmd/web/*.go & xdg-open http://localhost:8080 

## 'make kill' will stop the background process on port 8080 it neets fuser installed in order to work 
kill:
	fuser -k 8080/tcp
