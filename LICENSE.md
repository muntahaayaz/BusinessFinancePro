# License

## Recommendation

Business Finance Pro is a commercial product intended for sale (per the original product requirements: a $49–99 one-time-purchase Excel product), not an open-source project. A standard open-source license (MIT, Apache 2.0, GPL, etc.) would be a poor fit — those licenses grant redistribution and modification rights that directly undermine a paid, single-purchase product.

**Recommended approach: a proprietary End-User License Agreement (EULA)**, not an open-source license. A short template appropriate for this kind of product is below. This is a starting point for discussion with an actual lawyer before commercial use, not a finished legal document — I'm not a lawyer, and licensing terms should be reviewed by one before you rely on them.

---

## Suggested EULA Template

```
BUSINESS FINANCE PRO — END-USER LICENSE AGREEMENT

Copyright (c) [year] [your name / business name]. All rights reserved.

This workbook ("the Software") is licensed, not sold. Purchase of the
Software grants the purchaser a non-exclusive, non-transferable license to:

  1. Use the Software for their own business's internal financial tracking.
  2. Make copies of the Software solely for personal backup purposes.

The purchaser MAY NOT, without prior written permission:

  1. Resell, redistribute, sublicense, or share the Software or any
     derivative of it, in whole or in part.
  2. Remove or alter any copyright, branding, or attribution notices.
  3. Use the Software to build a competing commercial product or template.

The Software is provided "as is," without warranty of any kind, express or
implied. In no event shall the author be liable for any claim, damages, or
other liability arising from the use of the Software, including but not
limited to errors in financial calculations. This product does not
constitute financial, tax, accounting, or legal advice — consult a
qualified professional for guidance specific to your business.
```

## Why Not Open Source

If a future decision is made to open-source part of this project (for example, publishing the architecture and calculation-engine design as a portfolio/teaching reference, separate from selling the finished workbook itself), a permissive license like MIT would be appropriate for that *documentation and design pattern*, while the finished `.xlsx` product itself remains under the proprietary EULA above. These are two different artifacts and can carry two different licenses.

## For This Repository Specifically

If this repository is being used as a **portfolio piece** (showcasing the build process rather than selling the product), consider:
- Keeping the `.xlsx` workbook itself out of a public repository, or watermarking/limiting the seed data in any publicly-shared copy
- Publishing the documentation, architecture diagrams, and process writeups (this release package) under a permissive license, since that content demonstrates process and skill rather than being the sellable product itself
- Adding a clear statement to the README: "This repository showcases the design and engineering process behind Business Finance Pro. The workbook itself is a commercial product — see LICENSE.md for terms."
