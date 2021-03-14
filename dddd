#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int getCommand(char * inp) {
    char command[4];
    command[0] = inp[0];
    command[1] = inp[1];
    command[2] = inp[2];
    command[3] = '\0';
    if (!strcmp(command, "mov") ) {
        return 0;
    }
    if (!strcmp(command, "add") ) {
        return 1;
    }
    if (!strcmp(command, "sub") ) {
        return 2;
    }
}

int getReg(char * inp) {
    char reg[4];
    reg[0] = inp[4];
    reg[1] = inp[5];
    reg[2] = inp[6];
    reg[3] = '\0';
    if (!strcmp(reg, "eax") ) {
        return 0;
    }
    if (!strcmp(reg, "ebx") ) {
        return 1;
    }
    if (!strcmp(reg, "ecx") ) {
        return 2;
    }
    if (!strcmp(reg, "edx") ) {
        return 3;
    }
}
int gettt(char * inp) {
    char reg[4];
    reg[0] = inp[9];
    reg[1] = inp[10];
    reg[2] = inp[11];
    reg[3] = '\0';
    if (!strcmp(reg, "eax") ) {
        return 0;
    }
    if (!strcmp(reg, "ebx") ) {
        return 1;
    }
    if (!strcmp(reg, "ecx") ) {
        return 2;
    }
    if (!strcmp(reg, "edx") ) {
        return 3;
    }

}
//mov eax, ebx
//mov eax, 1
#define MAX_SIZE 100
int main() {
    int eax; //a
    int ecx; //b
    int ebx; //c
    int edx; //d
    char *inp = (char *) malloc(MAX_SIZE * sizeof(char));
    while(1) {
        fgets(inp, MAX_SIZE, stdin);
        if (inp[0] == '0') {
            break;
        }
        switch(getCommand(inp)) {
            case 0: // mov
                switch(getReg(inp) ){
                    case 0: // eax

                        if(inp[9] <= '9' && inp[9] >= '0') { // mov eax, number
                            eax = atoi(inp + 9);
                        } else { // not a number
                            switch (gettt(inp)) {
                                case 0: // mov eax, eax
                                    eax = eax;
                                    break;
                                case 1: // mov eax, ebx
                                    eax = ebx;
                                    break;
                                case 2: //mov eax, ecx
                                    eax = ecx;
                                    break;
                                case 3: // mov eax, edx
                                    eax = edx;
                                    break;
                            }
                        }
                        break;
                    case 1: //ebx
                        if(inp[9] <= '9' && inp[9] >= '0') { // mov ebx, number
                            ebx = atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // mov ebx, eax
                                    eax = eax;
                                    break;
                                case 1: // mov ebx, ebx
                                    ebx = ebx;
                                    break;
                                case 2: //mov ebx, ecx
                                    ebx = ecx;
                                    break;
                                case 3: // mov ebx, edx
                                    ebx = edx;
                                    break;
                            }
                        }
                        break;
                    case 2: //ecx
                        if(inp[9] <= '9' && inp[9] >= '0') { // mov ecx, number
                            ecx = atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // mov ecx, eax
                                    ecx = eax;
                                    break;
                                case 1: // mov ecx, ebx
                                    ecx = ebx;
                                    break;
                                case 2: //mov ecx, ecx
                                    ecx = ecx;
                                    break;
                                case 3: // mov ecx, edx
                                    ecx = edx;
                                    break;
                            }
                        }
                        break;
                    case 3://edx
                        if(inp[9] <= '9' && inp[9] >= '0') { // mov edx, number
                            edx = atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // mov edx, eax
                                    edx = eax;
                                    break;
                                case 1: // mov edx, ebx
                                    edx = ebx;
                                    break;
                                case 2: //mov edx, ecx
                                    edx = ecx;
                                    break;
                                case 3: // mov edx, edx
                                    edx = edx;
                                    break;
                            }
                        }
                        break;
                }
                break;
            case 1: // add
                switch(getReg(inp) ){
                    case 0: // eax
                        if(inp[9] <= '9' && inp[9] >= '0') { // add eax, number
                            eax += atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // add eax, eax
                                    eax += eax;
                                    break;
                                case 1: // add eax, ebx
                                    eax += ebx;
                                    break;
                                case 2: //add eax, ecx
                                    eax += ecx;
                                    break;
                                case 3: // add eax, edx
                                    eax += edx;
                                    break;
                            }
                        }
                        break;
                    case 1: //ebx
                        if(inp[9] <= '9' && inp[9] >= '0') { // add ebx, number
                            ebx +=atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // mov ebx, eax
                                    eax += eax;
                                    break;
                                case 1: // add ebx, ebx
                                    ebx += ebx;
                                    break;
                                case 2: //add ebx, ecx
                                    ebx += ecx;
                                    break;
                                case 3: // add ebx, edx
                                    ebx += edx;
                                    break;
                            }
                        }
                        break;
                    case 2: //ecx
                        if(inp[9] <= '9' && inp[9] >= '0') { // add ecx, number

                            ecx += atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // add ecx, eax
                                    ecx += eax;
                                    break;
                                case 1: // add ecx, ebx
                                    ecx += ebx;
                                    break;
                                case 2: //add ecx, ecx
                                    ecx += ecx;
                                    break;
                                case 3: // add ecx, edx
                                    ecx += edx;
                                    break;
                            }
                        }
                        break;
                    case 3://edx
                        if(inp[9] <= '9' && inp[9] >= '0') { // add edx, number

                            edx += atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // add edx, eax
                                    edx += eax;
                                    break;
                                case 1: // add edx, ebx
                                    edx += ebx;
                                    break;
                                case 2: //add edx, ecx
                                    edx += ecx;
                                    break;
                                case 3: // add edx, edx
                                    edx += edx;
                                    break;
                            }
                        }
                        break;
                }

                break;

            case 2: //sub
                switch(getReg(inp) ){
                    case 0: // eax
                        if(inp[9] <= '9' && inp[9] >= '0') { // sub eax, number

                            eax -= atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // sub eax, eax
                                    eax -= eax;
                                    break;
                                case 1: // sub eax, ebx
                                    eax -= ebx;
                                    break;
                                case 2: //sub eax, ecx
                                    eax -= ecx;
                                    break;
                                case 3: // sub eax, edx
                                    eax -= edx;
                                    break;
                            }
                        }
                        break;
                    case 1: //ebx
                        if(inp[9] <= '9' && inp[9] >= '0') { // sub ebx, number

                            ebx -= atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // sub ebx, eax
                                    eax -= eax;
                                    break;
                                case 1: // sub ebx, ebx
                                    ebx -= ebx;
                                    break;
                                case 2: //sub ebx, ecx
                                    ebx -= ecx;
                                    break;
                                case 3: // sub ebx, edx
                                    ebx -= edx;
                                    break;
                            }
                        }
                        break;
                    case 2: //ecx
                        if(inp[9] <= '9' && inp[9] >= '0') { // sub ecx, number
                            ecx -= atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // sub ecx, eax
                                    ecx -= eax;
                                    break;
                                case 1: // sub ecx, ebx
                                    ecx -= ebx;
                                    break;
                                case 2: //sub ecx, ecx
                                    ecx -= ecx;
                                    break;
                                case 3: // sub ecx, edx
                                    ecx -= edx;
                                    break;
                            }
                        }
                        break;
                    case 3://edx
                        if(inp[9] <= '9' && inp[9] >= '0') { // sub edx, number

                            edx -= atoi(inp + 9);
                        } else { // not a number
                            switch(gettt(inp)) {
                                case 0: // sub edx, eax
                                    edx -= eax;
                                    break;
                                case 1: // sub edx, ebx
                                    edx -= ebx;
                                    break;
                                case 2: //sub edx, ecx
                                    edx -= ecx;
                                    break;
                                case 3: // sub edx, edx
                                    edx -= edx;
                                    break;
                            }
                        }
                        break;
                }
                break;

        }
		
        printf("%d %d %d %d\n", eax, ebx, ecx, edx);

    }// end while


    return 0;
}
