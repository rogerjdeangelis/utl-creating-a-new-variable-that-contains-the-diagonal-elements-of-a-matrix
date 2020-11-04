# utl-creating-a-new-variable-that-contains-the-diagonal-elements-of-a-matrix
Creating a new variable that contains the diagonal elements of a matrix
    Creating a new variable that contains the diagonal elements of a matrix                                               
                                                                                                                          
    Interesting example of mete data in your data                                                                         
                                                                                                                          
    GitHub                                                                                                                
    https://cutt.ly/jgDBrJU                                                                                               
    https://github.com/rogerjdeangelis/utl-creating-a-new-variable-that-contains-the-diagonal-elements-of-a-matrix        
                                                                                                                          
    *                                                                                                                     
    #####  #   #  ####   #   #  #####                                                                                     
      #    ##  #  #   #  #   #    #                                                                                       
      #    # # #  #   #  #   #    #                                                                                       
      #    #  ##  ####   #   #    #                                                                                       
      #    #   #  #      #   #    #                                                                                       
      #    #   #  #      #   #    #                                                                                       
    #####  #   #  #       ###     #                                                                                       
                                                                                                                          
    #! INPUT ;                                                                                                            
    data have;                                                                                                            
    input colNam$ A B C;                                                                                                  
    cards4;                                                                                                               
    A  1 0 0                                                                                                              
    B  0 2 0                                                                                                              
    C  0 0 3                                                                                                              
    ;;;;                                                                                                                  
    run;quit;                                                                                                             
                                                                                                                          
                             |  RULES                                                                                     
                             |                                                                                            
    WORK.HAVE total obs=3    |                                                                                            
                             |                                                                                            
      COLNAM    A    B    C  |  DIAG                                                                                      
                             |                                                                                            
        A       1    0    0  |   1                                                                                        
        B       0    2    0  |   2                                                                                        
        C       0    0    3  |   3                                                                                        
                                                                                                                          
    *                                                                                                                     
     ###   #   #  #####  ####   #   #  #####                                                                              
    #   #  #   #    #    #   #  #   #    #                                                                                
    #   #  #   #    #    #   #  #   #    #                                                                                
    #   #  #   #    #    ####   #   #    #                                                                                
    #   #  #   #    #    #      #   #    #                                                                                
    #   #  #   #    #    #      #   #    #                                                                                
     ###    ###     #    #       ###     #                                                                                
                                                                                                                          
    #! OUTPUT ;                                                                                                           
                                                                                                                          
                                                                                                                          
    WORK.WANT total obs=3                                                                                                 
                                                                                                                          
       DIAG                                                                                                               
                                                                                                                          
        1                                                                                                                 
        2                                                                                                                 
        3                                                                                                                 
                                                                                                                          
    *                                                                                                                     
    ####   ####    ###    ###   #####   ###    ###                                                                        
    #   #  #   #  #   #  #   #  #      #   #  #   #                                                                       
    #   #  #   #  #   #  #      #       #      #                                                                          
    ####   ####   #   #  #      ####     #      #                                                                         
    #      # #    #   #  #      #         #      #                                                                        
    #      #  #   #   #  #   #  #      #   #  #   #                                                                       
    #      #   #   ###    ###   #####   ###    ###                                                                        
                                                                                                                          
    #! PROCESS ;                                                                                                          
                                                                                                                          
                                                                                                                          
    data want;                                                                                                            
                                                                                                                          
      set have;                                                                                                           
                                                                                                                          
      diag=vvaluex(colNam);                                                                                               
      keep diag;                                                                                                          
                                                                                                                          
    run;quit;                                                                                                             
                                                                                                                          
                                                                                                                          
