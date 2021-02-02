## Go embed

### Install Go 1.16rc1

Instructions are [here](https://golang.org/dl/) as of this writing on 2021-02-01.

1. Run `go get golang.org/dl/go1.16rc1`
2. The above will install an executable named `go1.16rc1.exe` (on Windows)
3. Run it and it will output a message:
```sh
$ go1.16rc1.exe
go1.16rc1: not downloaded. Run 'go1.16rc1 download' to install to C:\Users\mando\sdk\go1.16rc1
$
```
4. Run `go1.16rc1.exe download` as directed
5. It will download and unpack the SDK in a folder in your home directory namded `sdk`
```sh
$ go1.16rc1.exe download
Downloaded   0.0% (    16384 / 146872278 bytes) ...
Downloaded   8.9% ( 13089669 / 146872278 bytes) ...
Downloaded  26.8% ( 39421020 / 146872278 bytes) ...
Downloaded  45.7% ( 67142748 / 146872278 bytes) ...
Downloaded  65.3% ( 95913052 / 146872278 bytes) ...
Downloaded  84.9% (124649472 / 146872278 bytes) ...
Downloaded  99.5% (146113065 / 146872278 bytes) ...
Downloaded 100.0% (146872278 / 146872278 bytes)
Unpacking C:\Users\mando\sdk\go1.16rc1\go1.16rc1.windows-amd64.zip ...
Success. You may now run 'go1.16rc1'
$
```
6. The executable will be in `$HOME/sdk/go1.16rc1/bin`:
```sh
$ ls
go.exe*  gofmt.exe*
$ ./go.exe version
go version go1.16rc1 windows/amd64
$
```

### How to use
1. `cd client`
2. `npm i`
3. `npm run-script build`
3. `cd ..`
4. `go build -o server main.go`
5. `./server`
