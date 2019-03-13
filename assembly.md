MOVZX:进行全零扩展->  
  
      .data    
      test BYTE 10001111b  
      .code  
      movzx ax,test ;ax=0000000010001111b
MOVSX:进行符号扩展->  
  
      .data
      test BYTE 10001111b  
      .code  
      movsx ax,test ;ax=1111111110001111b  
加法和减法：  
      
      inc:操作数加1   
      dec:操作数减1   
      add eax,var ;加法   
      sub eax,var ;减法
  
例：计算rval = -xval + (yval - zval)  
    
      
      .data  
      rval SDWORD ?  
      xval SDWORD 26  
      yval SDWORD 30  
      zval SDWORD 40  
      .code  
      main proc  
      mov eax, xval  
      neg eax ;转为补码再取反  
      mov ebx, yval
      sub ebx, zval
      add eax, ebx
      neg ebx
      mov rval, eax
      invoke ExitProcess,0 
      main endp
      end main
