# Dhyana - EDM Continuous Music Generator
## Requirements Document

### Overview
Dhyana is a web-based EDM music generator that creates continuous, randomized electronic music using Tone.js. It features multiple drum patterns, synthesizer melodies, and real-time audio visualization.

### Functional Requirements

#### 1. Audio Engine
##### Implemented
- [x] Web Audio API initialization with user gesture
- [x] Dynamic loading of Tone.js library
- [x] Proper audio context state management
- [x] Sample-based drum machine with configurable samples
- [x] Synthesizer with pentatonic scale melodies
- [x] Real-time waveform visualization
- [x] Effects chain (filter, reverb)
- [x] Pattern randomization for drums and melodies
- [x] Settings persistence during playback

##### Planned
- [ ] Multiple simultaneous music generator instances
- [ ] Independent control of each generator instance
- [ ] Synchronization options between instances
- [ ] More synthesizer types and parameters
- [ ] Extended effects rack with more options
- [ ] Pattern memory and recall
- [ ] Pattern probability controls
- [ ] Tempo control and synchronization
- [ ] MIDI output support

#### 2. User Interface
##### Implemented
- [x] Play/Stop controls with visual feedback
- [x] Settings dialog with save/cancel functionality
- [x] Custom sample URL configuration
- [x] Sample URL validation
- [x] Real-time audio visualization
- [x] Logging system for user feedback
- [x] Responsive layout

##### Planned
- [ ] Retro-style 80s inspired control interface
  - [ ] Skeuomorphic knobs with realistic rotation
  - [ ] LED-style displays for values
  - [ ] Vintage slider designs
  - [ ] Realistic hover and active states
  - [ ] Fine/coarse value adjustment modes
  - [ ] Direct value input support
  - [ ] MIDI CC mapping for all controls
  - [ ] Mouse wheel support with modifier keys
  - [ ] Value acceleration based on input speed
  - [ ] Custom value scaling per control
  - [ ] Value snap points (optional per control)
  - [ ] Customizable value ranges and units
  - [ ] Focus states with keyboard control
  - [ ] Touch-optimized interaction modes
  - [ ] Control grouping and layouts
  - [ ] Preset morphing between values
  - [ ] Control value automation
- [ ] Adaptive grid layout for multiple generators
- [ ] Drag-and-drop interface for generator arrangement
- [ ] Visual pattern editor
- [ ] Pattern probability visualization
- [ ] Advanced waveform and spectrum analysis
- [ ] Preset management system
- [ ] MIDI mapping interface
- [ ] Touch-optimized controls for mobile
- [ ] Dark/Light theme support

#### 3. Control Interface
##### Technical Requirements
- Scalable Vector Graphics (SVG) for control elements
- CSS transforms for smooth animations
- WebGL for complex lighting effects
- Custom event handling for multi-touch
- MIDI input processing
- High-resolution value storage
- Efficient DOM updates
- Responsive layout system
- State management for all controls
- Undo/Redo support for value changes

##### Interaction Models
- Primary click and drag
- Scroll wheel with modifier keys
  - Default: Coarse adjustment
  - Shift: Fine adjustment
  - Ctrl/Cmd: Super-fine adjustment
- Double-click for default value
- Direct value entry
- Touch gestures
  - Single finger: Primary adjustment
  - Two fingers: Fine adjustment
  - Long press: Alternative functions
- MIDI CC mapping
  - Learn mode
  - Value scaling
  - Bidirectional sync

##### Visual Feedback
- Real-time value display
- Movement animation
- Hover state lighting
- Active state effects
- Focus indicators
- Value range indicators
- Current value marker
- Scale/tick marks
- Unit display
- Error state indication

#### 3. Sample Management
##### Implemented
- [x] Default sample set configuration
- [x] Custom sample URL support
- [x] Sample validation before use
- [x] Runtime sample switching

##### Planned
- [ ] Local sample file support
- [ ] Sample library management
- [ ] Sample preview functionality
- [ ] Sample editing capabilities
- [ ] Sample sharing between instances
- [ ] Cloud sample storage integration

### Technical Requirements

#### 1. Audio Processing
##### Current Implementation
- Web Audio API for low-level audio operations
- Tone.js for high-level audio synthesis and scheduling
- ScriptProcessorNode for waveform analysis
- Custom audio buffer management
- Real-time audio parameter modulation

##### Future Enhancements
- Upgrade to AudioWorklet for better performance
- Implement shared audio bus architecture
- Add audio routing matrix
- Implement advanced DSP algorithms
- Add support for VST-style plugins

#### 2. Performance
##### Current Implementation
- Asynchronous sample loading
- Efficient audio buffer management
- Request animation frame for visualization
- Event delegation for UI interactions

##### Future Optimizations
- Web Worker for heavy computations
- SharedArrayBuffer for audio data
- Optimized canvas rendering
- Lazy loading of inactive instances
- Memory pool for audio buffers

#### 3. Architecture
##### Current Structure
- Single HTML file application
- Modular JavaScript organization
- Event-driven UI updates
- State management for settings

##### Planned Improvements
- Module bundling system
- Component-based architecture
- State management library integration
- Service worker for offline support
- WebAssembly for critical paths

#### 4. Browser Compatibility
##### Current Support
- Modern browsers (Chrome, Firefox, Safari)
- Web Audio API support required
- ES6+ JavaScript features

##### Future Requirements
- Legacy browser fallbacks
- Progressive enhancement
- Mobile browser optimizations
- Reduced dependency requirements

### Development Guidelines

#### 1. Code Organization
- Maintain clear section comments in HTML
- Use consistent naming conventions
- Document all audio-related functions
- Maintain separation of concerns
- Use TypeScript for type safety

#### 2. Testing
- Unit tests for core functionality
- Integration tests for audio pipeline
- Browser compatibility testing
- Performance benchmarking
- Audio quality assurance

#### 3. Documentation
- Inline code documentation
- API documentation
- User guide
- Development setup guide
- Contributing guidelines

### Project Milestones

1. **Phase 1: Core Functionality** (Completed)
   - Basic audio engine
   - Single instance implementation
   - Essential UI controls
   - Sample management

2. **Phase 2: Multi-Instance Support** (In Progress)
   - Instance management system
   - Grid layout implementation
   - Instance synchronization
   - Resource sharing

3. **Phase 3: Retro UI Implementation** (Planned)
   - SVG-based control elements
   - Knob component development
   - Slider component development
   - LED display component
   - Input handling system
   - MIDI integration
   - Value management system
   - Visual feedback system
   - Touch optimization
   - Control presets
   - Automation framework

4. **Phase 4: Advanced Features** (Planned)
   - Extended synthesis capabilities
   - Advanced effects processing
   - Pattern editing and storage
   - Preset system

5. **Phase 5: Performance & Polish** (Planned)
   - Optimization passes
   - Mobile support
   - Offline capabilities
   - User experience improvements

### Notes
- All audio processing must maintain low latency
- UI should remain responsive during audio processing
- Sample management should be efficient and reliable
- Multiple instances should not degrade performance
- Mobile support should not compromise functionality
- Control interactions must feel precise and professional
- Visual feedback should be immediate and smooth
- MIDI integration should support high-resolution values
- Touch interface should not compromise desktop experience
