# CNN-size

Osize 	= floor((Isize - Ksize + 2Psize)/Ssize) + 1				
	=floor((227-11+2*0,1)/4)+1				
	=55				
					
Npam = Csize_previous * Csize_current * (Ksize^2 + 1)					
	＝96*3*（11*11+1）				
	=35136				
		
		
		
学習＆評価時
学習率(learning_rate)とは、機械学習の最適化においてどのくらい値を動かすかというパラメーター。学習率を大きくしすぎると発散し、小さくしすぎると収束まで遅くなる。


学習時
ドロップアウト率を渡してあげる必要があり、学習時には、0.5（KEEP_PROB）を設定。

		sess.run(train_step, {x: batch[0], y_: batch[1], keep_prob: KEEP_PROB})

評価時には、ドロップアウトさせない1.0（KEEP_PROB）を設定。

                summary = sess.run(tf.merge_summary([train_accuracy_summary]), {x: batch[0], y_: batch[1], keep_prob: 1.0})
                summary = sess.run(tf.merge_summary([test_accuracy_summary]), {x: mnist.test.images, 
