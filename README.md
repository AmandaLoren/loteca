<? php 
 
 menu (); 
 
 Menu function () { 
      echo "solicite hum Jogo (1) MEGA (2) QUINA (5) Sair."; 
      Jogo $ = fgets (STDIN); 
 
      switch ($ Jogo) { 
          Caso 1: 
              echo "REGRASS DA MEGA SENA"; 
              menu (); 
              break; 
 
          Caso 2: 
              $ Jogo = "quina"; 
              break; 
 
          case 3: 
              $ Jogo = "Lotomania"; 
              break; 
 
          Caso 4: 
              $ Jogo = "lotofácil"; 
              break; 
 
          Caso 5: 
              exit (); 
              break; 
 
          default: 
              echo "Opção inválida"; 
              menu (); 
 
      } 
      retornar $ Jogo; 
 } 
 
 
 Regras de função ($ Jogo) { 
      switch ($ Jogo) { 
          Caso 1: 
              $ Regras = [ 
                  'Nome' => 'Sena mega', 
                  'Possibilidades' => 60, 
                  'min' => 6, 
                  'max' => 15, 
                  'Valores' => [6 => 3,50, 7 => 24,50, 8 => 98,00, 9 => 294, 10 => 735,00,] // Terminar 
              ]; 
 
              break; 
 
      } 
 } 
 
 
 função sortear ($ Possibilidades, $ dezenas) { 
 
      $ numSorteados = []; 
 
      for ($ i = 1; $ i <= $ dezenas; $ i ++) { 
 
          $ sorteado = 0; // inicializado 
 
          fazer { 
              $ sorteado = rand (1, $ Possibilidades); 
          } While (in_array ($ sorteado, $ numSorteados)); 
 
          $ numSorteados [] = $ sorteado; 
      } 
 sort ($ numSorteados); 
      retornar $ numSorteados; 
 } 
