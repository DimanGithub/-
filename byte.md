# Initial byte array
  byte[]myb=new byte[]{0x01,110,0xff};

# Print byte in HEX format
  byte b =255;
  Console.WriteLine(b.ToString("X2"));  
  >Вывод на экран: ff
  
# Конвертируем выше приведенный массив байтов в строковый массив содержащий биты  использую LINQ
  string arrs=myb.Select(x=>Convert.ToString(x,2).PadLeft(8,'0')).ToArray();
  >если вывести на экран этот массив то он будет выглядеть так
  >>00000001 - myb[0]{0x01}; 
  >
  >>01101110 - myb[1]{110}; 
  >
  >>11111111 - myb[2]{0xff}; 
  
