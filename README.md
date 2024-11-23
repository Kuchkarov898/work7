//problem1
void days2years(int &days, int &years) {
    years=days/365;
    days=days%365;

}
// Problem 2
double func(double *x,double *y) {
    *y=(11*pow(*x,3))/3+5;
return *y;
}


// Problem 3
int minsNewYear(int *hour, int *min) {
    int totalMinutes=24*60;
    int currentMinutes=*hour*60+(*min);
    return totalMinutes-currentMinutes;
}

// Problem 4
double probability(int *A, int *B) {
    int countWins = 0, totalOutcomes = 36;
    for (int a = 1; a <= 6; a++) {
        for (int b = 1; b <= 6; b++) {
            if (a > *A && a > *B) countWins++;
        }
    }
    return static_cast<double>(countWins) / totalOutcomes;
}

// Problem 5
int presses(int *x) {
    int keypresses = 0;
    int d = *x % 10;
    int n = 0, temp = *x;
    while (temp > 0) {
        n++;
        temp /= 10;
    }
    for (int i = 1; i <= d; i++) {
        for (int len = 1; len <= (i == d ? n : 4); len++) {
            keypresses += len;  
        }
    }

    return keypresses;
}
#ifndef PROBLEMS_H
#define PROBLEMS_H

#endif //PROBLEMS_H
