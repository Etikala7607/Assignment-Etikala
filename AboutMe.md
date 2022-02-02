## Etikala Sravankumar
Hi, iam from Hyderabad India. I completed my Bachelors degree in CS in JNTUH and my passion for learning brought me here to pursue MS in US.

![Sravan](/Sravan.jpg)
*************************************************************************
|Sport|Location|Amount|
|---|---|---|
|Chess|INDIA|$100|
|Cricket|INDIA|$300|
|BasketBall|USA|$600|
|Badminton|USA|$400|
*************************************************************************
Be happy and stay happy
>  ~ *Mae West*

The real happiness lies in success
>  ~ * Ashok Babu*
*************************************************************************
# Code fencing usage for the Numerical methods
> Numerical method is the approach of solving mathematical or physical equations using computers.
Link source <https://www.sciencedirect.com/topics/engineering/numerical-method>
```
double ternary_search(double l, double r) {
    double eps = 1e-9;              
    while (r - l > eps) {
        double m1 = l + (r - l) / 3;
        double m2 = r - (r - l) / 3;
        double f1 = f(m1);      
        double f2 = f(m2);      
        if (f1 < f2)
            l = m1;
        else
            r = m2;
    }
    return f(l);                
}
```
Link source< https://cp-algorithms.com/index.html>