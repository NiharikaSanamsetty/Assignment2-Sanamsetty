# Assignment2-Sanamsetty
# SANAMSETTY NIHARIKA
###### Hyderabad

Hyderabad is the capital and largest city of the South Indian state of Telangana. It was ruled by the Qutub Shahis, Mughals and the Nizams which shaped its history. The city is noted for its monuments which includes the masterpiece of Charminar and the fort of Golconda. There are a multitude of masjids, temples, churches and bazaars in the city.

**LOVE THE WAY YOU LIVE**

# ROUTE FROM LOS ANGELES TO KANSAS CITY
1. Start from Los Angeles
    1. Head southeast on W 1st St toward N Main St
    2. Turn left onto N Main St
    3. Turn right onto W Aliso St
    4. Use the left 2 lanes to merge onto US-101 S via the ramp to I-10 E/I-5 S
2. Follow I-15 N and I-70 E to S 14th St in St. Louis. Take exit 39A from I-64 E
    1. Merge onto US-101 S
    2. Keep left at the fork to continue on San Bernardino Fwy, follow signs for I-10 E/San Bernardino
    3. Continue onto I-10 E/San Bernardino Fwy
    4. Keep left to stay on I-10 E
    5. Use the right 2 lanes to take exit 58A to merge onto I-15 N/Ontario Fwy toward Barstow/Las Vegas
    6. Take exit 39A for 14th St
3. Use Oak St to your destination
    1. Turn left onto Page St
    2. Turn left
    3. Turn right
4. Kansas City is arrived

* Fruits
    * Strawberry
    * Papaya
    * Green Apple
* Salad
* French Fries
* Veggies
    * Potato
    * Beetroot
* Grilled Chicken
* Scrambled Eggs

Hip Hip Hurray.. Let's see this **[Git](AboutMe.md)**
***
## FOOD/DRINK TABLE
 Here is the table for drinks we are introducing that everyone should try as you will definitely enjoy it. There are 3 columns which shows the info about the Type of drink, Location and Amount to be paid.
|  Food/Drink    |  Location    |  Amount    |
| ---               |  ---         |  ---       |
| Pasta             |  Store1      |   $5.6     |
| Burger            |  McD         |   $2.5     |
| Sprite            |  Union-1     |   $1.9     |
| Coke              |  Dining-5    |   $1.8     |
***
## PITHY QUOTES
> “I have only made this letter longer because I have not had the time to make it shorter." -  *Blaise Pascal*

> “What's really important here," I whispered loudly to myself,"is not the big things other people have thought up, but the small things you, yourself have.” - *Haruki Murakami*
***
## CODE FENCING(GRAPH FLOWS/MATCHINGS/MISC)
> Flow graph is a directed graph. It contains the flow of control information for the set of basic block. A control flow graph is used to depict that how the program control is being parsed among the blocks. It is useful in the loop optimization. <https://www.javatpoint.com/flow-graph>

```
const int INF = 1000000000;
vector<vector<pair<int, int>>> adj;

void dijkstra(int s, vector<int> & d, vector<int> & p) {
    int n = adj.size();
    d.assign(n, INF);
    p.assign(n, -1);
    vector<bool> u(n, false);

    d[s] = 0;
    for (int i = 0; i < n; i++) {
        int v = -1;
        for (int j = 0; j < n; j++) {
            if (!u[j] && (v == -1 || d[j] < d[v]))
                v = j;
        }

        if (d[v] == INF)
            break;

        u[v] = true;
        for (auto edge : adj[v]) {
            int to = edge.first;
            int len = edge.second;

            if (d[v] + len < d[to]) {
                d[to] = d[v] + len;
                p[to] = v;
            }
        }
    }
}
```

Source Code <https://cp-algorithms.com/graph/dijkstra.html>