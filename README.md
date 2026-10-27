# Skills to learn

## LLM, RAG and agents

- **LangGraph (advanced)** — human-in-the-loop interrupts before sensitive tool calls; checkpoints and durable state; supervisor and multi-agent patterns; streaming; long-running flows
- **MCP server design** — tool naming and schemas written for models; error handling and pagination; per-user auth and tool permissions; tool-use evals; cost and latency tracking per tool
- **Hybrid retrieval and reranking** — BM25 plus dense vectors; reciprocal rank fusion; cross-encoder rerankers; sparse plus dense in Qdrant; relevance tuning on real queries
- **Azure AI Search** — hybrid and semantic ranking; security trimming per user or group; indexers and incremental indexing; skillsets for chunking and embedding
- **Elasticsearch / OpenSearch vector search** — semantic_text and kNN fields; index design; document-level security; citations from hits
- **RAG data pipelines** — chunking strategies and chunk metadata; embedding refresh and idempotent upserts; re-indexing; multi-tenant filters; data contracts for document sources
- **Document understanding** — layout and table parsing (Docling); OCR fallbacks (Tesseract); extraction to Pydantic or JSON Schema; validation and retry loops; messy supplier PDFs
- **Context engineering** — what goes in the context window and when; memory and summarisation; structured output; keeping deterministic steps as plain code
- **Agent SDKs beyond LangChain** — Pydantic AI; OpenAI Agents SDK (handoffs, guardrails, tracing); Microsoft Agent Framework and Semantic Kernel; A2A agent cards versus MCP tools
- **Durable execution for agents (Temporal)** — workflows versus activities; retries and idempotency; sagas and compensation; versioning running workflows
- **Agent sandboxes** — running agent-written code in isolated sandboxes; network and filesystem limits; secrets handling
- **LLM gateways (LiteLLM)** — multi-provider routing and fallbacks; quotas and virtual keys; cost and sensitivity-based model selection; audit logging
- **Cloud GenAI services** — Azure AI Foundry deployments and evaluations; Amazon Bedrock Knowledge Bases, Agents and Guardrails; Snowflake Cortex Agents
- **Fine-tuning** — LoRA and PEFT with Hugging Face; dataset curation; when fine-tuning beats prompting or RAG; evaluating a fine-tuned model against the base
- **Speech and multimodal** — speech-to-text and text-to-speech basics; vision-language models for extraction and grounding

## Evals, guardrails and LLM observability

- **Eval harnesses** — golden datasets with edge and failure cases; LLM-as-judge and its pitfalls; groundedness, citation and tool-call checks; regression gates in CI after prompt or model changes
- **Ragas / DeepEval / promptfoo** — faithfulness, answer relevancy, context precision and recall; synthetic test sets; red-team suites
- **Langfuse / LangSmith** — traces per request and per tool call; prompt versioning; eval datasets and scores; replaying production traces; online sampling
- **OpenTelemetry for LLM apps** — spans per prompt, token and tool call; token and cost metrics; latency budgets; dashboards in Grafana
- **Guardrails** — input and output rails; prompt-injection and PII filters; tool allow-lists; NeMo Guardrails; human approval on risky actions
- **LLM security** — OWASP Top 10 for LLM apps; MITRE ATLAS; excessive agency; data leakage; jailbreak and red-team testing; least-privilege identity for agent tools
- **AI governance** — EU AI Act risk classes and documentation; NIST AI RMF; model cards; audit trails for regulated domains

## MLOps and model platform

- **Self-hosted LLM serving (vLLM)** — OpenAI-compatible server; continuous batching; quantized weights (AWQ, GPTQ, FP8); multi-LoRA; GPU memory sizing; air-gapped deploys
- **NVIDIA Triton Inference Server** — model repository; dynamic batching; ensembles; TensorRT and ONNX backends; GPU metrics
- **KServe and Open Data Hub / OpenShift AI** — InferenceService; autoscaling; GPU requests and scheduling; model storage
- **Full model lifecycle** — registry and promotion gates; canary and shadow deploys; rollback; reproducible training runs
- **Drift and model monitoring** — data drift, concept drift and performance monitoring (Evidently); alert tuning at scale across many models
- **Time-series MLOps** — point-in-time correctness; late and out-of-order data; backtesting at scale without leakage; monitoring models that act in real time
- **Orchestration (Dagster, Prefect)** — assets and schedules; backfills; data-quality checks inside pipelines
- **Data and dataset versioning** — DVC remotes and pipelines; FiftyOne for curation, dedup and label QA
- **Feature stores (Feast)** — offline and online stores; point-in-time joins; low-latency serving
- **Azure ML** — managed endpoints; pipelines; model registry; AKS for inference

## Cloud and infrastructure as code

- **Terraform** — providers and modules; remote state and locking; workspaces; plan/apply discipline; drift; secrets kept out of state; least-privilege IAM for ML resources
- **Helm** — charts and values; hooks; upgrades and rollbacks; probes, HPA and GPU requests for inference services; chart testing
- **Kubernetes hardening** — NetworkPolicies with default deny; Pod Security Standards; secrets via external-secrets or sealed-secrets; multi-tenant isolation
- **Prometheus and Grafana** — metrics design; PromQL; SLOs and alerting; dashboards for GPU and LLM traffic
- **Ansible and Bicep** — playbooks, roles and inventories; Bicep modules and what-if deployments
- **Site reliability practice** — on-call; incident runbooks; error budgets; FinOps and cost-aware design
- **Identity** — OAuth2 and OIDC flows in depth; token exchange and scopes; HashiCorp Vault; Azure Key Vault and RBAC

## Robotics and ROS 2

- **ROS 2 (production level)** — QoS; tf2 frames; lifecycle nodes; composition; launch and parameters; rosbag record and replay; DDS troubleshooting
- **Nav2** — behaviour trees; costmaps and inflation; planners versus controllers; tuning on real robots
- **SLAM and localization** — slam_toolbox mapping versus localization; robot_localization EKF fusing odometry, IMU and GPS; covariance tuning
- **ros2_control** — controller_manager; hardware interfaces; writing a hardware plugin; real-time update loops
- **MoveIt 2** — planning scene; collision checking; inverse kinematics; trajectory execution
- **Simulation and SIL** — Gazebo Sim worlds and sensors; Isaac Sim; deterministic replay for regression tests; CI for autonomy software
- **Robot learning** — imitation learning with LeRobot (ACT, diffusion policies); teleop data collection; domain randomisation and sim-to-real; vision-language-action models
- **Multi-robot systems** — task allocation; PDDL and PlanSys2; fleet coordination with Open-RMF; comms-limited operation

## Computer vision and perception

- **OpenCV in production** — camera calibration and undistortion; hand-eye calibration; PnP pose for pick-and-place; homographies; performance tuning
- **Industrial machine vision** — choosing cameras, lenses, filters and lighting; field of view, depth of field and resolution trade-offs; metrology and sub-pixel measurement; robustness to lighting and part variation
- **Detection, segmentation and tracking** — PyTorch and TorchVision training; instance segmentation; multi-object tracking (ByteTrack, BoT-SORT); HOTA, MOTA and IDF1 metrics
- **3D perception** — point-cloud filtering, clustering and registration (Open3D); stereo and depth; multi-sensor extrinsic calibration
- **6D pose and VLM perception** — PnP from 2D–3D correspondences; BOP metrics; vision-language models for detection and grounding
- **Image acquisition pipelines** — triggering and synchronisation; GStreamer; ROS 2 image_pipeline and image_transport; infrared and imaging-sensor calibration
- **Geospatial and earth-observation ML** — rasterio, CRS and tiling; TorchGeo; optical, SAR and hyperspectral fusion

## Embedded systems and C/C++

- **Modern C++ (C++17/20)** — RAII and move semantics; multithreading and memory layout; CMake; unit tests (GoogleTest); profiling with perf and gdb
- **Embedded Linux and Yocto** — layers, recipes and BSP images; device trees; U-Boot; kernel config; out-of-tree drivers
- **RTOS (Zephyr, FreeRTOS)** — threads, ISRs and work queues; synchronisation; device drivers for I2C, SPI and UART; power management
- **Bare-metal on ARM and RISC-V** — startup code; HAL design; memory-constrained code; JTAG debugging
- **CAN and CANopen** — frames and arbitration; bus errors; object dictionary, PDO and SDO; J1939 and UDS basics; python-can and cantools with DBC files
- **Firmware testing and CI** — host-side unit tests with mocks; hardware-in-the-loop rigs; cross-compiled builds in CI
- **Embedded Rust** — ownership and async; Embassy and RTIC; FFI to C

## State estimation, control and simulation

- **Kalman filtering** — KF, EKF and UKF; covariance and uncertainty propagation; tuning noise models (FilterPy)
- **Sensor fusion** — IMU noise, bias and calibration; orientation filters (Madgwick, complementary); visual-inertial odometry (OpenVINS); camera-IMU calibration
- **Tracking and orbit estimation** — multi-frame detection of faint objects; angles-only orbit determination; reference frames and time scales (Skyfield, Astropy)
- **Trajectory simulation** — ODE models with drag and wind (SciPy solve_ivp with events); Monte Carlo dispersion; Sobol and Morris sensitivity analysis (SALib)
- **Control engineering** — PID tuning; model predictive control; stochastic optimal control; motor control (field-oriented control, current and torque loops)
- **Simulink and model-based design** — block diagrams; solvers; plant models; code generation basics
- **Physics-based ML** — surrogate models trained on simulation data; physics-informed networks; CFD basics (OpenFOAM)

## Edge inference and hardware acceleration

- **Transformer inference internals** — attention variants; KV cache and paging; prefill versus decode; sampling; how a VLM joins a vision encoder to a language model
- **Quantization** — post-training versus quantization-aware training; weight-only and weight-activation schemes; calibration sets and outlier handling; telling quantization loss from a bug
- **ONNX Runtime** — exporting from PyTorch; opset pitfalls; execution providers; dynamic shapes; profiling
- **TensorRT and Jetson** — engine builds in FP16 and INT8; trtexec profiling; JetPack; zero-copy camera paths; DeepStream
- **CUDA** — kernels; memory transfers and streams; profiling with Nsight
- **On-device runtimes** — llama.cpp; ExecuTorch; LiteRT for microcontrollers; memory and latency budgets
- **Compilers for ML** — graph partitioning across accelerator and host; Triton, TVM or MLIR basics; differential testing against a reference

## Data engineering and governance

- **Databricks Unity Catalog** — catalogs, schemas and grants; lineage; volumes; Delta MERGE, change data feed, Z-order and liquid clustering; asset bundles CI/CD
- **dbt** — models, tests and incremental materialisations; sources and exposures; slim CI builds
- **Data modelling** — Kimball star schemas; conformed dimensions; SCD type 2; Data Vault
- **Microsoft Fabric and Azure Data Factory** — lakehouse versus warehouse; pipelines; Power BI semantic models
- **Data quality** — Great Expectations and Soda checks; data contracts; alerting on failed checks
- **Data catalogs and master data** — OpenMetadata, Collibra or Atlan concepts; lineage and classification; master data management basics
- **BigQuery and GCP data services** — partitioning and clustering; cost control; Pub/Sub; Dataflow
- **Streaming** — Kafka Streams (KStream, KTable, windowing, exactly-once); Delta streaming; Event Hubs and Azure Data Explorer with KQL
- **Open table formats** — Apache Iceberg tables, catalogs and partition evolution
- **Medical and clinical data standards** — DICOM; anonymisation; OMOP and HL7 FHIR basics
- **Spark on Kubernetes** — Spark Operator; executor sizing; shuffle and spill; S3A on MinIO

## Forecasting, optimisation and applied ML

- **Time-series forecasting** — baselines; time-series cross-validation; hierarchical and probabilistic forecasts; MASE and WAPE
- **Optimisation** — linear and mixed-integer programming; CP-SAT with OR-Tools; scheduling and dispatch under uncertainty
- **Tabular ML for finance** — gradient boosting (XGBoost, LightGBM); credit-risk and fraud features; price elasticity models
- **Statistical process control** — Shewhart, CUSUM and EWMA charts; process capability; PCA-based multivariate monitoring
- **Classic NLP** — token classification and NER fine-tuning; spaCy pipelines; topic clustering on embeddings

## Industrial, test and hardware integration

- **Hardware test automation** — PyVISA instrument control; test sequences with limits (OpenHTF, pytest); end-of-line tests; yield and Pareto analysis
- **PLC programming** — IEC 61131-3; CODESYS; TwinCAT and Siemens S7 basics; Modbus and Profinet
- **Industrial integration** — OPC UA subscriptions and security modes in practice; Ignition tags, scripting and historian; commissioning and FAT/SAT
- **Validation for regulated systems** — GAMP 5 categories; URS to FS to test traceability; change control
- **V-model verification** — requirements traceability; test plans and reports; MBSE with Capella
- **Industrial robot programming** — ABB RobotStudio and RAPID; cell layout; gripper and I/O integration
- **Space engineering basics** — ECSS standards; space mechanisms; qualification and acceptance testing

## Languages and frameworks

- **Go** — goroutines and channels; context cancellation; net/http services; streaming responses
- **Java 21 and Spring Boot** — modern Java features; Spring Boot services; Quarkus basics
- **C# and .NET** — ASP.NET Core; DDD and CQRS; WPF with MVVM for test-rig and machine GUIs
- **TypeScript backends** — Node.js with Express or Fastify; async integration with third-party APIs
- **Qt/QML** — QML bound to C++ models; threading off the UI thread; 3D visualisation