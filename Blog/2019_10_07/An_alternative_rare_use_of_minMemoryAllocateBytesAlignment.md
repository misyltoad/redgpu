99.9% of the time, you align memory allocations with minMemoryAllocateBytesAlignment and forget about it.

But there’s another use of minMemoryAllocateBytesAlignment that may come up in 0.1% of the time you need to be aware of: if your program receives RED_STATUS_ERROR_MEMORY_MAPPING_FAILED and it uses one or a couple of very large contiguous memory allocations which can’t be unmapped entirely, you need to map memory partially. For partial mapping of memory, minMemoryAllocateBytesAlignment becomes a block size at the beginning and end of which mapping must occur. In other words, for partial mapping of memory, you can not start mapping at an address which is not a multiple of minMemoryAllocateBytesAlignment and you can not end mapping at an address which is not a multiple of minMemoryAllocateBytesAlignment.

This is an edge case that might show up only due to a virtual address space fragmentation or a hidden platform limit on a maximum size of contiguous virtual address range, both of which are outside of program’s or API’s control. But if your program will receive RED_STATUS_ERROR_MEMORY_MAPPING_FAILED and it won’t have some memory to unmap to free up the virtual address space for a new mapping, then you’ll know what to do.