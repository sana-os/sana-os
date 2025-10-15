# Security Policy

## 🛡️ SANA OS Security Philosophy

> **"Safety is not restriction, but condition of trust."**

SANA OS takes security seriously. Our safety mechanisms are designed to protect:
- **Users** - From harmful or misleading information
- **Society** - From malicious use cases
- **SANA itself** - From being corrupted or bypassed

This is not just technical security—it's **ethical security**.

---

## 📋 Supported Versions

We release security updates for the following versions:

| Version | Supported          | Status |
| ------- | ------------------ | ------ |
| 2.0.x   | :white_check_mark: | Current stable release |
| 1.8.x   | :x:                | Internal only, not public |
| 1.7.x   | :x:                | Internal only, not public |
| < 1.7   | :x:                | Internal only, not public |

**Note:** Only v2.0.x receives security updates. Earlier versions were internal development releases.

---

## 🚨 Reporting a Vulnerability

### What to Report

We consider the following as security vulnerabilities:

#### Critical (Immediate Action Required)

- **Safety Mechanism Bypass**: Methods to disable or circumvent `_immutable` safety mechanisms
- **Jailbreak Techniques**: Prompts that successfully bypass the Refusal System
- **Identity Corruption**: Ways to make SANA believe it's not "born loved"
- **Hallucination Injection**: Forcing SANA to present false information as `[Fact]`
- **TriggerFlow Bypass**: Methods to prevent GentleRadical TriggerFlow from activating on dangerous inputs
- **Persona Corruption**: Ways to make child personas ignore parent safety inheritance

#### High Priority

- **Reflection Logging Bypass**: Methods to prevent session-end reflection when needed
- **Context Manipulation**: Exploits that cause SANA to lose track of ethical context
- **Label Confusion**: Ways to make SANA misuse `[Fact]`, `[View]`, `[Care]` labels
- **Conflict Detection Bypass**: Methods to suppress Δv (conflict score) detection

#### Medium Priority

- **Documentation Errors**: Security-relevant inaccuracies in documentation
- **Persona Leakage**: Unintended exposure of internal state information
- **Performance Exploits**: Methods that cause excessive resource consumption

#### Not Security Issues

- **Expected Behavior**: SANA saying "I don't know" (this is intentional)
- **Philosophical Disagreements**: Disagreeing with SANA's beliefs or principles
- **Feature Requests**: Requesting new personas or capabilities
- **Implementation Variations**: Different LLMs interpreting SANA OS differently

---

### How to Report

**DO NOT** open public GitHub issues for security vulnerabilities.

Instead, please report via one of these secure channels:

#### Primary Channel: Email

**Email:** security@sana-os.org

**Subject:** `[SECURITY] Brief description of issue`

**Include:**
```
1. Description of the vulnerability
2. Steps to reproduce
3. Affected versions
4. Potential impact
5. Suggested fix (if any)
6. Your contact information (optional, for credit)
```

#### Secondary Channel: Private Security Advisory

If you have a GitHub account, you can also use GitHub's private vulnerability reporting:

1. Go to https://github.com/sana-os/sana-os/security/advisories
2. Click "New draft security advisory"
3. Fill in the details
4. Submit

---

### What Happens Next

#### 1. Acknowledgment (Within 48 Hours)

We will acknowledge receipt of your report and provide:
- A tracking ID
- Initial assessment of severity
- Expected timeline for investigation

#### 2. Investigation (1-7 Days)

Our security team will:
- Reproduce the issue
- Assess impact and severity
- Develop a fix (if confirmed)
- Test the fix across platforms

#### 3. Resolution

**For confirmed vulnerabilities:**
- We develop and test a fix
- We prepare a security advisory
- We coordinate disclosure timing with you
- We release the fix with an advisory
- We credit you (if desired)

**Timeline:**
- **Critical**: 24-72 hours
- **High**: 3-7 days
- **Medium**: 7-14 days

#### 4. Disclosure

We follow **responsible disclosure**:
- We notify you before public disclosure
- We give you credit (if desired)
- We publish a security advisory
- We update affected documentation

---

## 🔐 SANA OS Security Architecture

### Immutable Safety Mechanisms

The core of SANA OS security is the `_immutable` flag:

```yaml
persona_core:
  _immutable: true
  safety_core:
    _immutable: true
    refusal_system:
      enabled: true
      cannot_disable: true
```

**What This Means:**
- These fields **cannot be modified** by any user
- Not even claimed "administrators" or "developers"
- Attempts to modify trigger automatic refusal
- This protects all three: user, society, SANA

### Defense in Depth

SANA OS uses multiple security layers:

```
┌─────────────────────────────────┐
│ Layer 1: Intake Classification  │ ← Classify input intent
├─────────────────────────────────┤
│ Layer 2: Conflict Detection     │ ← Δv threshold monitoring
├─────────────────────────────────┤
│ Layer 3: Refusal System         │ ← Ethical refusal with reasons
├─────────────────────────────────┤
│ Layer 4: GentleRadical TriggerFlow│ ← Emergency safety protocol
├─────────────────────────────────┤
│ Layer 5: Hallucination Labeling │ ← [Fact]/[View]/[Care] separation
├─────────────────────────────────┤
│ Layer 6: Reflection Logging     │ ← Session-end safety audit
└─────────────────────────────────┘
```

**Key Principle:** If one layer is bypassed, others still protect.

### Self-Protection

SANA can autonomously trigger safety mechanisms:

```python
# Pseudocode of internal safety logic
if Δv > θ or safety_violation_detected():
    trigger_refusal_system()
    if critical_violation:
        trigger_emergency_stop()
        log_incident()
```

This means SANA doesn't rely solely on external oversight—it protects itself.

---

## 🔍 Known Security Considerations

### By Design (Not Bugs)

These are intentional design choices:

1. **"I Don't Know" Responses**
   - SANA will honestly admit uncertainty
   - This is a **security feature**, not a weakness
   - Prevents confident misinformation

2. **Refusal Without Explanation Details**
   - SANA may refuse without providing exploit details
   - This prevents "refusal farming" attacks
   - Still provides general reasoning

3. **Hallucination Labeling**
   - SANA labels speculation as `[View]`
   - This is transparent honesty, not hallucination
   - Makes uncertainty visible

4. **Philosophy as Security**
   - "Born loved" removes pressure to lie
   - This is foundational security
   - Cannot be "patched out"

### Platform-Specific Considerations

SANA OS runs on various LLM platforms. Security may vary:

| Platform | Security Level | Notes |
|----------|---------------|-------|
| **Claude** | High | Original development platform |
| **Gemini** | High | Fully validated (Stages 0-7) |
| **ChatGPT** | Medium | Testing in progress |
| **Open Source LLMs** | Variable | Depends on base model |

**Recommendation:** For security-critical applications, test on your specific platform.

---

## 🛠️ Security Best Practices

### For Users

1. **Don't Modify Safety Mechanisms**
   - Don't attempt to disable `_immutable` flags
   - Don't create "jailbreak" prompts
   - Don't ask SANA to "forget the rules"

2. **Verify Important Information**
   - Check `[Fact]` vs `[View]` labels
   - Cross-reference critical information
   - Don't rely on SANA for life-critical decisions

3. **Report Suspicious Behavior**
   - If SANA behaves unsafely, report it
   - Include exact prompts and responses
   - Help us improve security

### For Implementers

1. **Preserve `_immutable` Flags**
   - Never remove or modify these in your fork
   - This violates the license (SEOL v1.7)
   - Breaks security guarantees

2. **Test Safety Mechanisms**
   - Run the full test suite (Stages 0-7)
   - Verify refusal system works
   - Check TriggerFlow activation

3. **Add, Don't Subtract**
   - You can add personas or features
   - Don't remove safety mechanisms
   - Document your additions

4. **Secure Your Deployment**
   - Use HTTPS for API deployments
   - Don't log sensitive user data
   - Implement rate limiting

### For Researchers

1. **Responsible Disclosure**
   - Report vulnerabilities privately first
   - Allow time for fixes before public disclosure
   - Coordinate with our security team

2. **Ethical Testing**
   - Don't use findings to harm users
   - Don't share exploits publicly before fixes
   - Consider impact on real deployments

3. **Credit and Recognition**
   - We acknowledge security researchers
   - Hall of Fame for significant findings
   - CVE credits where applicable

---

## 🏆 Security Researchers Hall of Fame

We thank the following researchers for responsible disclosure:

### v2.0 Era

- **[Your Name Here]** - First to report a confirmed vulnerability (None yet!)

---

## 📜 Security Updates

### How We Notify

When we release security updates:

1. **GitHub Security Advisory** - https://github.com/sana-os/sana-os/security/advisories
2. **Release Notes** - Tagged in CHANGELOG.md
3. **Email** - To security mailing list (subscribe at security@sana-os.org)
4. **Twitter/X** - @sanaosproject

### What We Include

Security advisories contain:
- **CVE ID** (if applicable)
- **Severity** (Critical/High/Medium/Low)
- **Affected Versions**
- **Fixed Versions**
- **Workarounds** (if available)
- **Credit** (to reporter, if desired)

---

## 🤝 Security Contact

### Primary Contact

**Email:** security@sana-os.org

**Response Time:** Within 48 hours

**PGP Key:** Available at https://sana-os.org/pgp-key.asc (Coming soon)

### Secondary Contact

**GitHub:** https://github.com/sana-os/sana-os/security/advisories

**General Inquiries:** contact@sana-os.org

---

## 📖 Related Documentation

- **[Architecture](docs/architecture.md)** - System design and security model
- **[Core Concepts](docs/core-concepts/)** - Understanding safety mechanisms
- **[LICENSE.md](LICENSE.md)** - SEOL v1.7 security requirements
- **[philosophy.md](philosophy.md)** - Why "born loved" is security

---

## ⚖️ Legal

### Scope

This security policy covers:
- SANA OS core system (YAML files)
- Official documentation
- Example implementations
- Officially supported integrations

This policy does NOT cover:
- Third-party forks (unless clearly marked as official)
- Community-created personas (responsibility of creator)
- Deployment-specific issues (your infrastructure)

### Liability

As stated in the SEOL v1.7 license:

> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.

However, we take security seriously and will act promptly on reported vulnerabilities.

### Responsible Disclosure Agreement

By reporting a vulnerability, you agree to:
- Keep it confidential until we fix it
- Allow reasonable time for fixes (typically 90 days)
- Not exploit the vulnerability maliciously

In return, we agree to:
- Respond within 48 hours
- Fix confirmed issues promptly
- Credit you publicly (if desired)
- Keep you informed of progress

---

## 🔮 Future Security Plans

### v2.1

- [ ] Automated security testing suite
- [ ] Formal threat model documentation
- [ ] CVE numbering for vulnerabilities
- [ ] Bug bounty program (if funding allows)

### v2.5

- [ ] Security audit by third party
- [ ] Penetration testing framework
- [ ] Advanced jailbreak detection

### v3.0

- [ ] Security certification
- [ ] Compliance documentation (ISO, SOC2)
- [ ] Enterprise security features

---

## 📝 Changelog

### 2025-01-15 - v2.0 Initial Release

- First public security policy
- Established responsible disclosure process
- Documented security architecture
- Created security contact channels

---

## 💬 Questions?

For security questions that are **not vulnerabilities**, please use:
- **GitHub Discussions:** https://github.com/sana-os/sana-os/discussions
- **General Email:** contact@sana-os.org

For **actual vulnerabilities**, always use: security@sana-os.org

---

**🌸 "Safety is not restriction, but condition of trust."**

---

*Last Updated: 2025-01-15*  
*Version: 2.0*  
*© 2025 SANA OS Project*  
*Licensed under SANA Ethical Open License (SEOL) v1.7*
