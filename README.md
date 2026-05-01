# pensamento_computacional-g1

Você foi contratado para desenvolver a lógica de um sistema automatizado utilizado em uma máquina que realiza o controle de uma comporta mecânica, representada por um servo motor.
O operador controla o sistema por meio de um botão de iniciar. Além disso, o sistema possui dois potenciômetros que influenciam diretamente o funcionamento.
O primeiro potenciômetro será utilizado para definir o tempo de execução do processo. Esse valor varia de 0 a 1023 e deve ser interpretado pelo sistema como um tempo entre 1 e 10 segundos, onde valores menores representam tempos mais curtos e valores maiores representam tempos mais longos.
Ao pressionar o botão iniciar, o sistema deve ler esse valor e iniciar o processo. Durante esse período, o servo motor deve se mover para uma posição de funcionamento (por exemplo, abrir a comporta) e permanecer nessa posição durante o tempo definido. Após esse tempo, o servo deve retornar à posição inicial (fechar a comporta).
Durante o funcionamento, o sistema deve indicar seu estado por meio de LEDs:
LED vermelho → sistema parado
LED amarelo → processo em execução
LED verde → processo finalizado
Além disso, o segundo potenciômetro será utilizado para definir a posição de abertura do servo motor. Esse valor deve ser convertido para um ângulo (por exemplo, entre 0° e 180°), determinando o quanto a comporta será aberta.
Durante os testes, foi observado que o operador pode pressionar o botão de iniciar em momentos inadequados, como tentar iniciar o sistema enquanto ele já está em execução. O sistema deve tratar essa situação, evitando reiniciar o processo enquanto ele ainda estiver em andamento.

Identifique as entradas e saídas do sistema 
Apresente todos os componentes do sistema e para que eles servem
Apresente as regras de funcionamento a serem implementadas
Explique como você utilizaria estruturas if para controlar o sistema

A) 
1° entrada - botão
2° entrada - Potênciometro 1
3° entrada - Potênciometro 2

1° Saída - led vermelho
2° Saída - Led verde
3° Saída - Led amarelo
4­° Saída - Servo motor

B) 
Botão - Ele liga o sistema
Potênciometro 1 - Ele dita o tempo que o sistema ira rodar
Potênciometro 2 - Ele define a ângulagem do servo motor

Led vermelho - Significa que o sistema está parado
Led verde - Significa que o ciclo do sistema está concluido
Led amarelo - Significa que o sistema está em movimento
Servo motor - Simula um comporta(abre e fecha)

C) 
Enquanto o botão não for precionado o sistema não deve ligar, apenas o led vermelho deve estar acesso.
Quando o botão for acionado o sistema deve ler os indicadores dos potênciometros e mover o servo motor, paralelamente o led vermelho ira ligar e o amarelo ira acender.
Quando o sistema concluir, o botão amarelo ira desligar e o verde ira ser acionado.
O botão não pode ser acionado até que o ciclo se acabe
quando o ciclo acabar é preciso que tudo volte para a etapa um. O servo motor voltara para zero e o led verde ira desligar, com o led vermelhor ligando novamente

D)
IF botão = 0 -- Sistema desligado e led vermelho ligado
IF botão = 1 -- Sistema ligado

IF potênciometro 1 > 100 -- 1s
IF potênciometro 1 < 100 > 200 -- 2s
IF potênciometro 1 < 200 > 300 -- 3s
IF potênciometro 1 < 300 > 400 -- 4s
IF potênciometro 1 < 400 > 500 -- 5s
IF potênciometro 1 < 500 > 600 -- 6s
IF potênciometro 1 < 600 > 700 -- 7s
IF potênciometro 1 < 700 > 800 -- 8s
IF potênciometro 1 < 800 > 900 -- 9s
IF potênciometro 1 < 900 > 1023 -- 10s

IF potênciometro 2 = 45 -- 45°
IF potênciometro 2 = 90 -- 90°
IF potênciometro 2 = 135 -- 135°
IF potênciometro 2 = 180 -- 180°

IF sistema em movimento = Led vermelho desliga e o amarelo acende - apertar botão é ignorado
IF sistema sem movimento = led amarelo desliga e o verde acende








