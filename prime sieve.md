#define N 100000
typedef long long ll;

vector<ll> sieve(N,0);

void PRIMESIEVE(vector<ll> &sieve)
{
    sieve[0] = sieve[1] = 0;
    sieve[2] = 1;

    for(ll i = 3; i <= N; i = i + 2)
    {
        
        sieve[i] = 1;
    }

    for(ll i = 3; i <= N; ++i)
    {
       if(sieve[i])
       {
           for(ll j = i*i; j <= N; j = j + i)
           {
              sieve[j] = 0;
           }
       }
    }
}
