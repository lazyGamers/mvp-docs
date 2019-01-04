# Map

Map is comprised of multiple provinces.

## Province
Province is an abstract entity, comprised of towns. It is under control of one kingdom. Each province has its own climate, geography and natural resource.

## Town

Town is an entity where characters can take residence and use functions according to type of town.
There are following types of towns:

| Type     | Leader |  Function         |  Communal buildings                      | Purchasable buildings | Description                                       |
|----------|--------|-------------------|------------------------------------------|-----------------------|---------------------------------------------------|
| Village  | x      | farming           | Wooden board, church                     | farm, field, house    |  town for gathering resources                     |
| City     | Mayor  | manufactoring     | town hall, market, church, court, prison | shop, house           | town for producing goods                          |
| Port     | Mayor  | travel            | docks                                    | house, pier           | town for travelling on sea to other places        |
| Bishopry | Bishop | clerical          | cathedral, abbey                         | house                 | town for religious activities                     |
|  Castle  | Noble | military          | castle, barracks, walls, quarters        | armorer, shieldmaker  | town for producing military equipment and defence |
| Capital  | King   | center of kingdom | palace, court, prison, walls             | house                 | town for king's actions                           |

More in [town page](https://github.com/lazyGamers/mvp-docs/blob/master/kingdoms/towns.md)

## Province composition

Each province contains at least one town. Town type can be changed with build action. Town can also be abandoned (if it is not the last town in province).
King can also contruct new towns. Having too many towns negatively affects income from that province.

## Province revenue
Each province generates X silver per week.
If there are more towns than there are people in province, the X amount is lowered (min 0).

To get an acceptable number of towns you calculate:

`T = max(1, floor(P / 3))`, where P is province population.

Example: province has 10 people --> 3 towns, province has 1 person --> 1 town, province has 0 people --> 1 town (but X = 0)

For each town over the limit the X amount is reduced by 20%.

## Travelling
Travelling inside province is fast (I), from one province to another takes longer (O = 8 x I).

### Sea routes
It is possible to travel by sea, but only from one port to other connected ports (TBD: connections pre-defined, or player-defined?)

# Analysis
* mvp: map with provinces, map with towns, travel, sea travel
* phase 1: province revenue