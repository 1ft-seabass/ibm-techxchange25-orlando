# Live Demonstration!

![alt text](images/02-live-demonstration/02-live-demonstration.jpg)

It's overview.

![alt text](images/02-live-demonstration/02-live-demonstration-1.jpg)

Meta Quest 3 (XR) UI and IoT Light device.

![alt text](images/02-live-demonstration/02-live-demonstration-5.jpg)

It's first voice recording step.

![alt text](images/02-live-demonstration/02-live-demonstration-2.jpg)

It starts voice recording by pressing Button A. I say "Turn on light.".

![alt text](images/02-live-demonstration/02-live-demonstration-3.jpg)

It stops voice recording by pressing Button A once again. 
The recorded audio is sent to public Whisper API (transcription API).

Whisper API returns the voice-to-text result: "Turn on light".

![alt text](images/02-live-demonstration/02-live-demonstration-4.jpg)

It moves AI Processing step.

![alt text](images/02-live-demonstration/02-live-demonstration-6.jpg)

- Node-RED
  - Ollama API calls with "Turn on light" message.
  - structured outputs JSON scheme with MCP tool list.
- Ollama + Granite LLM
  - Connect to "Turn on light" message to MCP tool choosing.
  - Granite LLM can understanding structured outputs like OpenAI function calling JSON scheme access.

It moves IoT control step.

![alt text](images/02-live-demonstration/02-live-demonstration-7.jpg)

- Node-RED
  - Node-RED call to simple MCP client.
- simple MCP client
  - Execute IoT MCP control server.
  - IoT MCP control server call IoT Light device with a "true" data state.
- IoT Light device
  - LED on!

