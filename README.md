# the-first-one

#2.0版本及以上session使用
import tensorflow as tf
tf.compat.v1.disable_eager_execution()

matrix1 = tf.constant([[3,3]])
matrix2 = tf.constant([[2],
                       [2]])
product = tf.matmul(matrix1,matrix2) # matmul 即为 matrix multiply(矩阵乘法)

#method1
sess = tf.compat.v1.Session()
result = sess.run(product)
print(result)
sess.close()

#method2
#with tf.Session() as sess
 #   result2=sess.run(product)
  #  print(result2)
