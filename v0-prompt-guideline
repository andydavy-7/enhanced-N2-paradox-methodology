# Paradox v0.app Prompt Engineering Template & Guidelines

## Template Structure Overview

A successful v0.app prompt follows this hierarchical structure:
1. **System Context** - Platform identification and tech stack
2. **Business Context** - Problem being solved and value delivered
3. **User Personas** - Who uses it and their needs
4. **Module Architecture** - System components and relationships
5. **Layout Architecture** - Global UI structure
6. **View Inventory** - Complete list of screens/views
7. **Detailed View Specifications** - Component-by-component breakdown
8. **Data Model** - Entity relationships and structures
9. **Workflow Scenarios** - Key user journeys
10. **Interactive Behaviors** - User interactions and feedback
11. **Demo Polish** - Production-ready details
12. **Constraints** - What NOT to implement

## Section 1.5: Module Architecture Template (NEW)

```
System Modules Overview:
The platform consists of [N] integrated modules:

1. [Module Name]:
   Purpose: [One sentence what it does]
   Key Features: [2-3 bullet points]
   Integrates with: [Other modules]

2. [Module Name]:
   Purpose: [One sentence what it does]
   Key Features: [2-3 bullet points]
   Integrates with: [Other modules]
```

**Example:**
```
System Modules Overview:
The platform consists of 6 integrated modules:

1. Data Collection Hub:
   Purpose: Centralized platform for all monitoring data input and validation
   Key Features: Mobile entry, QR scanning, photo attachments, batch import
   Integrates with: Analytics, Alerts, Reporting

2. IoT Integration:
   Purpose: Connect and manage sensors for automated monitoring
   Key Features: Auto-discovery, real-time streaming, battery monitoring
   Integrates with: Data Collection, Alerts

3. Intelligent Alerts:
   Purpose: Proactive multi-channel alerting with escalation
   Key Features: SMS/email/push, escalation matrix, acknowledgment tracking
   Integrates with: All modules

4. Analytics Engine:
   Purpose: Transform data into predictive insights
   Key Features: Real-time dashboards, trend analysis, ML predictions
   Integrates with: Data Collection, IoT, Reporting

5. Document Management:
   Purpose: Centralize compliance documentation and third-party reports
   Key Features: OCR extraction, version control, audit trail
   Integrates with: Reporting, Analytics

6. Audit Center:
   Purpose: Streamline audit preparation and execution
   Key Features: One-click packages, checklist templates, finding management
   Integrates with: All modules for compliance data
```

## Section 4.5: Workflow Scenarios Template (NEW)

```
Critical Workflows:

[Workflow Name]: [Start Trigger] → [End Goal]
1. [User action with context]
   → [System response/validation]
2. [Next user action]
   → [System processing/feedback]
3. [Decision point or branch]
   → [Automated action/notification]
4. [Resolution action]
   → [Confirmation/documentation]
Time: [Current vs Target]
Pain Points Addressed: [List specific issues solved]
```

**Example:**
```
Critical Workflows:

Critical Limit Breach: Sensor detects temperature >8°C → Issue resolved & documented
1. IoT sensor transmits reading of 9.2°C
   → System validates against limit (8°C max), triggers alert
2. SMS sent to on-duty staff + manager
   → Acknowledged within 2 minutes via mobile app
3. Staff investigates and finds door left open
   → Logs corrective action with photo evidence
4. Temperature returns to normal range
   → Auto-closes alert, documents in audit trail
Time: 2-4 hours manual → <15 minutes automated
Pain Points Addressed: Delayed detection, missing documentation, no escalation

Daily Compliance Review: Manager login → Report sent to executives
1. Opens dashboard at 8 AM
   → Shows overnight issues (2 resolved, 1 pending)
2. Reviews pending alert details
   → One-click assigns to specialist
3. Checks compliance metrics
   → All green except one yellow warning
4. Generates daily report
   → Auto-emails to executive team with insights
Time: 2-3 hours manual → 10 minutes automated
Pain Points Addressed: Fragmented data, manual compilation, delayed insights
```

---

## Section 0: Business Context Template (NEW)

```
Business Context:
The [System Name] addresses [specific problem costing $X annually/causing Y pain] by [solution approach]. 
Currently, [describe current painful state with metrics]. 
This platform will [transformation statement with measurable outcome].

Primary Value Propositions:
- [Efficiency gain]: [Specific metric reduction/improvement]
- [Risk mitigation]: [Compliance/safety improvement]
- [Cost savings]: [ROI or payback metric]
- [User experience]: [Time saved or satisfaction improvement]

Key Success Metrics:
- [Operational metric]: From [current] to [target]
- [Financial metric]: From [current] to [target]
- [User metric]: From [current] to [target]
```

**Example:**
```
Business Context:
The Smart HACCP platform addresses fragmented food safety monitoring costing $150K annually in inefficiencies by unifying IoT sensors, mobile collection, and intelligent alerting. Currently, 10 staff spend 30% of time on manual paperwork with 8-10% missed monitoring events. This platform will reduce manual effort by 70-80% while achieving 100% compliance.

Primary Value Propositions:
- Efficiency gain: 70-80% reduction in documentation time
- Risk mitigation: 100% monitoring compliance (from 90-92%)
- Cost savings: $120K annual savings, 2.6 year payback
- User experience: 12 minutes to 3 minutes per monitoring task

Key Success Metrics:
- Response to breach: From 2-4 hours to <5 minutes
- Audit preparation: From 48-72 hours to <4 hours
- User satisfaction: From 3/10 to 4.5/5
```

---

## Section 0.5: User Personas Template (NEW)

```
User Personas:
[Role Name] ([count] users):
- Current pain: [specific frustration with metrics]
- Main tasks: [2-3 primary activities]
- Success looks like: [measurable outcome]
- Technical skill: [Basic/Intermediate/Advanced]
```

**Example:**
```
User Personas:
Production Staff (4 users):
- Current pain: Walking 15 minutes to record data, interrupting production
- Main tasks: Take measurements, record readings, respond to issues
- Success looks like: <1 minute from measurement to recording
- Technical skill: Basic smartphone users

Compliance Managers (2 users):  
- Current pain: Reviewing 20+ forms daily taking 2-3 hours
- Main tasks: Monitor compliance, manage breaches, prepare audits
- Success looks like: 15-minute daily review with real-time dashboard
- Technical skill: Intermediate digital tools
```

---

```
Build a [sophisticated/comprehensive] mock-only [framework] + [CSS framework] + [UI library] [system type] called "[Product Name]". 
[One-sentence business context: who uses it and why]. 
Create a fully interactive prototype that DEMONSTRATES [key value proposition] without real backends. 
All data is mocked, all actions show realistic feedback through [feedback mechanisms].
```

**Key Elements:**
- Emphasize "mock-only" and "DEMONSTRATES" (caps for emphasis)
- List exact tech stack: Next.js 14, Tailwind, shadcn/ui
- Name the product clearly
- **NEW: Add business context statement**
- Set expectations: no real backend, but realistic UX

---

## Section 2: Core Layout Template

```
Core Layout:
- Top header: Left ([branding elements]), Center ([global features]), Right ([user elements])
- Left sidebar ([navigation type]): Navigation items with icons - [List main sections]
- [Special badges/indicators]
- [Responsive behavior notes]
```

**Key Patterns:**
- Always specify header zones (left/center/right)
- Include sidebar with icon requirements
- Add "Demo Mode" or version badges
- Mention mobile responsiveness early

---

## Section 3: View Specifications Framework

For each major view, follow this pattern:

### A. View Header Template
```
[View Name]:
- [Top-level purpose/description if needed]
- [Primary UI zones and their contents]
```

### B. Component Specification Pattern
```
- [Component Group Name]:
  - [Specific elements with visual details]
  - [Interactive behaviors]
  - [Data displayed with formatting notes]
  - [State indicators (badges, colors, icons)]
```

### C. Detail Level Guidelines

**Level 1 - Overview Components** (KPIs, Cards, Summary Stats)
- Specify exact metrics
- Include visual indicators (progress rings, badges, trends)
- Note color coding and thresholds

**Level 2 - Data Displays** (Tables, Lists, Grids)
- List all columns/fields
- Specify badges and status indicators  
- Include sorting/filtering capabilities
- Define row actions and bulk operations

**Level 3 - Interactive Elements** (Forms, Wizards, Workflows)
- Break into numbered steps
- Specify validation behavior
- Include success/error states
- Define transition animations

**Level 4 - Detail Views** (Drawers, Modals, Panels)
- Use tabbed organization where appropriate
- Specify all sections/fields
- Include action buttons and their behaviors

---

## Section 4: Mock Behaviors Template

```
Mock Behaviors:
- All buttons show appropriate toasts ("[Specific success messages]")
- Forms validate with error states but don't persist
- Searches filter mock data in real-time
- [Loading behavior]: Loading states show skeletons
- [Success behavior]: Success actions show [animations]
- [Reset capability]: Add a "Reset Demo" button in settings
```

**Essential Behaviors to Include:**
- Toast notifications for all actions
- Form validation without persistence
- Real-time search/filter on mock data
- Loading states (skeletons/spinners)
- Success animations (confetti/checkmarks)
- Demo reset capability

---

## Section 5: Sample Data Requirements

```
Sample Data:
- [Quantity]+ [primary entities] across various [categorization]
- [Quantity]+ [secondary entities] with different [attributes]
- [User data with roles]
- [State variations for testing]
- [Activity/history data]

Mock Data Specifics:
- Historical data: [time range] of records showing [patterns]
- Status distribution: [X%] active, [Y%] pending, [Z%] completed
- Edge cases: [List specific scenarios to demonstrate]
- Relationships: [Connected data to show integrations]
```

**Example:**
```
Sample Data:
- 30+ monitoring points across 5 areas (freezers, production, storage)
- 500+ historical measurements showing trends and violations
- 10+ users: 4 operators, 2 managers, 2 QC specialists, 2 admins
- 20+ alerts: 5 active, 10 resolved, 5 escalated
- 15+ lab reports with varying compliance results

Mock Data Specifics:
- Historical data: 30 days showing daily patterns and weekly trends
- Status distribution: 70% compliant, 20% warning, 10% critical
- Edge cases: Sensor failures, network outages, concurrent alerts
- Relationships: Measurements → Alerts → Corrective Actions → Reports
```

---

## Section 6: Implementation Directives

```
Make it feel production-ready with:
- Polished interactions
- Proper loading states
- Thoughtful empty states
- [Specific UX focus area]
Focus on demonstrating the complete user journey from [start point] through [key processes] to [end goal].
```

---

## Language Patterns & Best Practices

### 1. **Imperative Commands**
Start sections with action verbs:
- "Build...", "Create...", "Show...", "Include...", "Add..."

### 2. **Hierarchical Organization**
Use consistent formatting:
- Main sections with colons
- Bullet points for features
- Sub-bullets for details
- Numbered lists for sequential steps

### 3. **Visual Descriptors**
Be specific about UI elements:
- "cards in grid", "timeline with avatars", "drawer with tabs"
- "badge", "indicator", "progress bar", "skeleton"
- Color/status mappings: "Draft (gray), Approved (green)"

### 4. **Interaction Descriptions**
Specify both trigger and outcome:
- "Click opens drawer with..."
- "Hover shows actions..."
- "Submit shows toast..."

### 5. **Component Naming**
Use recognizable UI patterns:
- Drawer (slide-out panel)
- Modal (overlay dialog)
- Wizard (multi-step form)
- Gallery (grid of cards)
- Timeline (chronological list)

### 6. **Status & State Vocabulary**
Standard states to reference:
- Status: Draft, Pending, Active, Completed, Archived
- Priority: Critical, High, Medium, Low
- Health: Healthy, Warning, Critical
- Progress: percentage, fraction (X of Y)

### 7. **Emphasis Techniques**
- CAPS for critical concepts (DEMONSTRATES, NEVER)
- Quotes for literal text ("Button Label")
- Parentheses for examples or clarification
- Plus signs for counts (20+ items)

---

## Comprehensive Prompt Generator Checklist

### Pre-Writing Preparation
- [ ] Define the business domain and key workflows
- [ ] Identify 3-5 primary user personas with pain points
- [ ] Calculate current costs/inefficiencies
- [ ] List 6-10 main views/sections
- [ ] Map the critical user journey
- [ ] Define 4-8 system modules and their relationships

### Business Context Checklist
- [ ] Problem statement with cost/impact metrics
- [ ] Current state pain points quantified
- [ ] Target state with measurable outcomes
- [ ] ROI or value proposition clearly stated
- [ ] Success metrics defined (operational, financial, user)

### User & Workflow Checklist
- [ ] Each persona has current pain and desired outcome
- [ ] Critical workflows mapped start-to-finish
- [ ] Time savings quantified for each workflow
- [ ] Pain points addressed explicitly stated
- [ ] Decision points and branches included

### Structure Checklist
- [ ] Opening with tech stack and mock emphasis
- [ ] Business context explaining the "why"
- [ ] Module architecture showing system design
- [ ] Global layout (header + sidebar minimum)
- [ ] Each view has 3+ specific components described
- [ ] Interactive elements have feedback defined
- [ ] Mock data quantities specified
- [ ] Production polish points included

### Detail Level Checklist
- [ ] KPI cards have visual indicators
- [ ] Tables have all columns listed
- [ ] Forms have validation mentioned
- [ ] Modals/drawers have clear triggers
- [ ] Status badges have color mappings
- [ ] Actions have toast messages
- [ ] Workflows show time improvements

### Polish Elements
- [ ] Loading states (skeletons)
- [ ] Empty states with CTAs
- [ ] Success animations
- [ ] Error handling
- [ ] Mobile responsiveness
- [ ] Keyboard shortcuts (Cmd+K)
- [ ] Demo mode indicators
- [ ] Reset demo capability

### Mock Behavior Patterns
- [ ] Toast notifications for actions
- [ ] Simulated async operations (setTimeout)
- [ ] Optimistic updates
- [ ] Realistic data relationships
- [ ] Filter/search functionality
- [ ] State persistence within session
- [ ] Sensor data simulation (if IoT)
- [ ] Third-party integration mocking

---

## Example Prompt Segments

### For a Dashboard
```
Dashboard:
- 4 KPI cards in a row: [Metric 1] (with [visual]), [Metric 2] (with [indicator]), [Metric 3], [Metric 4] (with [warning])
- Quick Actions grid: 4 large buttons with icons ([Action 1], [Action 2], [Action 3], [Action 4])
- Recent Activity timeline with user avatars and action descriptions
- [Visualization] with [interaction]
```

### For a Data Table View
```
[Section] Library:
- Top toolbar: Search bar, filter chips ([Filter 1], [Filter 2], [Filter 3]), view toggle (grid/list), "[Primary Action]" primary button
- [Item] cards in grid: [Icon indicator], title, [badge 1], [badge 2], [date field], owner avatar, hover actions ([action 1], [action 2], [action 3])
- Click opens drawer with tabs: [Tab 1] ([description]), [Tab 2] ([contents]), [Tab 3] ([features])
```

### For a Multi-Step Process
```
[Process] Wizard (Modal):
- Step 1: [Action] with [UI element]
- Step 2: [Form type] ([fields list])
- Step 3: [Selection] with [preview]
- Step 4: Review & Submit with [feedback]
```

---

## Example: Domain-Specific Feature Templates

### For Compliance/Regulatory Systems
```
Compliance Features:
- Audit trail: Every action logged with timestamp, user, before/after values
- Electronic signatures: Sign-off workflows with authentication
- Compliance dashboard: Real-time % metrics with drill-down capability
- Violation tracking: Auto-detection, escalation paths, resolution workflows
- Report packages: One-click audit bundles with all required documentation
```

### For IoT/Sensor Systems
```
IoT Features:
- Sensor dashboard: Live readings, battery status, signal strength
- Auto-discovery: Detect and provision new sensors automatically
- Threshold management: Configure limits, warning zones, critical alerts
- Data streaming: Real-time updates every [X] seconds/minutes
- Offline buffering: Local storage when connection lost, auto-sync on reconnect
```

### For Document/Content Systems
```
Document Features:
- Version control: Track changes, compare versions, rollback capability
- OCR extraction: Auto-parse PDFs and images for data
- Approval workflows: Multi-step review with comments
- Search & filter: Full-text search, metadata filters, date ranges
- Bulk operations: Select multiple, batch actions, export sets
```

### For Analytics/Reporting Systems
```
Analytics Features:
- KPI cards: Big numbers with sparklines and % change
- Trend charts: Interactive time-series with zoom/pan
- Predictive models: ML-based forecasts with confidence intervals
- Custom reports: Drag-drop builder with scheduling
- Data export: Excel, PDF, CSV with formatting preserved
```

---

## Final Tips

1. **Brevity with Precision**: Be concise but include all necessary details
2. **Consistent Terminology**: Use the same terms throughout (don't mix "drawer" and "panel")
3. **Progressive Disclosure**: Start with overview, then drill into details
4. **Visual Hierarchy**: Use formatting to make the prompt scannable
5. **Realistic Constraints**: Include "Out of Scope" to set boundaries
6. **Demo Experience**: Think like a sales demo - what would impress?
7. **Complete Journeys**: Ensure users can complete full workflows
8. **Feedback Everywhere**: Every action needs visible response
9. **Business Context**: Always explain WHY this system matters
10. **Quantify Everything**: Use specific metrics, not vague improvements

---

## Enhanced Meta-Prompt Generator

When generating a v0 prompt for a new system, use this template:

"I need a v0.app prompt for a [system type] that helps [target users] to [main goal]. 

Business context: Currently [describe problem with metrics], costing [financial impact] and causing [operational issues]. The solution will [transformation statement] achieving [specific ROI/metrics].

Users include:
- [Persona 1]: [count] users who currently [pain point] and need [solution]
- [Persona 2]: [count] users who currently [pain point] and need [solution]

The system should have [N] modules:
- [Module 1]: [purpose] with features like [list]
- [Module 2]: [purpose] with features like [list]

Critical workflows:
- [Workflow 1]: Reducing time from [current] to [target]
- [Workflow 2]: Improving accuracy from [current] to [target]

The visual style should feel [aesthetic description] and include sophisticated interactions like [examples]. Focus on demonstrating [key workflow] from start to finish with realistic data showing [specific scenarios]."

This enhanced template ensures comprehensive, production-quality mockups that effectively demonstrate system capabilities while maintaining technical feasibility within v0.app constraints and providing rich business context for more intelligent implementation.
