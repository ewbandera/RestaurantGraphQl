# RestaurantGraphQl
Title:  RestaurantGraphQl Exercise
Description:  A Demonstration of the graph QL usage and query building for basic CRUD operations
How To Run:  Install npm.  Then node index.js.  After that go to browser and localhost:5500/graphql.  In there experiment with queries example queries below
License:MIT
query getrestaurant($iid: Int!)
{
  restaurant(id:$iid) {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}
query getrestaurants {
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}
mutation setrestaurant($rest:restaurantInput) {
  setrestaurant(input:$rest)
  {
    id
    name
    description
  }
}
mutation deleterestaurant($iid: Int!)
{
  deleterestaurant(id:$iid){
    ok
  }
}
mutation editrestaurant($editid: Int!,$editname:String!) {
  editrestaurant(id: $editid, name: $editname )
  {
     name
     description
  }
}