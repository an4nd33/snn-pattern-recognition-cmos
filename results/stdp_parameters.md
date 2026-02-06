# STDP Synapse Design Parameters

| Parameter | Description | Typical Value |
|----------|------------|---------------|
| A+ | Potentiation scaling factor | 0.005 |
| A− | Depression scaling factor | 0.005 |
| τ+ | Time constant for potentiation | 20 ms |
| τ− | Time constant for depression | 20 ms |
| Learning Rule | Pair-based STDP | Enabled |
| Synapse Type | CMOS-based memristive | Yes |

These parameters govern the synaptic weight update behavior based on
relative spike timing between pre- and post-synaptic neurons.
