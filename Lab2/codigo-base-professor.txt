.data
# Seção 1: variáveis f, g, h, i, j  armazenadas em memória (inicialização)
_f: .word 1
_g: .word 2
_h: .word 4
_i: .word 8
_j: .word 16

# Seção 2: jump address table
jat: 
.word L0 
.word L1 
.word L2 
.word L3
.word L4
.word default

.text
.globl main
main:
# Seção 3: registradores recebem valores inicializados 
lw $s0, _f
lw $s1, _g
lw $s2, _h
lw $s3, _i
lw $s4, _j

la $t4, jat # carrega em $t4 o endereco-base de jat

# Seção 4: testa se k no intervalo [0,4]
sltiu $t3, ...
b... $t3, ...
                                                                                
# Seção 5: calcula o endereço de jat[k]
...                                   

# Seção 6: desvia para o endereço em jat[k]
...                                

# Seção 7: codifica as alternativas de execução
L0:    ...
L1:    ...
L2:    ...
L3:    ...
L4:    ...
default:sub $s0, $s3, $s5 #f = i - k + 5
        addi $s0, $s0, 5
Exit:   nop
