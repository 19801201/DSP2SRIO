# DSP2SRIO

![Image](https://github.com/19801201/Image/blob/main/DSP2SRIO.png)

DSP传输数据方式如图所示。首先从DSP获取到数据到SRIO中，存到fifo缓存中，通过stream形式传入到DMA中，最后存放到DDR中。然后通过内部控制reg信号控制DMA从DDR读出的数据，以stream的形式存入到fifo中，读取到SRIO，返回给DSP。Reg1是内部控制reg由AXI lite映射与外部TJPU交互的寄存器。
