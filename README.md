# base-unit-trait-fortifies

The `Fortifies` unit trait: a unit type with it can fortify.

A unit type with this trait can be given the fortify order.

For example: Civ1: every unit that extends `Fortifiable` (including Diplomat and Caravan).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Fortifies)`:

```ts
import Fortifies from '@civ-clone/base-unit-trait-fortifies/Fortifies';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Fortifies));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
