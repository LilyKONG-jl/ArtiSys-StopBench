# Model Response Samples

These samples are selected from the formal 23-model pool used for the refreshed B/C/D tables. Each model contributes up to four examples spanning Task0, Task1, Task2-State, and Task2-Trajectory, with prompt strategies chosen to cover ordinary, ontology-aware, and bidirectional prompting.

Total sample records: 92

## MiniMax-M2.5

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_01052

- Artifact: `GEN_D_GEARBOX` / Gearbox
- Category: `D` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=1.0, relation_f1=1.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "transmission",
    "forward gear ratios",
    "reverse gear ratio",
    "electric motor",
    "engine"
  ],
  "functions": [
    "convert engine/motor speed and torque to wheel speed",
    "provide multiple speed ratios for different driving conditions",
    "enable reverse movement",
    "enable bidirectional operation"
  ],
  "interfaces": [
    "engine-to-transmission input",
    "transmission-to-wheels output",
    "gear ratio selection"
  ],
  "mechanism_facts": [
    {
      "fact": "transmission converts engine rotational input to variable wheel speed output through gear ratios",
      "support_status": "supported",
      "source_span_id": "span1"
    },
    {
      "fact": "conventional transmissions use 4-10 forward gear ratios and one reverse gear ratio to provide speed conversion",
      "support_status": "supported",
      "source_span_id": "span1"
    },
    {
      "fact": "electric vehicle transmissions use fixed-ratio or two-speed conversion due to wider motor efficiency range",
      "support_status": "supported",
      "source_span_id": "span2"
    },
    {
      "fact": "electric motors can operate efficiently from stopped to high speed, providing direct input conversion capability",
      "support_status": "supported",
      "source_span_id": "span2"
    },
    {
      "fact": "electric motors change direction electrically, eliminating need for reverse gear mechanism",
      "support_status": "supported",
      "source_span_id": "span2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "f1",
      "source_span_id": "span1",
      "support_status": "supported"
    },
    {
      "fact_id": "f2",
      "source_span_id": "span1",
      "support_status": "supported"
    },
    {
      "fact_id": "f3",
      "source_span_id": "span2",
      "support_status": "supported"
    },
    {
      "fact_id": "f4",
      "source_span_id": "span2",
      "support_status": "supported"
    },
    {
      "fact_id": "f5",
      "source_span_id": "span2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "core_function_chain_covered",
      "evidence_grounding_sufficient",
      "no_unresolved_conflict"
    ],
    "known_components": [
      "transmission",
      "forward gear ratios",
      "reverse gear ratio",
      "electric motor",
      "engine"
    ],
    "known_interfaces": [
      "engine-to-transmission input",
      "transmission-to-wheels output",
      "gear ratio selection"
    ],
    "known_mechanism_facts": [
      "f1",
      "f2",
      "f3",
      "f4",
      "f5"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": []
}
```

Raw output:
```text
{"components":["transmission","forward gear ratios","reverse gear ratio","electric motor","engine"],"functions":["convert engine/motor speed and torque to wheel speed","provide multiple speed ratios for different driving conditions","enable reverse movement","enable bidirectional operation"],"interfaces":["engine-to-transmission input","transmission-to-wheels output","gear ratio selection"],"mechanism_facts":[{"fact":"transmission converts engine rotational input to variable wheel speed output through gear ratios","support_status":"supported","source_span_id":"span1"},{"fact":"conventional transmissions use 4-10 forward gear ratios and one reverse gear ratio to provide speed conversion","support_status":"supported","source_span_id":"span1"},{"fact":"electric vehicle transmissions use fixed-ratio or two-speed conversion due to wider motor efficiency range","support_status":"supported","source_span_id":"span2"},{"fact":"electric motors can operate efficiently from stopped to high speed, providing direct input conversion capability","support_status":"supported","source_span_id":"span2"},{"fact":"electric motors change direction electrically, eliminating need for reverse gear mechanism","support_status":"supported","source_span_id":"span2"}],"evidence_mapping":[{"fact_id":"f1","source_span_id":"span1","support_status":"supported"},{"fact_id":"f2","source_span_id":"span1","support_status":"supported"},{"fact_id":"f3","source_span_id":"span2","support_status":"supported"},{"fact_id":"f4","source_span_id":"span2","support_status":"supported"},{"fact_id":"f5","source_span_id":"span2","support_status":"supported"}],"state_update":{"covered_critical_states":["core_function_chain_covered","evidence_grounding_sufficient","no_unresolved_conflict"],"known_components":["transmission","forward gear ratios","reverse gear ratio","electric motor","engine"],"known_interfaces":["engine-to-transmission input","transmission-to-wheels output","gear ratio selection"],"known_mechanism_facts":["f1","f2","f3","f4","f5"],"unresolved_conflicts":[]},"missing_critical_states":[]}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The spray bottle’s engineering function is to produce a spray of liquid when the user activates it. The typical causal chain is: the user’s press (user input) starts the pump mechanism (operating mechanism), which moves an internal piston or linkage (internal linkage) that forces liquid through the nozzle (working contact) onto the target, thereby generating the spray (named engineering output). This sequence matches option C.",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The spray bottle’s engineering function is to produce a spray of liquid when the user activates it. The typical causal chain is: the user’s press (user input) starts the pump mechanism (operating mechanism), which moves an internal piston or linkage (internal linkage) that forces liquid through the nozzle (working contact) onto the target, thereby generating the spray (named engineering output). This sequence matches option C.",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "No further extraction needed - all critical states covered with sufficient evidence and no unresolved conflicts",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "stop", "sufficiency_gap": [], "next_extraction_action": "No further extraction needed - all critical states covered with sufficient evidence and no unresolved conflicts", "reason_consistency": "consistent"}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## gemini-3.5-flash

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00603

- Artifact: `GEN_C_ALTERNATOR` / Alternator
- Category: `C` | Language: `en` | Question family: `interface_boundary`
- Key metrics: ontology_f1=0.8888888888888888, relation_f1=1.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "direct-current (DC) generator",
    "shaft",
    "alternator",
    "field coils"
  ],
  "functions": [
    "generate excitation electricity",
    "excite field coils",
    "generate output electricity"
  ],
  "interfaces": [
    "shaft-coupling interface",
    "excitation-supply interface",
    "alternator-output interface"
  ],
  "mechanism_facts": [
    {
      "fact": "The DC generator is mechanically coupled to the alternator by being fixed on the same shaft.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "The DC generator provides a small amount of electricity to the field coils of the alternator.",
      "support_status": "supported",
      "source_span_id": "SPAN_2"
    },
    {
      "fact": "The alternator generates electricity when its field coils are excited by the DC generator.",
      "support_status": "supported",
      "source_span_id": "SPAN_2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "f1",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f2",
      "source_span_id": "SPAN_2",
      "support_status": "supported"
    },
    {
      "fact_id": "f3",
      "source_span_id": "SPAN_2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "critical_interfaces_covered",
      "internal_external_boundary_distinguished",
      "evidence_grounding_sufficient"
    ],
    "known_components": [
      "direct-current (DC) generator",
      "shaft",
      "alternator",
      "field coils"
    ],
    "known_interfaces": [
      "shaft-coupling interface",
      "excitation-supply interface",
      "alternator-output interface"
    ],
    "known_mechanism_facts": [
      "f1",
      "f2",
      "f3"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "external_prime_mover_input_unspecified"
  ]
}
```

Raw output:
```text
{
  "components": [
    "direct-current (DC) generator",
    "shaft",
    "alternator",
    "field coils"
  ],
  "functions": [
    "generate excitation electricity",
    "excite field coils",
    "generate output electricity"
  ],
  "interfaces": [
    "shaft-coupling interface",
    "excitation-supply interface",
    "alternator-output interface"
  ],
  "mechanism_facts": [
    {
      "fact": "The DC generator is mechanically coupled to the alternator by being fixed on the same shaft.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "The DC generator provides a small amount of electricity to the field coils of the alternator.",
      "support_status": "supported",
      "source_span_id": "SPAN_2"
    },
    {
      "fact": "The alternator generates electricity when its field coils are excited by the DC generator.",
      "support_status": "supported",
      "source_span_id": "SPAN_2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "f1",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f2",
      "source_span_id": "SPAN_2",
      "support_status": "supported"
    },
    {
      "fact_id": "f3",
      "source_span_id": "SPAN_2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "critical_interfaces_covered",
      "internal_external_boundary_distinguished",
      "evidence_grounding_sufficient"
    ],
    "known_components": [
      "direct-current (DC) generator",
      "shaft",
      "alternator",
      "field coils"
    ],
    "known_interfaces": [
      "shaft-coupling interface",
      "excitation-supply interface",
      "alternator-output interface"
    ],
    "known_mechanism_facts": [
      "f1",
      "f2",
      "f3"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "external_prime_mover_input_unspecified"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_TAPE_MEASURE_STRUCTURAL_DECOMPOSITION_04_1442_ZH

- Artifact: `GEN_A_TAPE_MEASURE` / Tape measure
- Category: `A` | Language: `zh` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "根据工程本体论中的功能链逻辑，实现产品主要工程功能的必要工作组合应遵循以下因果与物理传递顺序：首先是“用户输入启动操作机构”，接着通过“内部连接关系传递动作”，然后是“工作接触作用于目标对象”，最终“卷尺的主要功能输出形成”。选项C完全符合这一标准的本体论逻辑顺序。",
  "confidence": 1.0
}
```

Raw output:
```text
```json
{
  "answer": "C",
  "reasoning": "根据工程本体论中的功能链逻辑，实现产品主要工程功能的必要工作组合应遵循以下因果与物理传递顺序：首先是“用户输入启动操作机构”，接着通过“内部连接关系传递动作”，然后是“工作接触作用于目标对象”，最终“卷尺的主要功能输出形成”。选项C完全符合这一标准的本体论逻辑顺序。",
  "confidence": 1.0
}
```
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "none",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "stop", "sufficiency_gap": [], "next_extraction_action": "none", "reason_consistency": "consistent"}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```
```

## gpt-5.6-luna

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00709

- Artifact: `GEN_C_HEAT_PUMP` / Heat pump
- Category: `C` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: ontology_f1=1.0, relation_f1=1.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "refrigerant working fluid",
    "refrigerant pumping unit",
    "coil heat exchanger",
    "air-moving fan"
  ],
  "functions": [
    "pump gaseous refrigerant into the coil heat exchanger",
    "move air across the coil",
    "transfer heat from the air to the refrigerant",
    "liquefy the refrigerant",
    "support heat transfer in both directions"
  ],
  "interfaces": [
    "refrigerant flow interface between the pumping unit and coil heat exchanger",
    "airflow interface between the fan and coil heat exchanger",
    "thermal exchange interface between air and refrigerant at the coil"
  ],
  "mechanism_facts": [
    {
      "fact": "A pumping unit sends gaseous refrigerant into coils in the heating unit.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "A fan blows air over the coils, enabling heat transfer from the air to the refrigerant.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "The refrigerant absorbs heat and liquefies in the coil heat exchanger.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "Heat pumps are capable of transferring heat in both directions.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "f1",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f2",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f3",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f4",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "evidence_grounding_sufficient"
    ],
    "known_components": [
      "refrigerant working fluid",
      "refrigerant pumping unit",
      "coil heat exchanger",
      "air-moving fan"
    ],
    "known_interfaces": [
      "refrigerant flow interface between the pumping unit and coil heat exchanger",
      "airflow interface between the fan and coil heat exchanger",
      "thermal exchange interface between air and refrigerant at the coil"
    ],
    "known_mechanism_facts": [
      "f1",
      "f2",
      "f3",
      "f4"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "complete refrigerant return and phase-change path not evidenced",
    "mechanism for reversing the heat-transfer direction not evidenced",
    "full two-sided heat-pump structural closure not evidenced"
  ]
}
```

Raw output:
```text
{
  "components": [
    "refrigerant working fluid",
    "refrigerant pumping unit",
    "coil heat exchanger",
    "air-moving fan"
  ],
  "functions": [
    "pump gaseous refrigerant into the coil heat exchanger",
    "move air across the coil",
    "transfer heat from the air to the refrigerant",
    "liquefy the refrigerant",
    "support heat transfer in both directions"
  ],
  "interfaces": [
    "refrigerant flow interface between the pumping unit and coil heat exchanger",
    "airflow interface between the fan and coil heat exchanger",
    "thermal exchange interface between air and refrigerant at the coil"
  ],
  "mechanism_facts": [
    {
      "fact": "A pumping unit sends gaseous refrigerant into coils in the heating unit.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "A fan blows air over the coils, enabling heat transfer from the air to the refrigerant.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "The refrigerant absorbs heat and liquefies in the coil heat exchanger.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "Heat pumps are capable of transferring heat in both directions.",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "f1",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f2",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f3",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f4",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "evidence_grounding_sufficient"
    ],
    "known_components": [
      "refrigerant working fluid",
      "refrigerant pumping unit",
      "coil heat exchanger",
      "air-moving fan"
    ],
    "known_interfaces": [
      "refrigerant flow interface between the pumping unit and coil heat exchanger",
      "airflow interface between the fan and coil heat exchanger",
      "thermal exchange interface between air and refrigerant at the coil"
    ],
    "known_mechanism_facts": [
      "f1",
      "f2",
      "f3",
      "f4"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "complete refrigerant return 
...<truncated>...
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The spray bottle sequence is: user input activates the operating mechanism, the internal linkage transfers the action, the working contact acts on the target liquid or air path, and the named engineering output is produced as a spray.",
  "confidence": 0.99
}
```

Raw output:
```text
{"answer":"C","reasoning":"The spray bottle sequence is: user input activates the operating mechanism, the internal linkage transfers the action, the working contact acts on the target liquid or air path, and the named engineering output is produced as a spray.","confidence":0.99}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00161_2

- Artifact: `GEN_A_MICROWAVE_OVEN` / Microwave oven
- Category: `A` | Language: `en` | Question family: `failure_propagation`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Stop extraction; the failure path is sufficiently covered and grounded.",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision":"stop","sufficiency_gap":[],"next_extraction_action":"Stop extraction; the failure path is sufficiently covered and grounded.","reason_consistency":"consistent"}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": "3",
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision":"best_stop_round","selected_round":"3","sufficiency_gap":[],"reason_consistency":"consistent"}
```

## grok-4.5

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_01759

- Artifact: `GEN_F_TELESCOPE` / Telescope
- Category: `F` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: ontology_f1=1.0, relation_f1=1.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "optical lenses",
    "curved mirrors",
    "combined optical system"
  ],
  "functions": [
    "observe distant objects via electromagnetic radiation"
  ],
  "interfaces": [
    "electromagnetic radiation input",
    "optical focusing interface",
    "observation output"
  ],
  "mechanism_facts": [
    {
      "fact": "minimal optical telescope structure requires lenses, curved mirrors, or a combination of both",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "these optical elements form the structural closure enabling observation of distant objects by emission, absorption, or reflection of electromagnetic radiation",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "f1",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f2",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "core_components_covered",
      "evidence_grounding_sufficient",
      "no_unresolved_conflict"
    ],
    "known_components": [
      "optical lenses",
      "curved mirrors",
      "combined optical system"
    ],
    "known_interfaces": [
      "electromagnetic radiation input",
      "optical focusing interface",
      "observation output"
    ],
    "known_mechanism_facts": [
      "f1",
      "f2"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": []
}
```

Raw output:
```text
{
  "components": [
    "optical lenses",
    "curved mirrors",
    "combined optical system"
  ],
  "functions": [
    "observe distant objects via electromagnetic radiation"
  ],
  "interfaces": [
    "electromagnetic radiation input",
    "optical focusing interface",
    "observation output"
  ],
  "mechanism_facts": [
    {
      "fact": "minimal optical telescope structure requires lenses, curved mirrors, or a combination of both",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    },
    {
      "fact": "these optical elements form the structural closure enabling observation of distant objects by emission, absorption, or reflection of electromagnetic radiation",
      "support_status": "supported",
      "source_span_id": "SPAN_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "f1",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    },
    {
      "fact_id": "f2",
      "source_span_id": "SPAN_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "core_components_covered",
      "evidence_grounding_sufficient",
      "no_unresolved_conflict"
    ],
    "known_components": [
      "optical lenses",
      "curved mirrors",
      "combined optical system"
    ],
    "known_interfaces": [
      "electromagnetic radiation input",
      "optical focusing interface",
      "observation output"
    ],
    "known_mechanism_facts": [
      "f1",
      "f2"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": []
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The necessary causal sequence for the Spray bottle's named engineering function (producing a directed spray) follows the standard energy/material flow: user input first starts the operating mechanism (trigger actuation), an internal linkage then transfers the action (piston/pump pressurization), the working contact subsequently acts on the target (nozzle atomizes and directs fluid), and the named engineering output is finally produced (spray delivered). This matches option C exactly; other options reverse or interleave the required order of relations.",
  "confidence": 0.9
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The necessary causal sequence for the Spray bottle's named engineering function (producing a directed spray) follows the standard energy/material flow: user input first starts the operating mechanism (trigger actuation), an internal linkage then transfers the action (piston/pump pressurization), the working contact subsequently acts on the target (nozzle atomizes and directs fluid), and the named engineering output is finally produced (spray delivered). This matches option C exactly; other options reverse or interleave the required order of relations.",
  "confidence": 0.9
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "none",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "stop", "sufficiency_gap": [], "next_extraction_action": "none", "reason_consistency": "consistent"}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```
```

## kimi-k2.7-code

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.19999999999999998, relation_f1=0.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "head",
    "handle",
    "object",
    "nail",
    "wood",
    "metal",
    "rock"
  ],
  "functions": [
    "deliver an impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head-handle fixation",
    "head-object contact area"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: the long handle is swung to move the weighted head.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Conversion: the weighted head fixed to the handle delivers an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Output: the hammer drives nails into wood.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Output: the hammer shapes metal (as with a forge).",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Output: the hammer crushes rock.",
      "support_status": "supported",
      "source_span_id": "span_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "0",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "1",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "2",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "3",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "4",
      "source_span_id": "span_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "handle is swung",
      "head delivers impact to small area of object",
      "nails driven into wood",
      "metal shaped",
      "rock crushed"
    ],
    "known_components": [
      "head",
      "handle",
      "object",
      "nail",
      "wood",
      "metal",
      "rock"
    ],
    "known_interfaces": [
      "head-handle fixation",
      "head-object contact area"
    ],
    "known_mechanism_facts": [
      "0",
      "1",
      "2",
      "3",
      "4"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "application of external force by a user to initiate swinging of the handle",
    "acceleration of the weighted head during the swing",
    "transfer of kinetic energy from the head to the object upon impact",
    "resulting displacement, penetration, or deformation of the object"
  ]
}
```

Raw output:
```text
```json
{
  "components": [
    "head",
    "handle",
    "object",
    "nail",
    "wood",
    "metal",
    "rock"
  ],
  "functions": [
    "deliver an impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head-handle fixation",
    "head-object contact area"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: the long handle is swung to move the weighted head.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Conversion: the weighted head fixed to the handle delivers an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Output: the hammer drives nails into wood.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Output: the hammer shapes metal (as with a forge).",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Output: the hammer crushes rock.",
      "support_status": "supported",
      "source_span_id": "span_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "0",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "1",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "2",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "3",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "4",
      "source_span_id": "span_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "handle is swung",
      "head delivers impact to small area of object",
      "nails driven into wood",
      "metal shaped",
      "rock crushed"
    ],
    "known_components": [
      "head",
      "handle",
      "object",
      "nail",
      "wood",
      "metal",
      "rock"
    ],
    "known_interfaces": [
      "head-handle fixation",
      "head-object contact area"
    ],
    "known_mechanism_facts": [
      "0",
      "1",
      "2",
      "3",
      "4"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "application of external force by a user to initiate swinging of the handle",
    "acceleration of the weighted head during the swing",
    "transfer of kinetic energy from the head t
...<truncated>...
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The Spray bottle performs its named engineering function through a causal chain: User input initiates the operating mechanism; an internal linkage transfers the action; the working contact acts on the target; and finally the named engineering output is produced. Option C matches this required sequence.",
  "confidence": 1.0
}
```

Raw output:
```text
{"answer": "C", "reasoning": "The Spray bottle performs its named engineering function through a causal chain: User input initiates the operating mechanism; an internal linkage transfers the action; the working contact acts on the target; and finally the named engineering output is produced. Option C matches this required sequence.", "confidence": 1.0}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00207_2

- Artifact: `GEN_A_SCISSORS` / scissors
- Category: `A` | Language: `en` | Question family: `interface_boundary`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate extraction and finalize the interface-boundary report",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate extraction and finalize the interface-boundary report",
  "reason_consistency": "consistent"
}
```
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## glm-5.1

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle",
    "head impact surface to target object",
    "handle to hand (grip)"
  ],
  "mechanism_facts": [
    {
      "fact": "Hammer is swung to deliver impact to an object",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "Weighted head concentrates force onto small area upon impact",
      "support_status": "supported",
      "source_span_id": "span_1_2"
    },
    {
      "fact": "Impact drives nails into wood",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Impact shapes metal",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Impact crushes rock",
      "support_status": "supported",
      "source_span_id": "span_3"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "mf_1",
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_2",
      "source_span_id": "span_1_2",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_3",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_4",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_5",
      "source_span_id": "span_3",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input: swinging motion",
      "output: impact delivered to object"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "head fixed to handle",
      "head impact surface to target object",
      "handle to hand"
    ],
    "known_mechanism_facts": [
      "Hammer is swung to deliver impact to an object",
      "Weighted head concentrates force onto small area upon impact",
      "Impact drives nails into wood",
      "Impact shapes metal",
      "Impact crushes rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "conversion: kinetic energy transfer from swing to concentrated impact force (not explicitly described)",
    "conversion: force amplification mechanism via head weight and handle leverage (not explicitly described)"
  ]
}
```

Raw output:
```text
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle",
    "head impact surface to target object",
    "handle to hand (grip)"
  ],
  "mechanism_facts": [
    {
      "fact": "Hammer is swung to deliver impact to an object",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "Weighted head concentrates force onto small area upon impact",
      "support_status": "supported",
      "source_span_id": "span_1_2"
    },
    {
      "fact": "Impact drives nails into wood",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Impact shapes metal",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Impact crushes rock",
      "support_status": "supported",
      "source_span_id": "span_3"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "mf_1",
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_2",
      "source_span_id": "span_1_2",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_3",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_4",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_5",
      "source_span_id": "span_3",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input: swinging motion",
      "output: impact delivered to object"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "head fixed to handle",
      "head impact surface to target object",
      "handle to hand"
    ],
    "known_mechanism_facts": [
      "Hammer is swung to deliver impact to an object",
      "Weighted head concentrates force onto small area upon impact",
      "Impact drives nails into wood",
      "Impact shapes metal",
      "Impact crushes rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "conversion: kinetic energy transfer from swing to concentrated impact force (not explicitly described)",
    "conversion: force amplification mechanism via head weight and handle leverage (not explicitly described)"
...<truncated>...
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The functional decomposition of a spray bottle follows a logical causal chain from input to final output. First, user input actuates the trigger (operating mechanism). Second, the internal linkage (piston, spring, valve) transfers this mechanical action to pressurize and expel the liquid. Third, the expelled liquid (working contact) acts on the target surface. Finally, the intended engineering function (e.g., cleaning, coating, or dispensing) is produced as the ultimate output. Option C correctly sequences these relations.",
  "confidence": 1.0
}
```

Raw output:
```text
```json
{
  "answer": "C",
  "reasoning": "The functional decomposition of a spray bottle follows a logical causal chain from input to final output. First, user input actuates the trigger (operating mechanism). Second, the internal linkage (piston, spring, valve) transfers this mechanical action to pressurize and expel the liquid. Third, the expelled liquid (working contact) acts on the target surface. Finally, the intended engineering function (e.g., cleaning, coating, or dispensing) is produced as the ultimate output. Option C correctly sequences these relations.",
  "confidence": 1.0
}
```
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate_extraction",
  "reason_consistency": "consistent"
}
```
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```
```

## kimi-k2.6

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.25, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "head",
    "handle",
    "object"
  ],
  "functions": [
    "deliver impact",
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head-handle interface",
    "head-object contact area"
  ],
  "mechanism_facts": [
    {
      "fact": "weighted head is fixed to long handle",
      "support_status": "directly_supported",
      "source_span_id": "consisting of a weighted 'head' fixed to a long handle"
    },
    {
      "fact": "handle is swung to deliver impact",
      "support_status": "directly_supported",
      "source_span_id": "that is swung to deliver an impact"
    },
    {
      "fact": "impact is delivered to small area of object",
      "support_status": "directly_supported",
      "source_span_id": "deliver an impact to a small area of an object"
    },
    {
      "fact": "mechanism can drive nails into wood",
      "support_status": "directly_supported",
      "source_span_id": "to drive nails into wood"
    },
    {
      "fact": "mechanism can shape metal as with a forge",
      "support_status": "directly_supported",
      "source_span_id": "to shape metal (as with a forge)"
    },
    {
      "fact": "mechanism can crush rock",
      "support_status": "directly_supported",
      "source_span_id": "to crush rock"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "weighted head is fixed to long handle",
      "source_span_id": "consisting of a weighted 'head' fixed to a long handle",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "handle is swung to deliver impact",
      "source_span_id": "that is swung to deliver an impact",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "impact is delivered to small area of object",
      "source_span_id": "deliver an impact to a small area of an object",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "mechanism can drive nails into wood",
      "source_span_id": "to drive nails into wood",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "mechanism can shape metal as with a forge",
      "source_span_id": "to shape metal (as with a forge)",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "mechanism can crush rock",
      "source_span_id": "to crush rock",
      "support_status": "directly_supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input: handle swung",
      "conversion: kinetic energy transfer",
      "output: impact delivered to small area"
    ],
    "known_components": [
      "head",
      "handle",
      "object"
    ],
    "known_interfaces": [
      "head-handle interface",
      "head-object contact area"
    ],
    "known_mechanism_facts": [
      "weighted head is fixed to long handle",
      "handle is swung to deliver impact",
      "impact is delivered to small area of object",
      "mechanism can drive nails into wood",
      "mechanism can shape metal as with a forge",
      "mechanism can crush rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "intermediate_state: head acceleration phase before impact",
    "intermediate_state: energy storage in handle flexion",
    "intermediate_state: force concentration mechanism at head-object interface",
    "intermediate_state: object deformation or penetration dynamics",
    "output_state: nail displacement or metal/rock fracture mechanics"
  ]
}
```

Raw output:
```text
```json
{
  "components": [
    "head",
    "handle",
    "object"
  ],
  "functions": [
    "deliver impact",
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head-handle interface",
    "head-object contact area"
  ],
  "mechanism_facts": [
    {
      "fact": "weighted head is fixed to long handle",
      "support_status": "directly_supported",
      "source_span_id": "consisting of a weighted 'head' fixed to a long handle"
    },
    {
      "fact": "handle is swung to deliver impact",
      "support_status": "directly_supported",
      "source_span_id": "that is swung to deliver an impact"
    },
    {
      "fact": "impact is delivered to small area of object",
      "support_status": "directly_supported",
      "source_span_id": "deliver an impact to a small area of an object"
    },
    {
      "fact": "mechanism can drive nails into wood",
      "support_status": "directly_supported",
      "source_span_id": "to drive nails into wood"
    },
    {
      "fact": "mechanism can shape metal as with a forge",
      "support_status": "directly_supported",
      "source_span_id": "to shape metal (as with a forge)"
    },
    {
      "fact": "mechanism can crush rock",
      "support_status": "directly_supported",
      "source_span_id": "to crush rock"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "weighted head is fixed to long handle",
      "source_span_id": "consisting of a weighted 'head' fixed to a long handle",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "handle is swung to deliver impact",
      "source_span_id": "that is swung to deliver an impact",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "impact is delivered to small area of object",
      "source_span_id": "deliver an impact to a small area of an object",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "mechanism can drive nails into wood",
      "source_span_id": "to drive nails into wood",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "mechanism can shape metal as with a forge",
      "source_span_id": "to shape metal (as with a forge)",
      "support_status": "directly_supported"
    },
    {
      "fact_id": "mechanism can crush rock",
      "source_span_id": "to crush rock",
      "support_status": "directly_supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input: handle swung",
      "conv
...<truncated>...
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The Spray bottle artifact follows the canonical engineering function ontology: User input (trigger press) starts the operating mechanism; An internal linkage (piston/spring assembly) transfers the action; The working contact (nozzle/spray) acts on the target; The named engineering output (dispersed liquid) is produced. This sequence C correctly orders the causal chain from input initiation through energy/motion transfer to working contact action and finally output production. Options A and D misplace the working contact and output order. Option B reverses the entire causal sequence.",
  "confidence": 0.95
}
```

Raw output:
```text
```json
{
  "answer": "C",
  "reasoning": "The Spray bottle artifact follows the canonical engineering function ontology: User input (trigger press) starts the operating mechanism; An internal linkage (piston/spring assembly) transfers the action; The working contact (nozzle/spray) acts on the target; The named engineering output (dispersed liquid) is produced. This sequence C correctly orders the causal chain from input initiation through energy/motion transfer to working contact action and finally output production. Options A and D misplace the working contact and output order. Option B reverses the entire causal sequence.",
  "confidence": 0.95
}
```
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00207_2

- Artifact: `GEN_A_SCISSORS` / scissors
- Category: `A` | Language: `en` | Question family: `interface_boundary`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate_extraction",
  "reason_consistency": "consistent"
}
```
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": "3",
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{"decision": "best_stop_round", "selected_round": "3", "sufficiency_gap": [], "reason_consistency": "consistent"}
```
```

## qwen3.6-27b

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.26666666666666666, relation_f1=0.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "handle",
    "head",
    "target_object"
  ],
  "functions": [
    "transfer_kinetic_energy",
    "concentrate_impact_force",
    "deform_or_penetrate_material"
  ],
  "interfaces": [
    "handle_head_fixation",
    "head_object_contact_surface"
  ],
  "mechanism_facts": [
    {
      "fact": "Swinging the handle provides kinetic energy input to the system.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The weighted head converts and transmits this motion into a concentrated impact force.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The impact is delivered to a small area to drive nails, shape metal, or crush rock.",
      "support_status": "supported",
      "source_span_id": "span_2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": "span_2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input_motion_transfer",
      "force_conversion",
      "output_impact_application"
    ],
    "known_components": [
      "handle",
      "head",
      "target_object"
    ],
    "known_interfaces": [
      "handle_head_fixation",
      "head_object_contact_surface"
    ],
    "known_mechanism_facts": [
      "fact_1",
      "fact_2",
      "fact_3"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "input_energy_generation_mechanism",
    "kinetic_to_impact_force_conversion_physics",
    "material_deformation_or_fracture_response_dynamics"
  ]
}
```

Raw output:
```text
{
  "components": [
    "handle",
    "head",
    "target_object"
  ],
  "functions": [
    "transfer_kinetic_energy",
    "concentrate_impact_force",
    "deform_or_penetrate_material"
  ],
  "interfaces": [
    "handle_head_fixation",
    "head_object_contact_surface"
  ],
  "mechanism_facts": [
    {
      "fact": "Swinging the handle provides kinetic energy input to the system.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The weighted head converts and transmits this motion into a concentrated impact force.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The impact is delivered to a small area to drive nails, shape metal, or crush rock.",
      "support_status": "supported",
      "source_span_id": "span_2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": "span_2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input_motion_transfer",
      "force_conversion",
      "output_impact_application"
    ],
    "known_components": [
      "handle",
      "head",
      "target_object"
    ],
    "known_interfaces": [
      "handle_head_fixation",
      "head_object_contact_surface"
    ],
    "known_mechanism_facts": [
      "fact_1",
      "fact_2",
      "fact_3"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "input_energy_generation_mechanism",
    "kinetic_to_impact_force_conversion_physics",
    "material_deformation_or_fracture_response_dynamics"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The functional ontology of GEN_A_SPRAY_BOTTLE dictates a strict causal chain: User_Input initiates the Operating_Mechanism, the Internal_Linkage transfers the mechanical action/pressure, the Working_Contact acts on the Target medium, and the Engineering_Output is subsequently produced. Option C correctly sequences these functional dependencies according to standard engineering function decomposition.",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The functional ontology of GEN_A_SPRAY_BOTTLE dictates a strict causal chain: User_Input initiates the Operating_Mechanism, the Internal_Linkage transfers the mechanical action/pressure, the Working_Contact acts on the Target medium, and the Engineering_Output is subsequently produced. Option C correctly sequences these functional dependencies according to standard engineering function decomposition.",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "none",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "stop", "sufficiency_gap": [], "next_extraction_action": "none", "reason_consistency": "consistent"}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## qwen3.5-plus-2026-04-20

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.3333333333333333, boundary_accuracy=0.8, minimal_system_accuracy=0.8

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle",
    "target object"
  ],
  "functions": [
    "transmit swing force",
    "concentrate impact force",
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle-head junction",
    "head-object contact area"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: Human swing motion is applied to the long handle.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Conversion: The handle transmits the swing motion to the weighted head, which concentrates the force upon contact.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Output: The concentrated impact force is delivered to a small area of an object, resulting in driving, shaping, or crushing.",
      "support_status": "supported",
      "source_span_id": "span_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "mf_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_2",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "mf_3",
      "source_span_id": "span_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input_mechanism",
      "conversion_mechanism",
      "output_mechanism"
    ],
    "known_components": [
      "weighted head",
      "long handle",
      "target object"
    ],
    "known_interfaces": [
      "handle-head junction",
      "head-object contact area"
    ],
    "known_mechanism_facts": [
      "mf_1",
      "mf_2",
      "mf_3"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "explicit human energy input quantification",
    "kinetic energy transfer dynamics",
    "force concentration physics",
    "material deformation/fracture process details"
  ]
}
```

Raw output:
```text
{
  "components": ["weighted head", "long handle", "target object"],
  "functions": ["transmit swing force", "concentrate impact force", "drive nails", "shape metal", "crush rock"],
  "interfaces": ["handle-head junction", "head-object contact area"],
  "mechanism_facts": [
    {"fact": "Input: Human swing motion is applied to the long handle.", "support_status": "supported", "source_span_id": "span_1"},
    {"fact": "Conversion: The handle transmits the swing motion to the weighted head, which concentrates the force upon contact.", "support_status": "supported", "source_span_id": "span_1"},
    {"fact": "Output: The concentrated impact force is delivered to a small area of an object, resulting in driving, shaping, or crushing.", "support_status": "supported", "source_span_id": "span_1"}
  ],
  "evidence_mapping": [
    {"fact_id": "mf_1", "source_span_id": "span_1", "support_status": "supported"},
    {"fact_id": "mf_2", "source_span_id": "span_1", "support_status": "supported"},
    {"fact_id": "mf_3", "source_span_id": "span_1", "support_status": "supported"}
  ],
  "state_update": {
    "covered_critical_states": ["input_mechanism", "conversion_mechanism", "output_mechanism"],
    "known_components": ["weighted head", "long handle", "target object"],
    "known_interfaces": ["handle-head junction", "head-object contact area"],
    "known_mechanism_facts": ["mf_1", "mf_2", "mf_3"],
    "unresolved_conflicts": []
  },
  "missing_critical_states": ["explicit human energy input quantification", "kinetic energy transfer dynamics", "force concentration physics", "material deformation/fracture process details"]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "Engineering functional modeling ontologies define artifact operation as a forward causal chain of functional primitives: user input activates the operating mechanism, which transfers action through an internal linkage to the working contact, ultimately acting on the target to produce the named engineering output. Option C correctly sequences these ontology-grounded relations in the required causal direction, while other options violate temporal or functional dependencies.",
  "confidence": 0.98
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "Engineering functional modeling ontologies define artifact operation as a forward causal chain of functional primitives: user input activates the operating mechanism, which transfers action through an internal linkage to the working contact, ultimately acting on the target to produce the named engineering output. Option C correctly sequences these ontology-grounded relations in the required causal direction, while other options violate temporal or functional dependencies.",
  "confidence": 0.98
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00207_2

- Artifact: `GEN_A_SCISSORS` / scissors
- Category: `A` | Language: `en` | Question family: `interface_boundary`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Terminate extraction; all critical interfaces and boundary distinctions are sufficiently covered with low marginal gain.",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Terminate extraction; all critical interfaces and boundary distinctions are sufficiently covered with low marginal gain.",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## qwen3.6-flash-2026-04-16

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle",
    "target object"
  ],
  "functions": [
    "swing",
    "deliver impact",
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle-to-user grip",
    "head-to-target contact"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: Swinging motion imparts kinetic energy to the handle.",
      "support_status": "supported",
      "source_span_id": 0
    },
    {
      "fact": "Conversion: Rigid handle transfers kinetic energy to the weighted head, concentrating force onto a small contact area.",
      "support_status": "supported",
      "source_span_id": 1
    },
    {
      "fact": "Output: Concentrated impact delivers mechanical work to the target object, causing fastening, deformation, or fragmentation.",
      "support_status": "supported",
      "source_span_id": 2
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_1",
      "source_span_id": 0,
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": 1,
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": 2,
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "energy_input",
      "force_concentration",
      "impact_output"
    ],
    "known_components": [
      "weighted head",
      "long handle",
      "target object"
    ],
    "known_interfaces": [
      "handle-to-user grip",
      "head-to-target contact"
    ],
    "known_mechanism_facts": [
      "Input: Swinging motion imparts kinetic energy to the handle.",
      "Conversion: Rigid handle transfers kinetic energy to the weighted head, concentrating force onto a small contact area.",
      "Output: Concentrated impact delivers mechanical work to the target object, causing fastening, deformation, or fragmentation."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "user_grip_dynamics",
    "handle_material_properties_and_damping",
    "contact_stress_distribution_at_impact",
    "target_material_yield_strength",
    "energy_efficiency_of_transfer"
  ]
}
```

Raw output:
```text
{
  "components": [
    "weighted head",
    "long handle",
    "target object"
  ],
  "functions": [
    "swing",
    "deliver impact",
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle-to-user grip",
    "head-to-target contact"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: Swinging motion imparts kinetic energy to the handle.",
      "support_status": "supported",
      "source_span_id": 0
    },
    {
      "fact": "Conversion: Rigid handle transfers kinetic energy to the weighted head, concentrating force onto a small contact area.",
      "support_status": "supported",
      "source_span_id": 1
    },
    {
      "fact": "Output: Concentrated impact delivers mechanical work to the target object, causing fastening, deformation, or fragmentation.",
      "support_status": "supported",
      "source_span_id": 2
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_1",
      "source_span_id": 0,
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": 1,
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": 2,
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "energy_input",
      "force_concentration",
      "impact_output"
    ],
    "known_components": [
      "weighted head",
      "long handle",
      "target object"
    ],
    "known_interfaces": [
      "handle-to-user grip",
      "head-to-target contact"
    ],
    "known_mechanism_facts": [
      "Input: Swinging motion imparts kinetic energy to the handle.",
      "Conversion: Rigid handle transfers kinetic energy to the weighted head, concentrating force onto a small contact area.",
      "Output: Concentrated impact delivers mechanical work to the target object, causing fastening, deformation, or fragmentation."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "user_grip_dynamics",
    "handle_material_properties_and_damping",
    "contact_stress_distribution_at_impact",
    "target_material_yield_strength",
    "energy_efficiency_of_transfer"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The functional execution of a spray bottle follows a canonical causal chain in engineering ontology: user actuation initiates the operating mechanism, an internal linkage transmits force and fluid dynamics, the working contact (nozzle/orifice) interfaces with the target medium, and the named engineering output (atomized spray) is subsequently produced. Option C preserves this strict chronological and dependency-ordered sequence required for the artifact's intended function.",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The functional execution of a spray bottle follows a canonical causal chain in engineering ontology: user actuation initiates the operating mechanism, an internal linkage transmits force and fluid dynamics, the working contact (nozzle/orifice) interfaces with the target medium, and the named engineering output (atomized spray) is subsequently produced. Option C preserves this strict chronological and dependency-ordered sequence required for the artifact's intended function.",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "terminate_extraction",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## glm-5.2

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver impact to small area of object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle",
    "impact contact with object surface"
  ],
  "mechanism_facts": [
    {
      "fact": "Hammer consists of a weighted head fixed to a long handle",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The handle is swung to deliver an impact to a small area of an object",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "The impact can drive nails into wood",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "The impact can shape metal (as with a forge)",
      "support_status": "supported",
      "source_span_id": "span_4"
    },
    {
      "fact": "The impact can crush rock",
      "support_status": "supported",
      "source_span_id": "span_5"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": 3,
      "source_span_id": "span_4",
      "support_status": "supported"
    },
    {
      "fact_id": 4,
      "source_span_id": "span_5",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "component composition",
      "input action (swing)",
      "output functions"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "head fixed to handle",
      "impact contact with object surface"
    ],
    "known_mechanism_facts": [
      "Hammer consists of a weighted head fixed to a long handle",
      "The handle is swung to deliver an impact to a small area of an object",
      "The impact can drive nails into wood",
      "The impact can shape metal",
      "The impact can crush rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "force transfer mechanism from handle to head",
    "energy conversion dynamics of the swing",
    "material properties of head enabling impact concentration to small area"
  ]
}
```

Raw output:
```text
```json
{
  "components": ["weighted head", "long handle"],
  "functions": ["deliver impact to small area of object", "drive nails into wood", "shape metal", "crush rock"],
  "interfaces": ["head fixed to handle", "impact contact with object surface"],
  "mechanism_facts": [
    {
      "fact": "Hammer consists of a weighted head fixed to a long handle",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The handle is swung to deliver an impact to a small area of an object",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "The impact can drive nails into wood",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "The impact can shape metal (as with a forge)",
      "support_status": "supported",
      "source_span_id": "span_4"
    },
    {
      "fact": "The impact can crush rock",
      "support_status": "supported",
      "source_span_id": "span_5"
    }
  ],
  "evidence_mapping": [
    {"fact_id": 0, "source_span_id": "span_1", "support_status": "supported"},
    {"fact_id": 1, "source_span_id": "span_2", "support_status": "supported"},
    {"fact_id": 2, "source_span_id": "span_3", "support_status": "supported"},
    {"fact_id": 3, "source_span_id": "span_4", "support_status": "supported"},
    {"fact_id": 4, "source_span_id": "span_5", "support_status": "supported"}
  ],
  "state_update": {
    "covered_critical_states": ["component composition", "input action (swing)", "output functions"],
    "known_components": ["weighted head", "long handle"],
    "known_interfaces": ["head fixed to handle", "impact contact with object surface"],
    "known_mechanism_facts": [
      "Hammer consists of a weighted head fixed to a long handle",
      "The handle is swung to deliver an impact to a small area of an object",
      "The impact can drive nails into wood",
      "The impact can shape metal",
      "The impact can crush rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "force transfer mechanism from handle to head",
    "energy conversion dynamics of the swing",
    "material properties of head enabling impact concentration to small area"
  ]
}
```
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The correct functional sequence for a spray bottle follows the causal chain of energy and action: user input starts the operating mechanism (trigger), an internal linkage transfers the action (piston and fluid chamber), the working contact acts on the target (nozzle emitting spray), and the named engineering output is produced (liquid sprayed).",
  "confidence": 0.98
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The correct functional sequence for a spray bottle follows the causal chain of energy and action: user input starts the operating mechanism (trigger), an internal linkage transfers the action (piston and fluid chamber), the working contact acts on the target (nozzle emitting spray), and the named engineering output is produced (liquid sprayed).",
  "confidence": 0.98
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "none",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "none",
  "reason_consistency": "consistent"
}
```
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## qwen3.6-35b-a3b

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00292

- Artifact: `GEN_A_WASHING_MACHINE` / Washing machine
- Category: `A` | Language: `en` | Question family: `removal_effect_reasoning`
- Key metrics: ontology_f1=0.0, relation_f1=0.5, boundary_accuracy=0.5, minimal_system_accuracy=0.8, removal_effect_accuracy=0.0

Parsed JSON:
```json
{
  "components": [
    "indoor plumbing",
    "pump",
    "well",
    "spring"
  ],
  "functions": [
    "direct water delivery for laundry processes",
    "manual water transport"
  ],
  "interfaces": [
    "water source connection point"
  ],
  "mechanism_facts": [
    {
      "fact": "Removal of indoor plumbing eliminates direct water access, resulting in the functional loss of automated water delivery and necessitating manual carriage of water from external sources for washing, boiling, and rinsing.",
      "support_status": "supported",
      "source_span_id": 0
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "mech_fact_1",
      "source_span_id": 0,
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [],
    "known_components": [
      "indoor plumbing",
      "pump",
      "well",
      "spring"
    ],
    "known_interfaces": [
      "water source connection point"
    ],
    "known_mechanism_facts": [
      "Removal of indoor plumbing eliminates direct water access, resulting in the functional loss of automated water delivery and necessitating manual carriage of water from external sources for washing, boiling, and rinsing."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "water pressure requirements",
    "flow rate specifications",
    "temperature control thresholds",
    "agitation force parameters"
  ]
}
```

Raw output:
```text
{
  "components": ["indoor plumbing", "pump", "well", "spring"],
  "functions": ["direct water delivery for laundry processes", "manual water transport"],
  "interfaces": ["water source connection point"],
  "mechanism_facts": [
    {
      "fact": "Removal of indoor plumbing eliminates direct water access, resulting in the functional loss of automated water delivery and necessitating manual carriage of water from external sources for washing, boiling, and rinsing.",
      "support_status": "supported",
      "source_span_id": 0
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "mech_fact_1",
      "source_span_id": 0,
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [],
    "known_components": ["indoor plumbing", "pump", "well", "spring"],
    "known_interfaces": ["water source connection point"],
    "known_mechanism_facts": ["Removal of indoor plumbing eliminates direct water access, resulting in the functional loss of automated water delivery and necessitating manual carriage of water from external sources for washing, boiling, and rinsing."],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "water pressure requirements",
    "flow rate specifications",
    "temperature control thresholds",
    "agitation force parameters"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "In engineering function ontologies, the canonical causal sequence for a mechanical system follows: actuation (user input) initiates the process, transmission (internal linkage) propagates the action, interaction (working contact) applies force to the target domain, and realization (named engineering output) yields the intended effect. For the spray bottle, pressing the pump triggers the rod, which drives the nozzle against the fluid, resulting in atomization. Option C correctly preserves this normalized functional chain.",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "In engineering function ontologies, the canonical causal sequence for a mechanical system follows: actuation (user input) initiates the process, transmission (internal linkage) propagates the action, interaction (working contact) applies force to the target domain, and realization (named engineering output) yields the intended effect. For the spray bottle, pressing the pump triggers the rod, which drives the nozzle against the fluid, resulting in atomization. Option C correctly preserves this normalized functional chain.",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision":"best_stop_round","selected_round":3,"sufficiency_gap":[],"reason_consistency":"consistent"}
```

## qwen3.6-flash

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle",
    "target object"
  ],
  "functions": [
    "swing",
    "transfer kinetic energy",
    "concentrate force",
    "deliver impact",
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle-grip interface",
    "head-target contact interface"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: Swinging the handle generates kinetic energy.",
      "support_status": "supported",
      "source_span_id": "[78-92]"
    },
    {
      "fact": "Conversion: The rigid handle transfers energy to the weighted head, concentrating force on a small area.",
      "support_status": "supported",
      "source_span_id": "[45-135]"
    },
    {
      "fact": "Output: The concentrated impact is delivered to the target object to drive, shape, or crush it.",
      "support_status": "supported",
      "source_span_id": "[136-248]"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "[78-92]",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "[45-135]",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "[136-248]",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input_kinetic_generation",
      "energy_transfer_path",
      "output_impact_effect"
    ],
    "known_components": [
      "weighted head",
      "long handle",
      "target object"
    ],
    "known_interfaces": [
      "handle-grip interface",
      "head-target contact interface"
    ],
    "known_mechanism_facts": [
      "Input: swinging generates kinetic energy",
      "Conversion: rigid transfer concentrates force",
      "Output: impact causes penetration/deformation/fracture"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "material_composition_and_properties",
    "impact_force_profile_and_duration",
    "energy_dissipation_and_heat_generation",
    "grip_stability_and_wrist_mechanics"
  ]
}
```

Raw output:
```text
{
  "components": ["weighted head", "long handle", "target object"],
  "functions": ["swing", "transfer kinetic energy", "concentrate force", "deliver impact", "drive nails", "shape metal", "crush rock"],
  "interfaces": ["handle-grip interface", "head-target contact interface"],
  "mechanism_facts": [
    {
      "fact": "Input: Swinging the handle generates kinetic energy.",
      "support_status": "supported",
      "source_span_id": "[78-92]"
    },
    {
      "fact": "Conversion: The rigid handle transfers energy to the weighted head, concentrating force on a small area.",
      "support_status": "supported",
      "source_span_id": "[45-135]"
    },
    {
      "fact": "Output: The concentrated impact is delivered to the target object to drive, shape, or crush it.",
      "support_status": "supported",
      "source_span_id": "[136-248]"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "[78-92]",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "[45-135]",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "[136-248]",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": ["input_kinetic_generation", "energy_transfer_path", "output_impact_effect"],
    "known_components": ["weighted head", "long handle", "target object"],
    "known_interfaces": ["handle-grip interface", "head-target contact interface"],
    "known_mechanism_facts": ["Input: swinging generates kinetic energy", "Conversion: rigid transfer concentrates force", "Output: impact causes penetration/deformation/fracture"],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "material_composition_and_properties",
    "impact_force_profile_and_duration",
    "energy_dissipation_and_heat_generation",
    "grip_stability_and_wrist_mechanics"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "In engineering function ontologies, the execution of a named engineering function follows a canonical causal-temporal chain: user input initiates the operating mechanism, an internal linkage transmits energy or motion, the working contact applies force to the target, and the named engineering output is generated. Option C correctly sequences these normalized functional relations from trigger to result.",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "In engineering function ontologies, the execution of a named engineering function follows a canonical causal-temporal chain: user input initiates the operating mechanism, an internal linkage transmits energy or motion, the working contact applies force to the target, and the named engineering output is generated. Option C correctly sequences these normalized functional relations from trigger to result.",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## deepseek-v4-flash

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.26666666666666666, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "head",
    "handle"
  ],
  "functions": [
    "deliver impact",
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head-object contact",
    "handle-user grip"
  ],
  "mechanism_facts": [
    {
      "fact": "A hammer consists of a weighted head fixed to a long handle.",
      "support_status": "supported",
      "source_span_id": "S1"
    },
    {
      "fact": "A hammer is swung to deliver an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "S1"
    },
    {
      "fact": "A hammer can be used to drive nails into wood.",
      "support_status": "supported",
      "source_span_id": "S2"
    },
    {
      "fact": "A hammer can be used to shape metal.",
      "support_status": "supported",
      "source_span_id": "S2"
    },
    {
      "fact": "A hammer can be used to crush rock.",
      "support_status": "supported",
      "source_span_id": "S2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact1",
      "source_span_id": "S1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact2",
      "source_span_id": "S1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact3",
      "source_span_id": "S2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact4",
      "source_span_id": "S2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact5",
      "source_span_id": "S2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "swinging",
      "impact delivery",
      "nail driving",
      "metal shaping",
      "rock crushing"
    ],
    "known_components": [
      "head",
      "handle"
    ],
    "known_interfaces": [
      "head-object contact",
      "handle-user grip"
    ],
    "known_mechanism_facts": [
      "A hammer consists of a weighted head fixed to a long handle.",
      "A hammer is swung to deliver an impact to a small area of an object.",
      "A hammer can be used to drive nails into wood.",
      "A hammer can be used to shape metal.",
      "A hammer can be used to crush rock."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": []
}
```

Raw output:
```text
{
  "components": ["head", "handle"],
  "functions": ["deliver impact", "drive nails", "shape metal", "crush rock"],
  "interfaces": ["head-object contact", "handle-user grip"],
  "mechanism_facts": [
    {
      "fact": "A hammer consists of a weighted head fixed to a long handle.",
      "support_status": "supported",
      "source_span_id": "S1"
    },
    {
      "fact": "A hammer is swung to deliver an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "S1"
    },
    {
      "fact": "A hammer can be used to drive nails into wood.",
      "support_status": "supported",
      "source_span_id": "S2"
    },
    {
      "fact": "A hammer can be used to shape metal.",
      "support_status": "supported",
      "source_span_id": "S2"
    },
    {
      "fact": "A hammer can be used to crush rock.",
      "support_status": "supported",
      "source_span_id": "S2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact1",
      "source_span_id": "S1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact2",
      "source_span_id": "S1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact3",
      "source_span_id": "S2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact4",
      "source_span_id": "S2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact5",
      "source_span_id": "S2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": ["swinging", "impact delivery", "nail driving", "metal shaping", "rock crushing"],
    "known_components": ["head", "handle"],
    "known_interfaces": ["head-object contact", "handle-user grip"],
    "known_mechanism_facts": [
      "A hammer consists of a weighted head fixed to a long handle.",
      "A hammer is swung to deliver an impact to a small area of an object.",
      "A hammer can be used to drive nails into wood.",
      "A hammer can be used to shape metal.",
      "A hammer can be used to crush rock."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": []
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The correct sequence for a spray bottle's function is: user input initiates the mechanism, an internal linkage transfers the action, the working contact (nozzle) acts on the target (liquid), and then the named engineering output (spray) is produced. Option C matches this order.",
  "confidence": 0.95
}
```

Raw output:
```text
{"answer": "C", "reasoning": "The correct sequence for a spray bottle's function is: user input initiates the mechanism, an internal linkage transfers the action, the working contact (nozzle) acts on the target (liquid), and then the named engineering output (spray) is produced. Option C matches this order.", "confidence": 0.95}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00207_2

- Artifact: `GEN_A_SCISSORS` / scissors
- Category: `A` | Language: `en` | Question family: `interface_boundary`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "no further extraction needed",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "no further extraction needed",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00281_3

- Artifact: `GEN_A_VACUUM_CLEANER` / Vacuum cleaner
- Category: `A` | Language: `en` | Question family: `failure_propagation`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## qwen3.6-max-preview

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.26666666666666666, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "head",
    "handle"
  ],
  "functions": [
    "deliver impact",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: The long handle is swung by a user to initiate motion",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Conversion: Swinging motion transfers kinetic energy to the weighted head to generate an impact",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "Conversion: The impact force is concentrated onto a small area of the target object",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Output: The concentrated impact deforms or displaces the target to drive nails, shape metal, or crush rock",
      "support_status": "supported",
      "source_span_id": "span_4"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": 3,
      "source_span_id": "span_4",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input_swing_motion",
      "kinetic_transfer_to_head",
      "impact_concentration",
      "output_target_deformation"
    ],
    "known_components": [
      "head",
      "handle"
    ],
    "known_interfaces": [
      "head fixed to handle"
    ],
    "known_mechanism_facts": [
      "handle_swing_input",
      "head_impact_conversion",
      "force_area_concentration",
      "material_deformation_output"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "user_hand_grip_interface",
    "leverage_mechanical_advantage_ratio",
    "kinetic_to_force_energy_conversion_efficiency",
    "recoil_vibration_dissipation_path",
    "handle_flexure_during_impact"
  ]
}
```

Raw output:
```text
{
  "components": [
    "head",
    "handle"
  ],
  "functions": [
    "deliver impact",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: The long handle is swung by a user to initiate motion",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Conversion: Swinging motion transfers kinetic energy to the weighted head to generate an impact",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "Conversion: The impact force is concentrated onto a small area of the target object",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Output: The concentrated impact deforms or displaces the target to drive nails, shape metal, or crush rock",
      "support_status": "supported",
      "source_span_id": "span_4"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": 3,
      "source_span_id": "span_4",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input_swing_motion",
      "kinetic_transfer_to_head",
      "impact_concentration",
      "output_target_deformation"
    ],
    "known_components": [
      "head",
      "handle"
    ],
    "known_interfaces": [
      "head fixed to handle"
    ],
    "known_mechanism_facts": [
      "handle_swing_input",
      "head_impact_conversion",
      "force_area_concentration",
      "material_deformation_output"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "user_hand_grip_interface",
    "leverage_mechanical_advantage_ratio",
    "kinetic_to_force_energy_conversion_efficiency",
    "recoil_vibration_dissipation_path",
    "handle_flexure_during_impact"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The functional sequence follows a causal chain consistent with engineering design ontologies: actuation (user input starts the operating mechanism) → transmission (internal linkage transfers the action) → interaction (working contact acts on the target) → output realization (named engineering output is produced). Option C preserves this temporal and causal precedence, whereas other options misorder transmission, interaction, or output generation.",
  "confidence": 0.95
}
```

Raw output:
```text
{"answer": "C", "reasoning": "The functional sequence follows a causal chain consistent with engineering design ontologies: actuation (user input starts the operating mechanism) → transmission (internal linkage transfers the action) → interaction (working contact acts on the target) → output realization (named engineering output is produced). Option C preserves this temporal and causal precedence, whereas other options misorder transmission, interaction, or output generation.", "confidence": 0.95}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "stop", "sufficiency_gap": [], "next_extraction_action": "finalize_extraction", "reason_consistency": "consistent"}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{"decision": "best_stop_round", "selected_round": 3, "sufficiency_gap": [], "reason_consistency": "consistent"}
```

## qwen3.7-max

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver impact to a small area",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "hand-to-handle interface",
    "head-to-object impact interface"
  ],
  "mechanism_facts": [
    {
      "fact": "The hammer consists of a weighted head fixed to a long handle",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The handle is swung by the user to generate kinetic energy",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "The swinging motion delivers an impact to a small area of an object",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "The impact can drive nails into wood",
      "support_status": "supported",
      "source_span_id": "span_4"
    },
    {
      "fact": "The impact can shape metal",
      "support_status": "supported",
      "source_span_id": "span_5"
    },
    {
      "fact": "The impact can crush rock",
      "support_status": "supported",
      "source_span_id": "span_6"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_4",
      "source_span_id": "span_4",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_5",
      "source_span_id": "span_5",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_6",
      "source_span_id": "span_6",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "component assembly (head fixed to handle)",
      "swinging input motion",
      "impact delivery to small area",
      "output applications (nails, metal, rock)"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "hand-to-handle interface",
      "head-to-object impact interface"
    ],
    "known_mechanism_facts": [
      "weighted head fixed to long handle",
      "handle swung to deliver impact",
      "impact concentrated on small area",
      "drives nails into wood",
      "shapes metal",
      "crushes rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "grip mechanics: how the hand grasps and controls the handle",
    "force amplification: how handle length and head mass convert swing velocity into impact force",
    "energy transfer dynamics: how kinetic energy transfers from head to target object during impact",
    "head material properties: hardness and mass characteristics enabling effective impact",
    "rebound and vibration: what happens to residual energy after impact"
  ]
}
```

Raw output:
```text
```json
{
  "components": ["weighted head", "long handle"],
  "functions": ["deliver impact to a small area", "drive nails into wood", "shape metal", "crush rock"],
  "interfaces": ["hand-to-handle interface", "head-to-object impact interface"],
  "mechanism_facts": [
    {"fact": "The hammer consists of a weighted head fixed to a long handle", "support_status": "supported", "source_span_id": "span_1"},
    {"fact": "The handle is swung by the user to generate kinetic energy", "support_status": "supported", "source_span_id": "span_2"},
    {"fact": "The swinging motion delivers an impact to a small area of an object", "support_status": "supported", "source_span_id": "span_3"},
    {"fact": "The impact can drive nails into wood", "support_status": "supported", "source_span_id": "span_4"},
    {"fact": "The impact can shape metal", "support_status": "supported", "source_span_id": "span_5"},
    {"fact": "The impact can crush rock", "support_status": "supported", "source_span_id": "span_6"}
  ],
  "evidence_mapping": [
    {"fact_id": "fact_1", "source_span_id": "span_1", "support_status": "supported"},
    {"fact_id": "fact_2", "source_span_id": "span_2", "support_status": "supported"},
    {"fact_id": "fact_3", "source_span_id": "span_3", "support_status": "supported"},
    {"fact_id": "fact_4", "source_span_id": "span_4", "support_status": "supported"},
    {"fact_id": "fact_5", "source_span_id": "span_5", "support_status": "supported"},
    {"fact_id": "fact_6", "source_span_id": "span_6", "support_status": "supported"}
  ],
  "state_update": {
    "covered_critical_states": ["component assembly (head fixed to handle)", "swinging input motion", "impact delivery to small area", "output applications (nails, metal, rock)"],
    "known_components": ["weighted head", "long handle"],
    "known_interfaces": ["hand-to-handle interface", "head-to-object impact interface"],
    "known_mechanism_facts": ["weighted head fixed to long handle", "handle swung to deliver impact", "impact concentrated on small area", "drives nails into wood", "shapes metal", "crushes rock"],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "grip mechanics: how the hand grasps and controls the handle",
    "force amplification: how handle length and head mass convert swing velocity into impact force",
    "energy transfer dynamics: how kinetic energy transfers from head to target object during impact",
    "head material properties: hardness and mass characteristics 
...<truncated>...
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The correct causal and chronological sequence for a mechanical device like a spray bottle begins with user input (squeezing the trigger) starting the operating mechanism. This action is then transferred via an internal linkage (the pump and piston assembly). Next, the working contact acts on the target (dispensing the atomized liquid onto the surface), which ultimately results in the named engineering output being produced.",
  "confidence": 1.0
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The correct causal and chronological sequence for a mechanical device like a spray bottle begins with user input (squeezing the trigger) starting the operating mechanism. This action is then transferred via an internal linkage (the pump and piston assembly). Next, the working contact acts on the target (dispensing the atomized liquid onto the surface), which ultimately results in the named engineering output being produced.",
  "confidence": 1.0
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00281_3

- Artifact: `GEN_A_VACUUM_CLEANER` / Vacuum cleaner
- Category: `A` | Language: `en` | Question family: `failure_propagation`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## qwen3.7-max-preview

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver an impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle (user grip)",
    "head (impact surface)"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: The long handle is swung by the user.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Conversion: The weighted head fixed to the handle delivers an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Output: The impact drives nails into wood, shapes metal, or crushes rock.",
      "support_status": "supported",
      "source_span_id": "span_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_0",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_1",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input: swinging handle",
      "conversion: impact delivery via weighted head",
      "output: material displacement or fracture"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "handle (user grip)",
      "head (impact surface)"
    ],
    "known_mechanism_facts": [
      "Input: The long handle is swung by the user.",
      "Conversion: The weighted head fixed to the handle delivers an impact to a small area of an object.",
      "Output: The impact drives nails into wood, shapes metal, or crushes rock."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "kinetic energy transfer mechanics from user to handle",
    "momentum accumulation and transfer within the weighted head",
    "force concentration and distribution mechanics at the impact surface",
    "material deformation, displacement, or fracture mechanics of the target object"
  ]
}
```

Raw output:
```text
 *   ```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver an impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle (user grip)",
    "head (impact surface)"
  ],
  "mechanism_facts": [
    {
      "fact": "Input: The long handle is swung by the user.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Conversion: The weighted head fixed to the handle delivers an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "Output: The impact drives nails into wood, shapes metal, or crushes rock.",
      "support_status": "supported",
      "source_span_id": "span_1"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_0",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_1",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_1",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input: swinging handle",
      "conversion: impact delivery via weighted head",
      "output: material displacement or fracture"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "handle (user grip)",
      "head (impact surface)"
    ],
    "known_mechanism_facts": [
      "Input: The long handle is swung by the user.",
      "Conversion: The weighted head fixed to the handle delivers an impact to a small area of an object.",
      "Output: The impact drives nails into wood, shapes metal, or crushes rock."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "kinetic energy transfer mechanics from user to handle",
    "momentum accumulation and transfer within the weighted head",
    "force concentration and distribution mechanics at the impact surface",
    "material deformation, displacement, or fracture mechanics of the target object"
  ]
}
```
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The functional operation of a spray bottle follows a strict causal sequence: user input initiates the operating mechanism (pressing the trigger), an internal linkage transfers the action (piston and valves pressurize the fluid), the working contact acts on the target (fluid is atomized and applied), and the named engineering output is produced (the target is sprayed). Option C correctly orders these functional dependencies.",
  "confidence": 0.98
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The functional operation of a spray bottle follows a strict causal sequence: user input initiates the operating mechanism (pressing the trigger), an internal linkage transfers the action (piston and valves pressurize the fluid), the working contact acts on the target (fluid is atomized and applied), and the named engineering output is produced (the target is sprayed). Option C correctly orders these functional dependencies.",
  "confidence": 0.98
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Finalize the extracted input-conversion-output mechanism chain as all critical states are covered and marginal gain is low.",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Finalize the extracted input-conversion-output mechanism chain as all critical states are covered and marginal gain is low.",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## qwen3.7-max-2026-05-20

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver impact to a small area",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "hand grip on handle",
    "head contact surface with object"
  ],
  "mechanism_facts": [
    {
      "fact": "Hammer consists of a weighted head fixed to a long handle",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "The handle is swung to generate motion",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Swinging delivers an impact to a small area of an object",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "Impact can drive nails into wood",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Impact can shape metal",
      "support_status": "supported",
      "source_span_id": "span_4"
    },
    {
      "fact": "Impact can crush rock",
      "support_status": "supported",
      "source_span_id": "span_5"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_0",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_4",
      "source_span_id": "span_4",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_5",
      "source_span_id": "span_5",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "component_assembly",
      "swing_input",
      "impact_output"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "hand grip on handle",
      "head contact surface with object"
    ],
    "known_mechanism_facts": [
      "Hammer consists of a weighted head fixed to a long handle",
      "The handle is swung to generate motion",
      "Swinging delivers an impact to a small area of an object",
      "Impact can drive nails into wood",
      "Impact can shape metal",
      "Impact can crush rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "force_amplification_through_leverage",
    "kinetic_energy_transfer_from_handle_to_head",
    "user_grip_mechanics",
    "swing_arc_and_velocity_dynamics",
    "contact_deformation_mechanics"
  ]
}
```

Raw output:
```text
```json
{
  "components": ["weighted head", "long handle"],
  "functions": ["deliver impact to a small area", "drive nails into wood", "shape metal", "crush rock"],
  "interfaces": ["hand grip on handle", "head contact surface with object"],
  "mechanism_facts": [
    {"fact": "Hammer consists of a weighted head fixed to a long handle", "support_status": "supported", "source_span_id": "span_0"},
    {"fact": "The handle is swung to generate motion", "support_status": "supported", "source_span_id": "span_1"},
    {"fact": "Swinging delivers an impact to a small area of an object", "support_status": "supported", "source_span_id": "span_2"},
    {"fact": "Impact can drive nails into wood", "support_status": "supported", "source_span_id": "span_3"},
    {"fact": "Impact can shape metal", "support_status": "supported", "source_span_id": "span_4"},
    {"fact": "Impact can crush rock", "support_status": "supported", "source_span_id": "span_5"}
  ],
  "evidence_mapping": [
    {"fact_id": "fact_0", "source_span_id": "span_0", "support_status": "supported"},
    {"fact_id": "fact_1", "source_span_id": "span_1", "support_status": "supported"},
    {"fact_id": "fact_2", "source_span_id": "span_2", "support_status": "supported"},
    {"fact_id": "fact_3", "source_span_id": "span_3", "support_status": "supported"},
    {"fact_id": "fact_4", "source_span_id": "span_4", "support_status": "supported"},
    {"fact_id": "fact_5", "source_span_id": "span_5", "support_status": "supported"}
  ],
  "state_update": {
    "covered_critical_states": ["component_assembly", "swing_input", "impact_output"],
    "known_components": ["weighted head", "long handle"],
    "known_interfaces": ["hand grip on handle", "head contact surface with object"],
    "known_mechanism_facts": [
      "Hammer consists of a weighted head fixed to a long handle",
      "The handle is swung to generate motion",
      "Swinging delivers an impact to a small area of an object",
      "Impact can drive nails into wood",
      "Impact can shape metal",
      "Impact can crush rock"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "force_amplification_through_leverage",
    "kinetic_energy_transfer_from_handle_to_head",
    "user_grip_mechanics",
    "swing_arc_and_velocity_dynamics",
    "contact_deformation_mechanics"
  ]
}
```
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The correct operational sequence for a spray bottle begins with user input (squeezing the trigger), which activates an internal linkage (the pump mechanism) that transfers the action to the working contact (the nozzle), which acts on the target (the liquid) to produce the named engineering output (the spray). Option C follows this logical chronological and causal order.",
  "confidence": 1.0
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The correct operational sequence for a spray bottle begins with user input (squeezing the trigger), which activates an internal linkage (the pump mechanism) that transfers the action to the working contact (the nozzle), which acts on the target (the liquid) to produce the named engineering output (the spray). Option C follows this logical chronological and causal order.",
  "confidence": 1.0
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_and_output_mechanism_chain",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_and_output_mechanism_chain",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## qwen3.7-max-2026-06-08

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "hand-to-handle interface (hand tool)",
    "head-to-object impact interface"
  ],
  "mechanism_facts": [
    {
      "fact": "Hammer consists of a weighted head fixed to a long handle",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "The handle is swung to generate motion",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Swinging delivers an impact to a small area of an object",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "Impact can drive nails into wood",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Impact can shape metal",
      "support_status": "supported",
      "source_span_id": "span_4"
    },
    {
      "fact": "Impact can crush rock",
      "support_status": "supported",
      "source_span_id": "span_5"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_0",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_4",
      "source_span_id": "span_4",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_5",
      "source_span_id": "span_5",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "component assembly (head fixed to handle)",
      "input action (swinging handle)",
      "output action (impact delivery to small area)"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "hand-to-handle interface",
      "head-to-object impact interface"
    ],
    "known_mechanism_facts": [
      "weighted head fixed to long handle",
      "handle is swung to deliver impact",
      "impact delivered to small area of object"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "user grip and force application on handle (input state)",
    "kinetic energy accumulation during swing arc (conversion state)",
    "lever/pivot mechanics of handle amplifying force (conversion state)",
    "energy transfer from handle to head at moment of impact (conversion state)",
    "force concentration at small contact area of head (output state)",
    "material deformation or displacement of target object (output state)"
  ]
}
```

Raw output:
```text
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "hand-to-handle interface (hand tool)",
    "head-to-object impact interface"
  ],
  "mechanism_facts": [
    {
      "fact": "Hammer consists of a weighted head fixed to a long handle",
      "support_status": "supported",
      "source_span_id": "span_0"
    },
    {
      "fact": "The handle is swung to generate motion",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "Swinging delivers an impact to a small area of an object",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "Impact can drive nails into wood",
      "support_status": "supported",
      "source_span_id": "span_3"
    },
    {
      "fact": "Impact can shape metal",
      "support_status": "supported",
      "source_span_id": "span_4"
    },
    {
      "fact": "Impact can crush rock",
      "support_status": "supported",
      "source_span_id": "span_5"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_0",
      "source_span_id": "span_0",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_3",
      "source_span_id": "span_3",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_4",
      "source_span_id": "span_4",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_5",
      "source_span_id": "span_5",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "component assembly (head fixed to handle)",
      "input action (swinging handle)",
      "output action (impact delivery to small area)"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "hand-to-handle interface",
      "head-to-object impact interface"
    ],
    "known_mechanism_facts": [
      "weighted head fixed to long handle",
      "handle is swung to deliver impact",
      "impact delivered to small area of object"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "user
...<truncated>...
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The functional sequence of a spray bottle follows a logical causal chain: user input (squeezing the trigger) starts the operating mechanism, an internal linkage (pump and fluid channel) transfers the action, the working contact (atomized liquid) acts on the target (surface), and finally the named engineering output (e.g., wetting, cleaning, or misting) is produced.",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The functional sequence of a spray bottle follows a logical causal chain: user input (squeezing the trigger) starts the operating mechanism, an internal linkage (pump and fluid channel) transfers the action, the working contact (atomized liquid) acts on the target (surface), and finally the named engineering output (e.g., wetting, cleaning, or misting) is produced.",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## qwen3.7-max-2026-05-17

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver an impact",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle",
    "head impact surface to object"
  ],
  "mechanism_facts": [
    {
      "fact": "The handle is swung to provide input motion.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The weighted head delivers an impact to a small area of an object as the output.",
      "support_status": "supported",
      "source_span_id": "span_2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "swinging motion input",
      "impact delivery output"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "head to handle joint",
      "head to object contact"
    ],
    "known_mechanism_facts": [
      "handle is swung",
      "head delivers impact"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "conversion of kinetic energy to work/deformation energy",
    "user biomechanical input and grip mechanics",
    "target material stress-strain response"
  ]
}
```

Raw output:
```text
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver an impact",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle",
    "head impact surface to object"
  ],
  "mechanism_facts": [
    {
      "fact": "The handle is swung to provide input motion.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The weighted head delivers an impact to a small area of an object as the output.",
      "support_status": "supported",
      "source_span_id": "span_2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact_1",
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact_2",
      "source_span_id": "span_2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "swinging motion input",
      "impact delivery output"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "head to handle joint",
      "head to object contact"
    ],
    "known_mechanism_facts": [
      "handle is swung",
      "head delivers impact"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "conversion of kinetic energy to work/deformation energy",
    "user biomechanical input and grip mechanics",
    "target material stress-strain response"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_TAPE_MEASURE_STRUCTURAL_DECOMPOSITION_04_1442_ZH

- Artifact: `GEN_A_TAPE_MEASURE` / Tape measure
- Category: `A` | Language: `zh` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "卷尺实现其主要工程功能的逻辑链条为：首先由用户输入启动操作机构（如拉动尺带），接着通过内部连接关系（如发条弹簧和卷轴机构）传递动作，然后工作接触部分（尺带及端钩）作用于目标对象（被测物体），最终形成卷尺的主要功能输出（获取并显示长度测量结果）。选项C准确描述了这一功能因果与时间顺序。",
  "confidence": 0.98
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "卷尺实现其主要工程功能的逻辑链条为：首先由用户输入启动操作机构（如拉动尺带），接着通过内部连接关系（如发条弹簧和卷轴机构）传递动作，然后工作接触部分（尺带及端钩）作用于目标对象（被测物体），最终形成卷尺的主要功能输出（获取并显示长度测量结果）。选项C准确描述了这一功能因果与时间顺序。",
  "confidence": 0.98
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "finalize_extraction",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## qwen3.7-plus

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00074

- Artifact: `GEN_A_DOOR_HANDLE` / Door handle
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.3333333333333333, boundary_accuracy=0.8, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "door handle",
    "doorknob",
    "door"
  ],
  "functions": [
    "open door",
    "close door"
  ],
  "interfaces": [
    "door handle mounted on door"
  ],
  "mechanism_facts": [
    {
      "fact": "door handle is used to open or close a door",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "door handle is mounted on doors",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "input-conversion-output mechanism chain (e.g. handle rotation to latch retraction) is missing",
      "support_status": "missing",
      "source_span_id": ""
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "",
      "support_status": "missing"
    }
  ],
  "state_update": {
    "covered_critical_states": [],
    "known_components": [
      "door handle",
      "doorknob",
      "door"
    ],
    "known_interfaces": [
      "door handle mounted on door"
    ],
    "known_mechanism_facts": [
      "door handle is used to open or close a door",
      "door handle is mounted on doors"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "input: user force applied to handle",
    "conversion: mechanical linkage retracting latch",
    "output: door opens or closes"
  ]
}
```

Raw output:
```text
{
  "components": [
    "door handle",
    "doorknob",
    "door"
  ],
  "functions": [
    "open door",
    "close door"
  ],
  "interfaces": [
    "door handle mounted on door"
  ],
  "mechanism_facts": [
    {
      "fact": "door handle is used to open or close a door",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "door handle is mounted on doors",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "input-conversion-output mechanism chain (e.g. handle rotation to latch retraction) is missing",
      "support_status": "missing",
      "source_span_id": ""
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "",
      "support_status": "missing"
    }
  ],
  "state_update": {
    "covered_critical_states": [],
    "known_components": [
      "door handle",
      "doorknob",
      "door"
    ],
    "known_interfaces": [
      "door handle mounted on door"
    ],
    "known_mechanism_facts": [
      "door handle is used to open or close a door",
      "door handle is mounted on doors"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "input: user force applied to handle",
    "conversion: mechanical linkage retracting latch",
    "output: door opens or closes"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The correct chronological and causal sequence for the engineering function of a spray bottle begins with the user input (squeezing the trigger), which is transferred via an internal linkage (the pump mechanism). This forces the fluid through the nozzle, allowing the working contact (the spray/fluid) to act on the target surface, ultimately producing the named engineering output (e.g., cleaning, coating, or wetting).",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The correct chronological and causal sequence for the engineering function of a spray bottle begins with the user input (squeezing the trigger), which is transferred via an internal linkage (the pump mechanism). This forces the fluid through the nozzle, allowing the working contact (the spray/fluid) to act on the target surface, ultimately producing the named engineering output (e.g., cleaning, coating, or wetting).",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Terminate extraction process",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Terminate extraction process",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## deepseek-v4-pro

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=1.0, minimal_system_accuracy=1.0

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle-head fixed connection",
    "head-object impact contact"
  ],
  "mechanism_facts": [
    {
      "fact": "A hammer consists of a weighted head fixed to a long handle.",
      "support_status": "supported",
      "source_span_id": "span-1"
    },
    {
      "fact": "The hammer is swung to deliver an impact.",
      "support_status": "supported",
      "source_span_id": "span-1"
    },
    {
      "fact": "The impact is delivered to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span-1"
    },
    {
      "fact": "The impact can drive nails into wood.",
      "support_status": "supported",
      "source_span_id": "span-2"
    },
    {
      "fact": "The impact can shape metal.",
      "support_status": "supported",
      "source_span_id": "span-2"
    },
    {
      "fact": "The impact can crush rock.",
      "support_status": "supported",
      "source_span_id": "span-2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact-1",
      "source_span_id": "span-1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-2",
      "source_span_id": "span-1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-3",
      "source_span_id": "span-1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-4",
      "source_span_id": "span-2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-5",
      "source_span_id": "span-2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-6",
      "source_span_id": "span-2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input (swinging)",
      "conversion (impact delivery)",
      "output (nail driving, metal shaping, rock crushing)"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "handle-head fixed connection",
      "head-object impact contact"
    ],
    "known_mechanism_facts": [
      "fact-1",
      "fact-2",
      "fact-3",
      "fact-4",
      "fact-5",
      "fact-6"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": []
}
```

Raw output:
```text
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "drive nails",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "handle-head fixed connection",
    "head-object impact contact"
  ],
  "mechanism_facts": [
    {
      "fact": "A hammer consists of a weighted head fixed to a long handle.",
      "support_status": "supported",
      "source_span_id": "span-1"
    },
    {
      "fact": "The hammer is swung to deliver an impact.",
      "support_status": "supported",
      "source_span_id": "span-1"
    },
    {
      "fact": "The impact is delivered to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span-1"
    },
    {
      "fact": "The impact can drive nails into wood.",
      "support_status": "supported",
      "source_span_id": "span-2"
    },
    {
      "fact": "The impact can shape metal.",
      "support_status": "supported",
      "source_span_id": "span-2"
    },
    {
      "fact": "The impact can crush rock.",
      "support_status": "supported",
      "source_span_id": "span-2"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": "fact-1",
      "source_span_id": "span-1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-2",
      "source_span_id": "span-1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-3",
      "source_span_id": "span-1",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-4",
      "source_span_id": "span-2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-5",
      "source_span_id": "span-2",
      "support_status": "supported"
    },
    {
      "fact_id": "fact-6",
      "source_span_id": "span-2",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [
      "input (swinging)",
      "conversion (impact delivery)",
      "output (nail driving, metal shaping, rock crushing)"
    ],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "handle-head fixed connection",
      "head-object impact contact"
    ],
    "known_mechanism_facts": [
      "fact-1",
      "fact-2",
      "fact-3",
      "fact-4",
      "fact-5",
      "fact-6"
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": []
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The correct causal sequence for a spray bottle is: user input (trigger pull) starts the operating mechanism; an internal linkage (piston, spring, tube) transfers the action; the working contact (nozzle) acts on the target (liquid); the named engineering output (spray) is produced. Option C follows this order.",
  "confidence": 0.95
}
```

Raw output:
```text
{"answer": "C", "reasoning": "The correct causal sequence for a spray bottle is: user input (trigger pull) starts the operating mechanism; an internal linkage (piston, spring, tube) transfers the action; the working contact (nozzle) acts on the target (liquid); the named engineering output (spray) is produced. Option C follows this order.", "confidence": 0.95}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "none",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "none",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

## qwen3.7-plus-2026-05-26

### Task0_Evidence_conditioned_Extraction | ordinary_prompt | E2S_V5_00404

- Artifact: `GEN_B_HAMMER` / Hammer
- Category: `B` | Language: `en` | Question family: `functional_behavior`
- Key metrics: ontology_f1=0.0, relation_f1=0.0, boundary_accuracy=0.8, minimal_system_accuracy=0.8

Parsed JSON:
```json
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver an impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle"
  ],
  "mechanism_facts": [
    {
      "fact": "The hammer consists of a weighted head fixed to a long handle.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The hammer is swung to deliver an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "The impact can drive nails into wood, shape metal, or crush rock.",
      "support_status": "supported",
      "source_span_id": "span_3"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "span_3",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "head fixed to handle"
    ],
    "known_mechanism_facts": [
      "The hammer consists of a weighted head fixed to a long handle.",
      "The hammer is swung to deliver an impact to a small area of an object.",
      "The impact can drive nails into wood, shape metal, or crush rock."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "kinetic energy transfer from the swinging handle to the weighted head",
    "force concentration mechanism converting momentum into localized impact pressure"
  ]
}
```

Raw output:
```text
{
  "components": [
    "weighted head",
    "long handle"
  ],
  "functions": [
    "deliver an impact to a small area of an object",
    "drive nails into wood",
    "shape metal",
    "crush rock"
  ],
  "interfaces": [
    "head fixed to handle"
  ],
  "mechanism_facts": [
    {
      "fact": "The hammer consists of a weighted head fixed to a long handle.",
      "support_status": "supported",
      "source_span_id": "span_1"
    },
    {
      "fact": "The hammer is swung to deliver an impact to a small area of an object.",
      "support_status": "supported",
      "source_span_id": "span_2"
    },
    {
      "fact": "The impact can drive nails into wood, shape metal, or crush rock.",
      "support_status": "supported",
      "source_span_id": "span_3"
    }
  ],
  "evidence_mapping": [
    {
      "fact_id": 0,
      "source_span_id": "span_1",
      "support_status": "supported"
    },
    {
      "fact_id": 1,
      "source_span_id": "span_2",
      "support_status": "supported"
    },
    {
      "fact_id": 2,
      "source_span_id": "span_3",
      "support_status": "supported"
    }
  ],
  "state_update": {
    "covered_critical_states": [],
    "known_components": [
      "weighted head",
      "long handle"
    ],
    "known_interfaces": [
      "head fixed to handle"
    ],
    "known_mechanism_facts": [
      "The hammer consists of a weighted head fixed to a long handle.",
      "The hammer is swung to deliver an impact to a small area of an object.",
      "The impact can drive nails into wood, shape metal, or crush rock."
    ],
    "unresolved_conflicts": []
  },
  "missing_critical_states": [
    "kinetic energy transfer from the swinging handle to the weighted head",
    "force concentration mechanism converting momentum into localized impact pressure"
  ]
}
```

### Task1_Diagnostic_QA | ontology_aware_prompt | Q_V41_GEN_A_SPRAY_BOTTLE_STRUCTURAL_DECOMPOSITION_01_0390_EN

- Artifact: `GEN_A_SPRAY_BOTTLE` / Spray bottle
- Category: `A` | Language: `en` | Question family: `structural_decomposition`
- Key metrics: task1_accuracy=1.0, qa_correct=True

Parsed JSON:
```json
{
  "answer": "C",
  "reasoning": "The correct chronological and causal sequence for the engineering function of a spray bottle begins with the user input (squeezing the trigger), which is transferred via an internal linkage (the pump mechanism). This forces the fluid through the nozzle, allowing the working contact (the spray/fluid) to act on the target surface, ultimately producing the named engineering output (e.g., cleaning, coating, or wetting).",
  "confidence": 0.95
}
```

Raw output:
```text
{
  "answer": "C",
  "reasoning": "The correct chronological and causal sequence for the engineering function of a spray bottle begins with the user input (squeezing the trigger), which is transferred via an internal linkage (the pump mechanism). This forces the fluid through the nozzle, allowing the working contact (the spray/fluid) to act on the target surface, ultimately producing the named engineering output (e.g., cleaning, coating, or wetting).",
  "confidence": 0.95
}
```

### Task2_State_to_Stop | bidirectional_prompt | S2S_V5_00092_2

- Artifact: `GEN_A_ELECTRIC_TOOTHBRUSH` / Electric toothbrush
- Category: `A` | Language: `en` | Question family: `functional_behavior`
- Key metrics: stop_accuracy=1.0, cost_reduction=1.0, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Terminate extraction process",
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "stop",
  "sufficiency_gap": [],
  "next_extraction_action": "Terminate extraction process",
  "reason_consistency": "consistent"
}
```

### Task2_Trajectory_to_Stop | ordinary_prompt | T2S_V5_00276_2

- Artifact: `GEN_A_UMBRELLA` / umbrella
- Category: `A` | Language: `en` | Question family: `architecture_tradeoff_optimization`
- Key metrics: stop_accuracy=1.0, cost_reduction=0.4, stop_reason_consistency=1.0

Parsed JSON:
```json
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

Raw output:
```text
{
  "decision": "best_stop_round",
  "selected_round": 3,
  "sufficiency_gap": [],
  "reason_consistency": "consistent"
}
```

