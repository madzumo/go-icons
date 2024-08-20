# Generate .syso files (icon on .exe)

Install rsrc:
```shell
go install github.com/akavel/rsrc@latest
```

Run rsrc:
```shell
$GOPATH/bin/rsrc -ico iconname.ico
```
It will create a new .syso file every time. Store these files inside your main package.

OPTIONS:
  * -arch string

    	architecture of output file - one of: 386, amd64, [EXPERIMENTAL: arm, arm64] (default "amd64") ex: $GOPATH/bin/rsrc -arch amd64 -ico icon.ico

  * -ico string
    	
        comma-separated list of paths to .ico files to embed

  * -manifest string
    	
        path to a Windows manifest file to embed

  * -o string
    	
        name of output COFF (.res or .syso) file; if set to empty, will default to 'rsrc_windows_{arch}.syso'