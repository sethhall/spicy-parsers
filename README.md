# Spicy Parsers

Dropping parsers here for now

## Running some parsers

### Parse an example UTF16 string with a BOM.

```sh
spicy-dump -f unicode/example1.txt unicode/utf16.spicy --json | jq
```

### Parse a Notepad Cache file and dump the entire data structure.

```sh
spicy-dump --library-path=unicode/ -p NotepadCache::File -f notepad-cache/example1.bin --json notepad-cache/notepad-cache-parser.spicy | jq
```

### Run a tool to validate CRC32 checksums in a Notepad Cache file.

```sh
spicy-driver --library-path=unicode/ -p NotepadCache::File -f notepad-cache/example1.bin notepad-cache/notepad-cache-validator.spicy notepad-cache/notepad-cache-parser.spicy
```
