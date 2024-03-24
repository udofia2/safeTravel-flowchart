```mermaid
graph LR
  A[User opens SafeTravel app] --> B{Trip Initiation (Diamond)}
  B --> C{Yes: Onboarding tutorial}
  B --> D{No: Skip to next step}
  C --> E{Trip Details}
  D --> E
  E --> F{Vehicle Information}
  F --> G{Optional GPS Sharing (Diamond)}
  G --> H{Yes: Share GPS}
  G --> I{No: Skip to next step}
  H --> J{SafeTravel Activated}
  I --> J
  J --> K{Mid-Trip Check-ins}
  K --> L{User takes selfie} --> M{Safe Arrival}
  K --> N{User ignores prompt}
  N --> O{Notification to take selfie}
  O --> L
  N --> P{Ignore multiple prompts}
  P --> Q{Low battery & Critical notification}
  Q --> R{Optional: Emergency background alert}
  K - [Emergency Button Pressed]-> S{Confirmation Prompt}
  S --> T{Cancel} --> K
  S --> U{Confirm Emergency} --> V{Send distress signal}
  V --> W{Emergency alert & Optional call to services}
  M --> X{Trip Record Created}
  X --> Y{Download record (optional)}
  X --> Z{Share data anonymously (optional)}
  Y --> End
  Z --> End

```