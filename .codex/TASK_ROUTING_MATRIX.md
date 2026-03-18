# Task Routing Matrix

| Task Type      | Primary Agent | Primary Skill                  | Secondary Options                                  | Review Required |
|----------------|---------------|--------------------------------|----------------------------------------------------|-----------------|
| feature        | builder       | feature-ship                   | architect, premium-ui-pass, form-systems          | yes             |
| bug            | tester/builder| bug-hunt                       | pre-merge-review                                   | yes             |
| UI refinement  | ui-designer   | premium-ui-pass                | builder                                             | yes             |
| architecture   | architect     | feature-ship planning mode     | reviewer                                            | usually         |
| review         | reviewer      | pre-merge-review               | none                                                | yes             |
| dashboard      | architect     | dashboard-build                | feature-ship, data-table-master, premium-ui-pass  | yes             |
| auth           | builder       | auth-flow-ship                 | tester, form-systems                               | yes             |
| billing        | builder       | billing-and-checkout           | ui-designer, landing-page-conversion-pass         | yes             |
| onboarding     | architect     | onboarding-flow-ship           | builder, premium-ui-pass                           | yes             |
| table          | builder       | data-table-master              | ui-designer                                         | yes             |
| settings       | ui-designer   | settings-page-pass             | builder, form-systems                              | yes             |
| design-system  | reviewer      | design-system-enforcer         | builder, ui-designer                               | yes             |
| admin          | architect     | admin-panel-ship               | builder, data-table-master                         | yes             |