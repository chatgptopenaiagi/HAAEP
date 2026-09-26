# GPU Compute Plane

Status: **CONCEPT / RESEARCH DIRECTION**. No GPU detection, workload routing, CUDA/cuDNN support, or GPU playground exists in HAAEP.

The future GPU Compute Plane should explain and expose accelerator capabilities to both AI workflows and humans. Possible technologies include CUDA, cuDNN, PyTorch, TensorRT, ROCm, DirectML, and future accelerators. Listing a technology is not a compatibility promise.

## Evidence questions

| Layer | Questions a future adapter may answer |
|---|---|
| Device | Which GPU, architecture, memory capacity, and device identity are observed? |
| Driver | Which driver and supported interfaces are visible to this process? |
| Runtime/toolkit | Which runtime or toolkit is present, active, and available to the task? |
| Libraries/framework | Which cuDNN or framework build is active, and what does it require? |
| Workload | What capabilities and memory does this exact task require? |
| Context | Is execution native, in WSL, or in a container, and is device access verified there? |
| Availability | What resources are currently available, reserved, or unknown? |

Driver capability, installed toolkit version, framework build, and workload compatibility are different facts. A GPU visible on the host does not prove availability in WSL or a container. A successful inventory does not prove inference or training will succeed.

Observations need time, producer, environment scope, provenance, and explicit gaps. A compatibility conclusion should identify the tested capability and evidence rather than relying only on a product name or version string.

## AI face and human playground

The AI face may expose inventory, compatibility queries, resource estimates, and explicitly authorized bounded workloads. A human playground may show device/resource state, explain compatibility gaps, compare a small experiment before and after, and allow cancellation.

The Chocolate Rule calls for a useful human experience of the work. A dashboard should answer an actual question such as “Can this chosen workload run here, and what remains unverified?” rather than displaying impressive but unexplained metrics.

## Safety and verification

- Inspection and workload execution are separate capabilities and permissions.
- Experiments need bounded duration, memory, concurrency, and an explicit task scope.
- Driver changes, toolkit installation, environment edits, and device passthrough configuration are separate consequential operations.
- A cancelled workload may take time to release resources; verification must report the observed state.
- Historical utilization and resource availability must not be presented as current facts.
- No broad security weakening, automatic installation, or global reconfiguration follows from detecting an incompatibility.

A first implementation should address one real read-only inventory or compatibility question with a small verified environment matrix. Performance benchmarking, training management, and multi-device scheduling require separate evidence and blocks.

See [local AI direction](LOCAL_AI.md), [runtime plane](RUNTIME_PLANE.md), [OS plane](OS_PLANE.md), [playground contract](PLAYGROUND_CONTRACT.md), and [security model](SECURITY_MODEL.md).
