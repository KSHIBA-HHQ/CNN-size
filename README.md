# CNN-size

Osize 	= floor((Isize - Ksize + 2Psize)/Ssize) + 1				
	=floor((227-11+2*0,1)/4)+1				
	=55				
					
Npam = Csize_previous * Csize_current * (Ksize^2 + 1)					
	＝96*3*（11*11+1）				
	=35136				
					
学習率とは、機械学習の最適化においてどのくらい値を動かすかというパラメーター。学習率を大きくしすぎると発散し、小さくしすぎると収束まで遅くなる。

