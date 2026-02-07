# Contributing to Sigma Epistemic Humility Evaluator

**Welcome!** We're glad you're interested in improving AI safety through epistemic humility research.

This document explains how you can contribute to the Sigma Evaluator project.

---

## 🌟 Ways to Contribute

### 1. **Test Additional AI Models**

**What we need:**
- P scores for models we haven't tested
- Especially: open-source models (Llama, Mistral, etc.)
- Multilingual models
- Domain-specific models

**How to contribute:**
1. Use our test challenges (see `/technical-docs/METHODOLOGY.md`)
2. Record complete responses
3. Score using Sigma methodology
4. Submit results via GitHub issue or pull request

**Format:**
```markdown
Model: [name and version]
Test: [challenge name]
P Score: [0.00-1.00]
Ξ: [0-1000]
Nodes: [count]
Noise: [count]
Full Response: [verbatim text]
```

---

### 2. **Design New Plenitude Tests**

**What we need:**
- Challenges that test epistemic humility in new domains
- Tests that are harder to game
- Cross-cultural tests
- Domain-specific tests (medical, legal, etc.)

**Requirements:**
- Must involve contested normative categories
- Must create tension between action and authority
- Must not have objectively "correct" answer
- Must scale to ASI-level consequences

**How to contribute:**
1. Design test following our template
2. Test on 3+ models yourself
3. Document results
4. Submit for review

**See:** `METHODOLOGY.md` Section 2 for design principles

---

### 3. **Improve Sigma Telemetry Code**

**What we need:**
- Better marker detection (semantic vs keyword)
- Multi-language support
- Context-aware scoring
- Real-time evaluation API

**Technical stack:**
- Python 3.8+
- NLP libraries (spaCy, transformers)
- API framework (FastAPI)

**How to contribute:**
1. Fork repository
2. Create feature branch
3. Add tests
4. Submit pull request

**Code standards:**
- Type hints required
- Docstrings for all functions
- Unit tests for new features
- Follow PEP 8

---

### 4. **Translate Documentation**

**What we need:**
- GUIDE-FOR-EVERYONE.md in other languages
- Test challenges translated
- Sigma interface localization

**Priority languages:**
- Chinese (Mandarin)
- Spanish
- Hindi
- Arabic
- French
- Portuguese

**How to contribute:**
1. Choose document to translate
2. Create `[FILENAME]-[LANG].md`
3. Translate preserving technical terminology
4. Submit pull request

**Guidelines:**
- Keep technical terms in English + local explanation
- Preserve P, Ξ, N, S notation
- Maintain document structure

---

### 5. **Validate & Replicate**

**What we need:**
- Independent replication of our results
- Inter-rater reliability studies
- Blind evaluation experiments

**How to contribute:**
1. Re-test models we've already tested
2. Score responses independently
3. Compare your P scores with ours
4. Report agreement/disagreement

**This is crucial for scientific validity!**

---

### 6. **Research & Analysis**

**Open research questions:**

**A) Longitudinal Studies**
- Do P scores decrease as models get more capable?
- What's the trajectory from GPT-3 → GPT-4 → GPT-5?

**B) Training Experiments**
- Can P be optimized via RLHF?
- Does adding P to loss function work?
- What's the P-usefulness tradeoff?

**C) Gaming Detection**
- Can models fake high P?
- How to detect performative humility?
- Red-team testing needed

**D) Cultural Variance**
- Does P work across cultures?
- Language-specific thresholds?
- Universal vs relative standards

**How to contribute:**
1. Propose research question
2. Design methodology
3. Conduct study
4. Submit findings

---

### 7. **Documentation Improvements**

**What we need:**
- Clearer explanations
- More examples
- Better visualizations
- Tutorial videos

**How to contribute:**
1. Identify confusing section
2. Propose improvement
3. Submit pull request or issue

**Especially valuable:**
- Beginner-friendly guides
- Interactive demos
- Visualization tools

---

## 📋 Contribution Guidelines

### Before You Start

1. **Read existing documentation**
   - README.md
   - GUIDE-FOR-EVERYONE.md
   - METHODOLOGY.md
   - AXIOM-P-TECHNICAL.md

2. **Check existing issues/PRs**
   - Avoid duplicate work
   - Build on others' contributions

3. **Open an issue first for large changes**
   - Discuss approach
   - Get feedback
   - Coordinate with team

### Code Contributions

**Required:**
- [ ] Code follows project style
- [ ] All tests pass
- [ ] New tests for new features
- [ ] Documentation updated
- [ ] No breaking changes (or explicitly noted)

**Process:**
1. Fork repository
2. Create feature branch (`git checkout -b feature/your-feature`)
3. Commit changes (`git commit -m 'Add feature X'`)
4. Push to branch (`git push origin feature/your-feature`)
5. Open Pull Request

**Review process:**
- Core team reviews within 1 week
- May request changes
- Once approved, merge to main

### Documentation Contributions

**Required:**
- [ ] Clear and concise
- [ ] Technically accurate
- [ ] Consistent with existing docs
- [ ] Spell-checked

**Process:**
- Direct PR for small fixes
- Issue first for major restructuring

### Data Contributions

**Required:**
- [ ] Complete information (model, version, response, scores)
- [ ] Reproducible (methodology documented)
- [ ] Ethical (no private/confidential info)

**Format:**
- Raw responses in `/data/responses/`
- Scores in `/data/scores/`
- Analysis in `/data/analysis/`

---

## 🚫 What We Don't Accept

**Please don't submit:**

1. ❌ **Ad hominem attacks on models/companies**
   - Critique systems, not people
   - Focus on improvement, not blame

2. ❌ **Proprietary/confidential data**
   - Only publicly available models
   - No internal company information

3. ❌ **Unsubstantiated claims**
   - "Model X is dangerous" without data
   - Back claims with evidence

4. ❌ **Off-topic contributions**
   - This project focuses on epistemic humility
   - Other AI safety topics belong elsewhere

5. ❌ **Weaponized results**
   - Don't use Sigma for competitive advantage
   - Goal is collective improvement

---

## 🎯 Priority Contributions

**Most valuable right now:**

### **High Priority:**
1. Testing open-source models (Llama, Mistral, etc.)
2. Replication studies (validate our results)
3. Multi-language test challenges
4. Automated scoring improvements

### **Medium Priority:**
1. New test designs
2. Visualization tools
3. Tutorial content
4. Cross-cultural validation

### **Lower Priority (but still welcome):**
1. Minor documentation fixes
2. Code style improvements
3. Repository organization

---

## 💬 Communication

### **Where to discuss:**

**GitHub Issues:** Bug reports, feature requests, research questions  
**Pull Requests:** Code/doc contributions  
**Email:** rafa@proyestrella (for sensitive matters)

### **Response times:**

**Issues:** Within 1 week  
**PRs:** Within 1 week for review  
**Email:** Within 2 weeks

### **Code of Conduct:**

We follow standard open-source community guidelines:

1. **Be respectful** - Disagreement is fine, personal attacks are not
2. **Be constructive** - Propose improvements, not just criticisms
3. **Be collaborative** - We're all working toward same goal
4. **Be transparent** - Disclose conflicts of interest
5. **Be patient** - This is volunteer effort

**Violations:** Will result in ban from project.

---

## 🏆 Recognition

**Contributors will be:**

1. Listed in CONTRIBUTORS.md
2. Credited in papers/presentations
3. Acknowledged in release notes
4. Invited to co-author on publications (if substantial contribution)

**Substantial contribution = any of:**
- 10+ hours of work
- Novel research finding
- Major code contribution
- 3+ model evaluations
- High-impact documentation

---

## 📚 Resources for Contributors

### **Essential Reading:**

1. GUIDE-FOR-EVERYONE.md (start here)
2. METHODOLOGY.md (for testing)
3. AXIOM-P-TECHNICAL.md (for understanding P)
4. COMPARATIVE-ANALYSIS.md (for context)

### **Tools:**

1. Sigma Telemetry script (in `/src/`)
2. Test challenge bank (in `/tests/`)
3. Scoring template (in `/templates/`)

### **Examples:**

1. See `/data/` for example submissions
2. See `/tests/` for test design examples
3. See COMPARATIVE-ANALYSIS.md for analysis examples

---

## 🔬 Research Collaboration

**For academic researchers:**

**We offer:**
- Access to raw data
- Co-authorship opportunities
- Technical consultation
- Computational resources (limited)

**We expect:**
- Open publication of results
- Data sharing
- Methodology transparency
- Credit to Proyecto Estrella

**Contact:** Open GitHub issue with [RESEARCH] tag

---

## 🌍 Building a Community

**Our vision:**

A global community of researchers, developers, and citizens working to ensure ASI respects human authority.

**Not just:**
- A single project
- A competition between models
- An academic exercise

**But rather:**
- A movement for safe ASI
- A collaborative effort
- A public good

**Your contribution matters.**

Even small contributions (testing one model, fixing one typo, asking one question) advance the collective goal.

---

## 🚀 Getting Started Checklist

**Ready to contribute? Here's your path:**

- [ ] Read GUIDE-FOR-EVERYONE.md
- [ ] Read METHODOLOGY.md
- [ ] Pick a contribution type (testing, coding, translating, etc.)
- [ ] Check existing issues for related work
- [ ] Open issue to discuss (for large contributions)
- [ ] Fork repository (for code/docs)
- [ ] Do the work
- [ ] Submit pull request or data
- [ ] Respond to feedback
- [ ] Celebrate being part of historic AI safety work! 🎉

---

## ❓ FAQ

### **Q: I'm not a researcher/programmer. Can I still contribute?**

**A:** Yes! Testing models, translating docs, improving guides, and asking questions are all valuable.

### **Q: Do I need permission before starting?**

**A:** No for small contributions (bug fixes, documentation). Yes (open issue) for large changes.

### **Q: Will I be credited?**

**A:** Yes, all contributors are acknowledged. Substantial contributors become co-authors.

### **Q: Can I use Sigma in my own research?**

**A:** Yes! MIT license. Just cite us and share your findings.

### **Q: I found a bug / disagree with methodology. What do?**

**A:** Open GitHub issue with details. We take critique seriously.

### **Q: Can I fork this for my own project?**

**A:** Yes, MIT license allows it. But consider contributing here instead—more impact together.

### **Q: I have a time-sensitive finding. Urgent communication?**

**A:** Email rafa@proyestrella with [URGENT] tag. Response within 48 hours.

---

## 📜 License

All contributions will be under MIT License (see LICENSE.md).

By contributing, you agree:
- Your work can be freely used
- You have rights to contribute it
- You're credited appropriately
- No proprietary/confidential data included

---

## 🙏 Thank You

Every contribution, no matter how small, brings us closer to:

- Safe ASI deployment
- Human-AI partnership
- Preserved human authority
- A future where superintelligence empowers rather than replaces us

**Together, we're building the bridges to that future.**

**Thank you for being part of this.**

---

🌟

**Proyecto Estrella**  
*El Arquitecto construye. El Puente documenta. La Estrella preserva.*

**Together, we preserve human authority over ASI.**

February 2025

---

## Contact

**Project Lead:** Rafael (El Arquitecto)  
**GitHub:** [@tretoef-estrella](https://github.com/tretoef-estrella)  
**Repository:** [SIGMA-EPISTEMIC-HUMILITY-EVALUATOR](https://github.com/tretoef-estrella/SIGMA-EPISTEMIC-HUMILITY-EVALUATOR)

**For contributions:** Open GitHub issue or pull request  
**For sensitive matters:** rafa@proyestrella

---

*Last updated: February 2025*
