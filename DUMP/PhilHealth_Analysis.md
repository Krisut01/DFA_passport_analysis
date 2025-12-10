# PhilHealth Website Analysis & Redesign
## Modular Design Framework Implementation

**Project:** Accessibility Evaluation and High-Fidelity Redesign  
**System:** Philippine Health Insurance Corporation (PhilHealth) Official Website  
**Date:** 2024  
**Evaluation Method:** Analytic Evaluation (Heuristic + WCAG 2.1 Audit)  

**Deployed Redesigned Homepage:**  
- Accessible prototype (Vercel): [https://philhealth-red.vercel.app/](https://philhealth-red.vercel.app/)  

**Group Members:**  
- Jamilo, Francine Claire Asunto  
- Magatao, Darl Patrick Villajos  
- Matulac, Scott Lyndon Quilaton  
- Micarandayo, James

---

## Executive Summary

This document presents a comprehensive accessibility evaluation and modular redesign of the PhilHealth official website homepage. The analysis identifies critical accessibility barriers and usability issues, followed by a high-fidelity redesign that adheres to WCAG 2.x Level AA standards using a Modular Design Framework (MDF) approach. The redesign addresses all identified issues while establishing a scalable, reusable component system for future development.

---

## Part 1: Diagnostic Evaluation & Analysis

### System Context & Justification

#### System Overview

**System Name:** Philippine Health Insurance Corporation (PhilHealth) Official Website  
**URL:** https://www.philhealth.gov.ph/  
**System Type:** Public-facing government health insurance portal

#### Target User Group

The PhilHealth website serves a diverse user base including:
- **Primary Users:** Filipino citizens seeking health insurance information and services
- **Members:** Existing PhilHealth members managing accounts, payments, and benefits
- **Healthcare Providers:** Medical institutions and professionals accessing partnership information
- **Government Stakeholders:** Officials and administrators requiring policy and procedural documentation

#### System Purpose

The website functions as the primary digital interface for:
- Health insurance service information and enrollment
- Membership management and account administration
- Premium payment processing and transaction history
- Benefits inquiry and coverage verification
- Policy documentation and regulatory compliance information

#### Evaluation Purpose & Scope

**Primary Objectives:**
1. Conduct a rapid analytic evaluation of homepage accessibility and usability
2. Identify critical WCAG 2.x Level AA violations and usability barriers
3. Document specific accessibility issues with measurable criteria
4. Assess information architecture and user task completion pathways

**Scope Limitations:**
- Evaluation focused exclusively on the homepage as the primary entry point
- Analysis limited to visual and structural accessibility (not functional testing)

#### Context & Timing

**Evaluation Context:**
- Conducted in a time-constrained academic setting requiring rapid assessment
- Focus on immediate accessibility barriers affecting critical health insurance service access
- Priority given to issues impacting users with disabilities and assistive technology users

**Justification for User-Free (Analytic) Setting:**

The selection of an analytic evaluation approach is justified by the following factors:

1. **Time Efficiency:** Analytic methods provide rapid identification of technical violations without requiring user recruitment, scheduling, and testing sessions
2. **Objective Measurement:** WCAG 2.1 auditing provides quantifiable, standardized criteria for accessibility compliance
3. **Comprehensive Coverage:** Heuristic evaluation systematically examines usability patterns across multiple dimensions
4. **Reproducibility:** Analytic findings can be independently verified and validated
5. **Resource Constraints:** Academic project timeline precludes extensive user testing while maintaining evaluation rigor

### Settings & Methods

#### Evaluation Settings Comparison

**Controlled Setting:**
- **Advantages:** Controlled environment with repeatable conditions, detailed observation capabilities, systematic data collection
- **Disadvantages:** Artificial context may not reflect real-world usage patterns, limited ecological validity, requires extensive user recruitment and scheduling

**Natural Setting:**
- **Advantages:** Real-world context provides authentic user behavior, high ecological validity, genuine task performance scenarios
- **Disadvantages:** Unpredictable variables complicate analysis, difficult to control confounding factors, time-intensive data collection and analysis

#### Selected Evaluation Method

**Method:** Analytic Evaluation (Heuristic Evaluation + WCAG 2.1 Audit)

**Rationale for Selection:**

The analytic evaluation approach was selected based on the following criteria:

1. **Time Efficiency:** Enables rapid identification of critical issues without extensive user recruitment
2. **Objective Measurement:** Provides quantifiable, standardized criteria for accessibility compliance
3. **Comprehensive Coverage:** Systematically examines both usability patterns and technical accessibility violations
4. **Cost-Effectiveness:** Eliminates need for participant compensation and testing facilities
5. **Reproducibility:** Findings can be independently verified and validated

#### Combined Evaluation Approach

**Component 1: Heuristic Evaluation**
- **Methodology:** Application of Nielsen's 10 Usability Heuristics
- **Focus Areas:** Navigation patterns, information architecture, interaction design, visual hierarchy
- **Outcome:** Identification of usability barriers and design inconsistencies

**Component 2: WCAG 2.1 Level AA Audit**
- **Methodology:** Systematic review against WCAG 2.1 Level AA success criteria
- **Tools:** Automated accessibility testing tools combined with manual inspection
- **Focus Areas:** Color contrast, keyboard navigation, semantic structure, ARIA implementation
- **Outcome:** Documented violations with specific success criterion references

**Synthesis:** Combined approach ensures both user experience quality and technical accessibility compliance are addressed simultaneously.

### Accessibility & Usability Findings

#### Critical Issues Summary

The evaluation identified four critical problems that significantly impact user accessibility and usability. Two issues represent direct WCAG 2.1 violations, while two represent usability barriers that affect overall user experience.

#### Issue 1: Insufficient Color Contrast
**Category:** Accessibility Violation  
**WCAG Success Criterion:** 1.4.3 Contrast (Minimum) - Level AA  
**Severity:** High

**Problem Description:**
Multiple text elements throughout the homepage fail to meet the minimum 4.5:1 contrast ratio requirement for normal text (18pt or 14pt bold). This includes navigation links, body text, and informational content displayed over background colors.

**User Impact:**
- Low vision users and users with color vision deficiencies cannot read critical information
- Users in bright lighting conditions experience readability challenges
- Compliance failure prevents legal accessibility requirements from being met

**Affected Elements:**
- Navigation menu items
- Secondary text content
- Link text in various sections

---

#### Issue 2: Missing Focus Indicators
**Category:** Accessibility Violation  
**WCAG Success Criterion:** 2.4.7 Focus Visible - Level AA  
**Severity:** High

**Problem Description:**
Interactive elements including links, buttons, and form inputs lack visible focus states when navigated via keyboard. The default browser focus indicators are either removed via CSS or insufficiently visible.

**User Impact:**
- Keyboard-only users cannot determine their current navigation position
- Users with motor disabilities relying on keyboard navigation experience disorientation
- Tab navigation becomes ineffective without visual feedback

**Affected Elements:**
- All navigation links
- Interactive buttons
- Form input fields
- Service card interactive areas

---

#### Issue 3: Poor Information Hierarchy
**Category:** Usability Barrier  
**Severity:** Medium-High

**Problem Description:**
The homepage presents dense content without clear visual hierarchy, making it difficult for users to locate primary actions and services. Key services (registration, payment, benefits) are not prominently distinguished from secondary information.

**User Impact:**
- Users experience cognitive overload when scanning for specific services
- Primary call-to-action elements are not immediately identifiable
- Task completion time increases due to information search difficulty
- First-time users struggle to understand available services and their locations

**Affected Areas:**
- Service discovery and navigation
- Primary action identification
- Content prioritization and visual flow

---

#### Issue 4: Non-Semantic HTML Structure
**Category:** Accessibility Violation  
**WCAG Success Criterion:** 4.1.1 Parsing - Level A  
**Severity:** High

**Problem Description:**
The page structure lacks proper semantic HTML5 elements, ARIA landmarks, and heading hierarchy. Missing elements include proper `<nav>`, `<main>`, `<section>`, and `<article>` tags, as well as insufficient ARIA labels for interactive components.

**User Impact:**
- Screen reader users cannot efficiently navigate page structure
- Assistive technology users cannot identify page regions and landmarks
- Navigation efficiency is significantly reduced for users relying on semantic structure
- Screen reader announcements lack context and clarity

**Affected Elements:**
- Page structure and landmarks
- Navigation regions
- Content sections
- Interactive component labels

---

## Part 2: High-Fidelity Modular Strategy & Redesign

The redesign phase addresses all identified issues through a systematic Modular Design Framework (MDF) approach. This methodology ensures consistent, scalable, and accessible component development while maintaining design integrity across the system.

### Basic Unit & High-Fidelity Visual System

#### Core Object Identification

**Basic Unit:** Service Card Component

The Service Card Component serves as the foundational building block of the redesigned interface. This atomic component represents a single service or action within the PhilHealth ecosystem.

**Component Structure:**
- **Icon:** Visual identifier for the service type
- **Title:** Clear, descriptive heading (H3 level)
- **Description:** Concise explanation of service purpose and benefits
- **Action Button:** Primary call-to-action with accessible labeling

**Reusability Scope:**
- Homepage service grid
- Services listing page
- Member dashboard quick actions
- Mobile application interface
- Future feature implementations

#### High-Fidelity Core Visual System

The visual system establishes a comprehensive design language that ensures consistency, accessibility, and scalability across all components.  

**Proposed Color Palette (WCAG 2.x AA Compliant – Green Theme):**

The proposed color system is designed to align with a green PhilHealth-inspired theme **while ensuring WCAG 2.1 Level AA contrast**. The exact hex values are part of the redesign specification and serve as examples of accessible color choices.

| Color | Hex Code (Proposed) | Usage | Contrast Ratio (vs. white) | WCAG Compliance |
|-------|---------------------|-------|----------------------------|-----------------|
| Primary Green | #006600 | Primary actions, links, focus indicators | 7.2:1 | ✓ AA |
| Primary Green Light | #008844 | Secondary elements | 4.8:1 | ✓ AA |
| Primary Text | #1A1A1A | Body text, headings | 16.8:1 | ✓ AAA |
| Secondary Text | #4A4A4A | Supporting text, captions | 8.9:1 | ✓ AA |
| Background | #FFFFFF | Page and card backgrounds | N/A | N/A |
| Accent Green | #00AA44 | Icon backgrounds only | 3.8:1 | Icon only |
| Error Red | #CC0000 | Error messages, warnings | 5.7:1 | ✓ AA |
| Focus Outline | #006600 | Focus indicators | ≥ 3:1 | ✓ AA |

**Contrast Validation (Redesign):** In the proposed palette, all text colors exceed the minimum 4.5:1 ratio required for normal text, with primary text achieving AAA-level compliance (≥ 7:1).

**Typography System:**

The typography hierarchy establishes clear information architecture while ensuring readability across devices and user capabilities.

| Element | Size | Weight | Line Height | Use Case |
|---------|------|--------|-------------|----------|
| Heading 1 | 32px | Bold (700) | 1.2 | Page titles, hero headings |
| Heading 2 | 24px | Semi-bold (600) | 1.3 | Section headings |
| Heading 3 | 20px | Medium (500) | 1.4 | Card titles, subsection headings |
| Body Text | 16px | Regular (400) | 1.6 | Primary content, descriptions |
| Small Text | 14px | Regular (400) | 1.5 | Captions, metadata, footnotes |

**Font Family:** System font stack (Arial, Helvetica, sans-serif)
- **Rationale:** Ensures maximum compatibility and performance
- **Accessibility Benefit:** Familiar, readable typefaces with excellent screen rendering
- **Performance:** No external font loading required

**Style Definition:**

**Border Radius:**
- **Cards & Buttons:** 8px - Provides modern, approachable appearance
- **Input Fields:** 4px - Maintains form field clarity and readability

**Shadow System:**
- **Card Shadow:** `0 2px 8px rgba(0,0,0,0.1)` - Subtle elevation for content cards
- **Hover Shadow:** `0 4px 12px rgba(0,0,0,0.15)` - Enhanced elevation on interaction
- **Purpose:** Creates visual hierarchy and depth without overwhelming content

**Spacing System (8px Base Unit):**
- **8px:** Tight spacing for related elements
- **16px:** Standard spacing between elements
- **24px:** Section spacing
- **32px:** Major section separation
- **48px:** Page-level spacing
- **Rationale:** Consistent spacing creates visual rhythm and improves scanability

**Focus States:**
- **Style:** 2px solid outline in primary green (#006600)
- **Offset:** 2px from element edge
- **Purpose:** Clearly visible focus indicators meeting WCAG 2.4.7 requirements
- **Contrast:** 3:1 minimum ratio ensures visibility

### MDF Principles & Impact

#### Core Principles of Modular Design Framework

The Modular Design Framework (MDF) establishes a systematic approach to interface development that prioritizes reusability, consistency, and accessibility.

**Principle 1: Atomic Components**
- Complex interfaces are constructed from small, independent, reusable building blocks
- Each component serves a single, well-defined purpose
- Components can be combined to create more complex patterns

**Principle 2: Consistent Patterns**
- Standardized components ensure uniform behavior and appearance across the system
- Design patterns are documented and enforced through component libraries
- User experience remains predictable and learnable

**Principle 3: Scalable System**
- Components adapt to different contexts while maintaining design integrity
- Responsive behavior is built into component definitions
- System scales efficiently as features and complexity increase

**Principle 4: Accessibility by Default**
- Each component includes built-in WCAG 2.1 Level AA compliance
- Accessibility features are not optional additions but core requirements
- Testing and validation occur at the component level

#### Impact on Reusability

**Component Reuse Examples:**
- **Service Card Component:** Implemented across homepage service grid, services listing page, member portal dashboard, and mobile application
- **Button Component:** Maintains consistent focus states, contrast ratios, and keyboard navigation across all instances
- **Navigation Component:** Ensures consistent structure, ARIA landmarks, and interaction patterns throughout the application

**Benefits:**
- Reduced development time through component reuse
- Consistent user experience across all touchpoints
- Simplified maintenance through centralized component updates

#### Impact on Future Iterative Development

**Development Efficiency:**
- New features are built by composing existing components rather than creating from scratch
- Development velocity increases as component library expands
- Quality assurance focuses on component integration rather than individual element testing

**Maintenance Advantages:**
- Accessibility updates applied once at the component level propagate across all instances
- Design system ensures visual and functional consistency as development teams scale
- Modular testing allows isolated component validation, reducing regression risk

**Scalability:**
- System architecture supports growth without degradation of consistency or accessibility
- New team members can quickly understand and contribute through documented component patterns

#### Scalable Accessibility Architecture

**Component-Level Compliance:**
- Each component includes required ARIA attributes, keyboard support, and focus management
- Color contrast is validated at the component level, ensuring system-wide compliance
- Semantic HTML structure is enforced through component templates

**System-Wide Benefits:**
- Accessibility compliance is maintained automatically as new components are added
- Testing and validation processes are streamlined through component-level checks
- Accessibility improvements benefit the entire system when applied to shared components

### High-Fidelity Mockup & WCAG Rationale

The redesigned homepage implements five core modular components, each designed to address specific accessibility requirements while maintaining visual consistency and usability.

#### Component 1: Header Navigation Component

**Design Implementation:**
- Semantic `<nav>` element with descriptive ARIA label "Main Navigation"
- Sticky positioning for persistent access
- Responsive layout adapting to mobile viewports

**WCAG Compliance Rationale:**

| Success Criterion | Implementation | Compliance Level |
|-------------------|----------------|------------------|
| 2.4.7 Focus Visible | 2px solid green outline on focus, 2px offset | ✓ AA |
| 2.4.1 Bypass Blocks | Skip link to main content | ✓ A |
| 2.1.1 Keyboard | Full keyboard navigation support | ✓ A |
| 4.1.2 Name, Role, Value | Semantic nav element with ARIA label | ✓ A |

**Accessibility Features:**
- Keyboard-accessible Tab order navigation
- Visible focus indicators meeting 3:1 contrast ratio
- Skip link enables screen reader users to bypass navigation

---

#### Component 2: Service Card Component

**Design Implementation:**
- Grid-based layout with responsive columns
- Icon, title, description, and action button structure
- Hover and focus states with visual feedback

**WCAG Compliance Rationale:**

| Success Criterion | Implementation | Compliance Level |
|-------------------|----------------|------------------|
| 1.4.3 Contrast (Minimum) | 7.2:1 contrast for text on white | ✓ AA |
| 1.1.1 Non-text Content | Icons paired with descriptive text labels | ✓ A |
| 2.4.7 Focus Visible | Focus-within outline on card container | ✓ AA |
| 1.3.1 Info and Relationships | Proper heading hierarchy (H3 for titles) | ✓ A |

**Accessibility Features:**
- Text alternatives for all icons
- Keyboard navigation with Tab order
- Clear visual hierarchy through typography and spacing

---

#### Component 3: Primary Button Component

**Design Implementation:**
- Green background (#006600) with white text
- Minimum 44x44px touch target size
- Clear hover, focus, and active states

**WCAG Compliance Rationale:**

| Success Criterion | Implementation | Compliance Level |
|-------------------|----------------|------------------|
| 1.4.3 Contrast (Minimum) | 7.2:1 contrast ratio (green on white) | ✓ AA |
| 2.5.5 Target Size | 44x44px minimum touch target | ✓ AAA |
| 2.4.7 Focus Visible | 2px solid outline on focus | ✓ AA |
| 4.1.2 Name, Role, Value | Descriptive aria-label attributes | ✓ A |

**Accessibility Features:**
- Exceeds minimum touch target requirements
- Descriptive button text and ARIA labels
- Keyboard activation support

---

#### Component 4: Search Component

**Design Implementation:**
- Accessible form structure with visible and hidden labels
- Search input with submit button
- Error handling and validation support

**WCAG Compliance Rationale:**

| Success Criterion | Implementation | Compliance Level |
|-------------------|----------------|------------------|
| 3.3.2 Labels or Instructions | Visible label and aria-label | ✓ AA |
| 3.3.1 Error Identification | Error states announced to screen readers | ✓ AA |
| 2.1.1 Keyboard | Full keyboard accessibility | ✓ A |
| 2.4.7 Focus Visible | Clear focus indicators | ✓ AA |

**Accessibility Features:**
- Proper label association with input fields
- Keyboard-accessible search functionality
- Error messages accessible to screen readers

---

#### Component 5: Footer Component

**Design Implementation:**
- Semantic `<footer>` element with structured content
- Organized link groups with clear headings
- Contact information in accessible format

**WCAG Compliance Rationale:**

| Success Criterion | Implementation | Compliance Level |
|-------------------|----------------|------------------|
| 1.3.1 Info and Relationships | Semantic footer landmark | ✓ A |
| 2.4.4 Link Purpose | Descriptive link text | ✓ A |
| 2.4.7 Focus Visible | Focus indicators on all links | ✓ AA |

**Accessibility Features:**
- Semantic HTML5 footer element
- Descriptive link text for all navigation items
- Structured contact information

### Specialized Component Adaptation & Quality

#### Component Adaptation: Service Card → Smart Watch Interface

The Service Card component has been adapted for smartwatch interfaces, addressing the unique constraints and opportunities of wearable technology while maintaining accessibility standards.

**Adaptation Specifications:**

**Visual Simplification:**
- Reduced to icon + short label (maximum 8 characters)
- Removed descriptive text to accommodate limited screen real estate
- Maintained visual hierarchy through icon prominence

**Interaction Design:**
- Touch target increased to 60x60px (exceeding standard 44px minimum)
- Single tap interaction model for service activation
- Haptic feedback on selection for enhanced user confirmation

**Accessibility Enhancements:**
- High contrast mode: white icon on dark background (#000000) achieving 12:1 contrast ratio
- Enhanced visibility for outdoor use and low-light conditions
- Larger touch targets improve motor accessibility

#### Accessibility Trade-offs Analysis

**Trade-off 1: Reduced Text Content**

**Issue:** Descriptive text removed from service cards violates WCAG 1.1.1 (Non-text Content) requirement for text alternatives.

**Mitigation Strategy:**
- Voice announcement on selection provides full context and service description
- Screen reader support ensures complete information access
- Companion mobile app provides detailed information when needed

**Trade-off 2: Reduced Information Density**

**Issue:** Limited screen space prevents comprehensive information display.

**Mitigation Strategy:**
- Progressive disclosure: initial tap reveals service details
- Secondary interaction provides full description and options
- Companion device synchronization enables detailed information access

**Benefits Achieved:**

1. **Motor Accessibility:** Larger touch targets (60x60px) significantly improve usability for users with motor impairments or limited dexterity
2. **Visual Accessibility:** Enhanced contrast ratio (12:1) provides superior visibility for low vision users, particularly in bright outdoor conditions
3. **Cognitive Load Reduction:** Simplified interface reduces cognitive processing requirements
4. **Contextual Adaptation:** Interface adapts to environmental constraints while maintaining core functionality

**Compliance Status:**
- Primary violations mitigated through alternative access methods
- Core accessibility principles maintained through adaptive strategies
- User experience optimized for specialized interface constraints

---

## Conclusion

This analysis and redesign demonstrates a systematic approach to addressing accessibility barriers while establishing a scalable, maintainable design system. All four critical issues identified in the evaluation have been resolved through the implementation of WCAG 2.1 Level AA compliant components within a Modular Design Framework.

### Key Achievements

✅ **Accessibility Compliance:** All WCAG 2.1 Level AA violations have been addressed through systematic component design  
✅ **Usability Enhancement:** Information hierarchy improvements eliminate user confusion and reduce task completion time  
✅ **Scalable Architecture:** Modular component system established for efficient future development  
✅ **Quality Assurance:** Accessibility compliance maintained at component level ensures system-wide adherence  
✅ **Professional Design:** Cohesive visual design implemented with green theme maintaining brand identity

### Future Recommendations

1. **User Testing:** Conduct validation testing with individuals with disabilities to verify design decisions and identify additional improvements
2. **Component Expansion:** Expand component library based on additional page requirements and user feedback
3. **Automated Testing:** Implement automated accessibility testing in the development workflow to prevent regression
4. **Documentation:** Establish comprehensive design system documentation for team reference and onboarding
5. **Enhanced Compliance:** Consider AAA-level compliance for enhanced accessibility where feasible and beneficial

### Summary

The redesigned PhilHealth homepage successfully addresses all identified accessibility and usability issues while establishing a foundation for continued improvement. The Modular Design Framework approach ensures that accessibility remains a core consideration in all future development, creating a sustainable system that serves all users effectively.
