---
id: withdraw-exit-faster
title: withdrawExitFaster
keywords:
- 'plasma client, erc721, withdrawExitFaster, polygon, sdk'
description: 'MATICJS দিয়ে শুরু করুন'
---

# withdrawExitFaster {#withdrawexitfaster}

সবগুলো টোকেন অনুমোদন করার জন্য `withdrawExitFaster`পদ্ধতি ব্যবহার করা যাবে।

এটি দ্রুত কারণ এটি ব্যাকএন্ডে প্রমাণ তৈরি করে। নিবেদিত প্রাইভেট rpc-র মাধ্যমে ব্যাকএন্ড কনফিগার করা যেতে পারে।

**দ্রষ্টব্য**- উইথড্র থেকে বেরিয়ে আসার জন্য withdrawStart লেনদেনটি অবশ্যই চেকপয়েন্ট করতে হবে।

```
const erc721RootToken = plasmaClient.erc721(<root token address>, true);

const approveResult = await erc721RootToken.withdrawExitFaster(<burn tx hash>);

const txHash = await approveResult.getTransactionHash();

const txReceipt = await approveResult.getReceipt();

```