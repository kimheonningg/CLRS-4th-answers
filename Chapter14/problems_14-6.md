If **root r is included**-> solve the subproblem of the tree with the **grandchild** of r as a root

If **root r is not included**-> solve the subproblem of the tree with the **child** of r as a root

Define C[x] = max conviviality score in a subtree with root x.

Define G[x] = the guest list when C[x]

C[x] = max {x.conviviality + ∑{y is a grandchild of x} C[y], ∑{y is a child of x} C[y]}
