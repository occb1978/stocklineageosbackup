# backup_microg_lineageos

- Install

```
go install github.com/github-release/github-release@latest
```

- Create a token with Repository permissions with  Read and Write access to code
- https://github.com/settings/apps

```
export GITHUB_TOKEN=github_pat_11
```

- Download 

```
wget -r -l1 --no-parent https://download.lineage.microg.org/sargo
```

- Create a tag for release

```
github-release release --user atrink1978 --repo backup_microg_lineageos --tag flame
```

- Run command

```
for i in `ls line*`
  do 
   ls -al $i 
   github-release upload --user atrink1978 --repo backup_microg_lineageos --tag  sailfish  --name  $i --file  $i 
   sleep 60
  done
```
