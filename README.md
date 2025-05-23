           
           // Генерируем новые случайные позиции
           bombPositions = [];
           while (bombPositions.length < bombCount) {
               const row = Math.floor(Math.random() * boardSize);
               const col = Math.floor(Math.random() * boardSize);
               const pos = `${row},${col}`;
               
               if (!bombPositions.includes(pos)) {
                   bombPositions.push(pos);
                   const cell = document.querySelector(`.cell[data-row="${row}"][data-col="${col}"]`);
                   cell.classList.add('bomb');
               }
           }
       }
 
       function goTo1Win() {
           window.open('https://dzen.ru/?clid=2411725&yredirect=true', '_blank');
       }
 
       // Инициализация при загрузке
       createBoard();
       // Выделяем кнопку 3 бомбы по умолчанию
       bombButtons[1].classList.add('active');
   </script>
</body>
</html>
