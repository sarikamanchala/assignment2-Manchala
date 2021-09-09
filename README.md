# assignment2-Manchala
# Sarika manchala
######  India
It is one of my favourite place since childhood . **India** is known for being one of the most beautiful and serene place on earth.  It is the __seventh-largest__ country by area, the second-most populous country, and the most populous democracy in the world.

---

## Directions to my favourite place
1. Book a cab from maryville to kansas
2. Fly from kansas to Chicago
3. Travel from chicago to India for a huge time in a fight 
4. After Reaching India we can use local transport like :
    1. Flights
    2. Trains
    3. Buses
    4. Autos
5. I prefer to use Trains in india and reach my favaurite place Hyderabad in India
6. Things i do for maximum enjoyment
    * Meeting friends
    * Playing
    * Reading

[AboutMe](AboutMe.md)

---

# food Table

following table describes food items lsweets which are famous in India
| Name | Location | Cost |
| --- | --- | --- |
| Kaja | Kakinada| $50 |
| Jilebhi | Karimnagar| $40 |
| putharekhulu | Palakollu| $70|
| Laddu | Thirapathi | $100|

---

# Pity Quotes
>Every motherworks hard, and every women deserves to be respected *MichelleObama*

>The greatest glory in living lies not in never falling, but in rising every time we fall. *Nelson Mandela*

---

# Code Fencing
>A spanning tree of that graph is a subgraph that is a tree and connects all the vertices together. A single graph can have many different spanning trees. A minimum spanning tree (MST) or minimum weight spanning tree for a weighted, connected, undirected graph is a spanning tree with a weight less than or equal to the weight of every other spanning tree. The weight of a spanning tree is the sum of weights given to each edge of the spanning tree.

Link to Minimum spanning tree - Kruskal's algorithm : <https://www.geeksforgeeks.org/kruskals-minimum-spanning-tree-algorithm-greedy-algo-2/>
```
struct Edge {
    int u, v, weight;
    bool operator<(Edge const& other) {
        return weight < other.weight;
    }
};

int n;
vector<Edge> edges;

int cost = 0;
vector<int> tree_id(n);
vector<Edge> result;
for (int i = 0; i < n; i++)
    tree_id[i] = i;

sort(edges.begin(), edges.end());

for (Edge e : edges) {
    if (tree_id[e.u] != tree_id[e.v]) {
        cost += e.weight;
        result.push_back(e);

        int old_id = tree_id[e.u], new_id = tree_id[e.v];
        for (int i = 0; i < n; i++) {
            if (tree_id[i] == old_id)
                tree_id[i] = new_id;
        }
    }
}
```
Link to the source code : <https://cp-algorithms.com/graph/mst_kruskal.html>





