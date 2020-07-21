# Block Interleaver
The project contains VHDL implementation of block interleaver and deinterleaver.


## Block Description
### Port Descriptions
- ***clk***: System clock pin
- ***rst***: System reset pin
- ***i_consume***: Readiness to consume o_data
- ***i_end_cw***:  End of data reception
- ***i_start_cw***: Start of data reception
- ***i_valid***: Validity of input symbols
- ***i_data***: Input data
- ***o_end_cw***:  End of data transmission
- ***o_start_cw***: Start of data transmission
- ***o_valid***: Validity of output symbols
- ***o_data***: Output data
- ***o_in_ready***: Readiness to accept new input symbols
- ***o_error***: Error status

### Generic Parameters 
***src/block_interleaver.vhd*** is the top level architecture of the block. Its entity contains generic parameters that can be adjusted before synthesis:
- **NUMBER_OF_ELEMENTS**: RAM's maximum capacity
- **NUMBER_OF_LINES**: Fixed number of rows
- **WORD_LENGTH**: Number of bits of each symbol
- **MODE**: false to select INTERLEAVER and true to select DEINTERLEAVER
