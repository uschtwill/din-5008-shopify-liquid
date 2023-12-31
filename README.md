# din-5008-shopify-liquid

## About

This is a repository of [DIN-5008](https://de.wikipedia.org/wiki/DIN_5008) conformant [liquid templates](https://shopify.dev/docs/api/liquid) for [Shopify](https://shopify.dev/docs).

_"Lol, why?"_

Because in Germany we have envelopes and 'shipping bags' with little windows in them, and you need the shipping address to be in the right place for it to be visible in that window. And being DIN-5008 conformant ensures that. Also, you need to fold the paper in a specific way (that's what the markings on the left edge are for). True story.

Anyways, so far, we have the [packing slip](https://help.shopify.com/en/manual/shipping/setting-up-and-managing-your-shipping/packing-slips-variable-list).

It looks like this:

> ![Packing Slip](packing-slip/packing-slip-example.png)

## Caveats

- The packing slip liquid works for orders/fulfillments that are not longer than a DIN-A4 page. If you have more items, leading to the content breaking to a second page, you need to adjust this template, otherwise things will break. Removing the height on the `.din-5008` class and then fixing things up probably will be enough. But our current use case doesn't require this, so we didn't bother. If you fix this, please submit a PR.
- When printing, make sure you print at 100%. Some prining software (looking at you MacOS) wants to scale the PDF, which will lead to things being slightly off.

## Acknowledgements

Thanks and shoutout to [@Xiphe](https://github.com/Xiphe), [whose work](https://github.com/Xiphe/din-5008-css/tree/master) this is based on.
