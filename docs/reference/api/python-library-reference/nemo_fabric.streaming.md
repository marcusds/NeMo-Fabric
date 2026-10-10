---
title: "Relay Streaming"
slug: "/reference/api/python-library-reference/streaming"
description: "Consume raw NVIDIA NeMo Relay ATOF records and terminal invocation results."
---
<!-- SPDX-FileCopyrightText: Copyright (c) 2026, NVIDIA CORPORATION & AFFILIATES. All rights reserved.
SPDX-License-Identifier: Apache-2.0 -->

# <kbd>module</kbd> `nemo_fabric.streaming`

NeMo Relay streaming support for the NVIDIA NeMo Fabric Python SDK.



---


## <kbd>class</kbd> `InvokeStream`

Async iterator of raw ATOF records for one runtime invocation.

Consume the final normalized result separately with :meth:`result`. If iteration stops early, call :meth:`aclose` before starting another turn.




---


### <kbd>method</kbd> `aclose`

```python
async def aclose(cancel: 'bool' = False) -> None
```

Stop iteration and drain this turn.



**Args:**

 - <b>`cancel`</b>:  Interrupt the running turn instead of waiting for it to finish. The runtime is stopped as it is when ``invoke()`` is cancelled.

---


### <kbd>method</kbd> `result`

```python
async def result() -> RunResult
```

Return the terminal normalized result without adding it to the stream.




---

_This file was automatically generated via [lazydocs](https://github.com/ml-tooling/lazydocs)._
