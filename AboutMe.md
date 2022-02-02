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


# Code fencing usage for the Dynamic Programming
> Dynamic Programming is an algorithmic technique for solving a problem by recursively breaking it down into simpler subproblem.
Link source<https://www.interviewbit.com/courses/programming/topics/dynamic-programming/>
```
int m, n;
vector<long long> dp_before(n), dp_cur(n);

long long C(int i, int j);

// compute dp_cur[l], ... dp_cur[r] (inclusive)
void compute(int l, int r, int optl, int optr) {
    if (l > r)
        return;

    int mid = (l + r) >> 1;
    pair<long long, int> best = {LLONG_MAX, -1};

    for (int k = optl; k <= min(mid, optr); k++) {
        best = min(best, {(k ? dp_before[k - 1] : 0) + C(k, mid), k});
    }

    dp_cur[mid] = best.first;
    int opt = best.second;

    compute(l, mid - 1, optl, opt);
    compute(mid + 1, r, opt, optr);
}

int solve() {
    for (int i = 0; i < n; i++)
        dp_before[i] = C(0, i);

    for (int i = 1; i < m; i++) {
        compute(0, n - 1, 0, n - 1);
        dp_before = dp_cur;
    }

    return dp_before[n - 1];
}
```
Link source< https://cp-algorithms.com/index.html>