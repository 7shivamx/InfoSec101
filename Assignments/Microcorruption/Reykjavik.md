# Microcorruption - Reykjavik

Author: [Shivam Mishra](https://github.com/7shivamx)

## Approach

The enc function is called in the main function, but it seems that the function expands the instruction on the stack in memory.
```
4438 <Main> 
4438: 3E40 2045 Mov # 0X4520, R14   
443C: 0F4e Mov R14, R15   
443E: 3E40 F800 Mov # 0Xf8, R14   
4442: 3F40 0024 Mov # 0X2400, R15 
4446: D012 8644 Call # 0X4486 <Enc> 
444A: d012 0024 call # 0x2400 
444e: 0f43 clr r15
```

If we look at the current instruction, a comparison instruction will appear.
```
d490 8d40 bcff 
cmp # 0x408d, -0x24 (r4)
```

Thus considering little endian, -0x24 (r4) points to the beginning of the input value

## Flag (hex)
> 8d40
