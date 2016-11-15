# mx_vmar_unmap

## NAME

vmar_unmap - unmap a memory mapping

## SYNOPSIS

```
#include <magenta/syscalls.h>

mx_status_t mx_vmar_unmap(mx_handle_t vmar_handle,
                          uintptr_t addr, mx_size_t len);
```

## DESCRIPTION

**vmar_unmap**() unmaps all VMO mappings and destroys (as if **vmar_destroy**
were called) all sub-regions within the given range.  Note that this operation
is logically recursive.

## RETURN VALUE

**vmar_unmap**() returns **NO_ERROR** on success.

## ERRORS

**ERR_NOT_FOUND**  could not find the requested mapping

## NOTES

Currently *len* must be either 0, or *addr* and *len* must completely
describe either a single mapping or sub-region.

## SEE ALSO

[vmar_destroy](vmar_destroy.md).
[vmar_map](vmar_map.md).
[vmar_protect](vmar_protect.md).
