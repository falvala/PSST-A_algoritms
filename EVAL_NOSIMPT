
function [seleccionNOSIMP]= EVAL_NOSIMPT (matsuj);

%crit1- al menos 1 de  #1 a #4 debe ser valor 4 (TDPM) y 3
%(SPM)
matcri1= matsuj(:, 1:4);
cri1= abs(matcri1)>=3; 
totcri1= sum(cri1,2);
selec1= totcri1~=0;
clear matcri1 totcri1 cri1

%crit2- ademas al menos 4 de #1 a #14 debe ser valor 4 (TDPM) o 3 (SPM)
matcri2= matsuj(:, 1:14);
cri2= abs(matcri2)>=3;
totcri2= sum(cri2,2);
selec2= totcri2~=0;
clear matcri2 totcri2 cri2

%crit3- ademas uno de A,B,C,D o E tiene valor 4 (TDPM) o 3 (SPM)
matcri3= matsuj(:, 15:18);
cri3= abs(matcri3)>=3;
totcri3= sum(cri3,2);
selec3= totcri3~=0;
clear matcri3 totcri3 cri3

%concatenar matriz con selec1, selec2 y selec3
diagn=[];
diagn(:,1)= selec1;
diagn(:,2)= selec2;
diagn(:,3)= selec3;
totcriS= sum(diagn,2);
selectionsimp= totcriS==3;% en este punto solo necesito que me devuelva la fila en la que hay un uno.

%coge a las que no cumplen criterios TDPM, SPM
selectionsimpfree = selectionsimp==0;

end
