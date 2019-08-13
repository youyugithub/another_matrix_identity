# another_matrix_identity

```
Sigmae<-diag(runif(10))
Sigmab<-matrix(NA,5,5)
Sigmab<-0.8^abs(row(Sigmab)-col(Sigmab))
X<-matrix(runif(50),10,5)

A<-solve(Sigmab)-solve(Sigmab)%*%solve(t(X)%*%solve(Sigmae)%*%X+solve(Sigmab))%*%solve(Sigmab)
B<-t(X)%*%solve(X%*%Sigmab%*%t(X)+Sigmae)%*%X

A-B
```
