# ArangoRocks

Access an ArangoDB/RocksDB database directory with a standalone C++ program.

## Building

Dependencies (on ubuntu):V

```
sudo apt-get install libgflags-dev libsnappy-dev build-essential cmake
```

Run

```
./getstuff.sh
```

this will clone a few subrepositories.

Then do

```
make normal
```

for a release build and

```
make debug
```

for a debug build.

Result is in `./build/arangorocks`.

## Usage

```
  Usage:
    arangorocks [-h] [--version] [-d DBPATH] dump_all [-o OUTPATH]
    arangorocks [-h] [--version] [-d DBPATH] dump_collection [-c OBJID] [-o OUTPATH]
    arangorocks [-h] [--version] [-d DBPATH] list_collections [-o OUTPATH]

  Options:
    -h --help                    Only show this screen.
    --version                    Only show the version.
    -c OBJID --objid=OBJID       ObjectId of collection to dump.
    -d DBPATH --dbpath=DBPATH    Path to DB [default: /tmp/testdb].
    -o OUTPATH --output=OUTPATH  Path to write collection dump [default: ./dump].
```
