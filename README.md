# Spicy Parsers

Dropping parsers here for now

## Running some parsers

### Parse an example UTF16 string with a BOM.

```sh
spicy-dump -f unicode/example1.txt unicode/utf16.spicy --json | jq
```

### Parse a Notepad Cache file and dump the entire data structure.

```sh
spicy-dump  -p Notepad_Cache::File -f notepad-cache/example1.bin --json notepad-cache/notepad_cache.spicy | jq
```

### Run a tool to validate CRC32 checksums in a Notepad Cache file.

```sh
spicy-driver --library-path=notepad-cache -p Notepad_Cache::File -f notepad-cache/example1.bin notepad-cache/notepad_cache_validator.spicy
```

### Parse an iCalendar file.

```sh
spicy-dump -f icalendar/test.ics icalendar/icalendar.spicy
```
