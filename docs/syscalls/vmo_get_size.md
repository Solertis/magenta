# mx_vmo_get_size

## NAME

vmo_get_size - read the current size of a VMO object

## SYNOPSIS

```
#include <magenta/syscalls.h>

mx_status_t mx_vmo_get_size(mx_handle_t handle, uint64_t* size);

```

## DESCRIPTION

**vmo_get_size**() returns the current size of the VMO.

## RETURN VALUE

**vmo_get_size**() returns **NO_ERROR** on success. In the event
of failure, a negative error value is returned.

## ERRORS

**ERR_INVALID_ARGS**  *size* is an invalid pointer or NULL.

## SEE ALSO

[vmo_create](vmo_create.md),
[vmo_read](vmo_read.md),
[vmo_write](vmo_write.md),
[vmo_set_size](vmo_set_size.md),
[vmo_op_range](vmo_op_range.md).

