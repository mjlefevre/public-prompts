# Fabric Patterns Catalog

A comprehensive catalog of all patterns available in the [Fabric framework](https://github.com/danielmiessler/fabric) by Daniel Miessler.

**Key Pattern:** `suggest_pattern` - Suggests appropriate fabric patterns or commands based on user input.

## Table of Contents

- [General Use Patterns](#general-use-patterns)
- [Specific Role/Job Patterns](#specific-rolejob-patterns)
- [About Fabric](#about-fabric)

---

## General Use Patterns

These patterns can be used across various domains and aren't specific to particular jobs.

### Content Creation & Writing

- **create_summary**: Creates concise summaries in various formats
- **create_micro_summary**: Creates very brief 20-word summaries
- **summarize**: Formats content into key points and takeaways
- **summarize_micro**: Creates minimal summaries with main points
- **create_aphorisms**: Generates brief, witty statements
- **create_art_prompt**: Generates detailed visual descriptions
- **create_formal_email**: Crafts professional emails
- **write_essay**: Writes concise essays in Paul Graham's style
- **write_micro_essay**: Creates short, clear essays
- **humanize**: Rewrites AI text to sound more natural
- **improve_writing**: Refines text with grammar and style
- **clean_text**: Fixes broken or malformatted text
- **convert_to_markdown**: Converts content to clean Markdown
- **analyze_prose**: Evaluates writing for novelty and clarity
- **analyze_prose_json**: Similar to analyze_prose but in JSON format
- **analyze_prose_pinker**: Evaluates prose based on Steven Pinker's style

### Data Analysis & Extraction

- **extract_ideas**: Extracts key ideas as bullet points
- **extract_insights**: Extracts powerful ideas from text
- **extract_main_idea**: Extracts main idea and recommendation
- **extract_core_message**: Extracts core message of text
- **extract_primary_problem**: Identifies primary problem in text
- **extract_primary_solution**: Identifies primary solution in text
- **extract_recommendations**: Extracts practical recommendations
- **export_data_as_csv**: Outputs data structures as CSV
- **extract_wisdom**: Extracts insights on human flourishing, AI, etc.
- **extract_controversial_ideas**: Extracts controversial statements
- **extract_questions**: Extracts questions from conversations

### Visualization & Organization

- **create_mermaid_visualization**: Creates visualizations using Mermaid syntax
- **create_mermaid_visualization_for_github**: Similar but GitHub-optimized
- **create_visualization**: Creates visualizations using ASCII art
- **create_idea_compass**: Organizes ideas by exploring definition and evidence
- **create_markmap_visualization**: Transforms ideas into MarkMap visualizations
- **create_recursive_outline**: Breaks down complex tasks hierarchically
- **compare_and_contrast**: Compares items in a markdown table

### General Problem Solving

- **solve_with_cot**: Provides step-by-step chain of thought reasoning
- **raw_query**: Analyzes input to produce best possible result
- **rate_value**: Produces optimal output based on deep analysis
- **create_better_frame**: Analyzes different frames of interpreting reality
- **find_logical_fallacies**: Identifies fallacies in arguments
- **explain_math**: Explains mathematical concepts clearly
- **ai**: Interprets questions and provides concise answers
- **suggest_pattern**: Recommends appropriate fabric patterns based on input

---

## Specific Role/Job Patterns

### Software Development & Engineering

- **create_coding_project**: Generates wireframes and starter code
- **create_design_document**: Creates detailed system design documents
- **create_prd**: Creates Product Requirements Documents
- **create_user_story**: Writes technical user stories
- **agility_story**: Generates user stories and acceptance criteria
- **create_git_diff_commit**: Generates Git commands and commit messages
- **explain_code**: Explains code and security tool output
- **coding_master**: Explains coding concepts to beginners
- **summarize_git_changes**: Summarizes recent project updates
- **summarize_git_diff**: Summarizes Git diff changes
- **summarize_pull-requests**: Summarizes pull requests
- **write_pull-request**: Drafts detailed pull request descriptions
- **review_design**: Reviews and analyzes architecture design
- **refine_design_document**: Refines design documents based on reviews
- **explain_project**: Summarizes project documentation

### Cybersecurity & IT

- **analyse_incident**: Extracts details from cybersecurity breach articles
- **analyse_logs**: Analyzes server log files to identify issues
- **analyse_malware**: Analyzes malware details and indicators
- **analyze_threat_report**: Extracts insights from cybersecurity reports
- **analyse_threat_report_cmds**: Extracts cybersecurity commands
- **analyse_threat_report_trends**: Extracts trends from threat reports
- **analyse_email_headers**: Analyzes email security headers
- **create_network_threat_landscape**: Analyzes network security threats
- **create_security_update**: Creates concise security updates
- **create_sigma_rules**: Creates Sigma detection rules
- **create_stride_threat_model**: Creates STRIDE-based threat models
- **create_threat_scenarios**: Identifies attack methods
- **extract_poc**: Extracts proof of concept URLs from security reports
- **write_hackerone_report**: Generates bug bounty reports
- **write_nuclei_template_rule**: Generates Nuclei templates
- **write_semgrep_rule**: Creates Semgrep rules
- **create_command**: Helps determine parameters for penetration testing tools
- **create_report_finding**: Creates security finding reports
- **improve_report_finding**: Improves security findings
- **ask_secure_by_design_questions**: Generates security-focused questions

### Academic & Research

- **create_academic_paper**: Generates academic papers in LaTeX format
- **analyse_paper**: Analyzes research papers
- **summarize_paper**: Summarizes academic papers
- **create_reading_plan**: Generates review questions and reading plans
- **to_flashcards**: Creates Anki flashcards from text
- **create_quiz**: Creates reading plans and quizzes
- **analyse_answers**: Evaluates quiz answers
- **explain_terms**: Produces glossaries of advanced terms
- **write_latex**: Generates LaTeX code

### Business & Professional

- **analyse_candidates**: Compares political candidates
- **analyse_cfp_submission**: Reviews conference submissions
- **analyse_claims**: Analyzes truth claims with evidence
- **analyse_comments**: Evaluates internet comments
- **analyse_debate**: Rates debates with analysis
- **summarize_debate**: Summarizes debates and arguments
- **analyze_product_feedback**: Analyzes user feedback
- **analyze_sales_call**: Rates sales call performance
- **answer_interview_question**: Generates interview responses
- **analyze_risk**: Conducts risk assessments
- **check_agreement**: Analyzes contracts and agreements
- **create_keynote**: Creates TED-style presentations
- **create_ttrc_graph**: Creates vulnerability remediation graphs
- **create_ttrc_narrative**: Creates narratives about vulnerability metrics
- **create_7s_strategy**: Prepares strategy documents
- **create_hormozi_offer**: Creates business offers

### Content Analysis & Media

- **analyze_interviewer_techniques**: Analyzes interviewer techniques
- **analyze_personality**: Performs psychological analysis
- **analyze_presentation**: Reviews presentations
- **extract_song_meaning**: Analyzes song meanings
- **extract_videoid**: Extracts video IDs from URLs
- **extract_latest_video**: Extracts latest YouTube video URLs
- **get_youtube_rss**: Returns RSS URLs for YouTube channels
- **get_wow_per_minute**: Determines content's "wow-factor"
- **summarize_lecture**: Extracts topics from lecture transcripts
- **create_video_chapters**: Extracts topics and timestamps
- **extract_instructions**: Extracts instructions from video transcripts
- **youtube_summary**: Creates timestamped video summaries
- **create_show_intro**: Creates intros for podcasts
- **extract_sponsors**: Extracts sponsors from transcripts

### Specialized Professional Tasks

- **analyse_patent**: Analyzes patents in detail
- **analyse_military_strategy**: Analyzes historical battles
- **analyze_proposition**: Analyzes ballot propositions
- **analyze_spiritual_text**: Compares spiritual texts
- **analyze_tech_impact**: Analyzes technology societal impact
- **summarize_legislation**: Summarizes political proposals
- **capture_thinkers_work**: Analyzes philosophers and works
- **create_ai_jobs_analysis**: Analyzes job automation susceptibility
- **dialog_with_socrates**: Engages in Socratic method dialogues
- **extract_skills**: Extracts and classifies skills from job descriptions
- **identify_job_stories**: Identifies key job requirements
- **provide_guidance**: Provides psychological advice

### Meeting & Documentation

- **summarize_meeting**: Analyzes meeting transcripts
- **transcribe_minutes**: Extracts meeting minutes
- **create_newsletter_entry**: Creates newsletter summaries
- **enrich_blog_post**: Enhances blog posts
- **explain_docs**: Improves tool documentation
- **extract_newsletter_wisdom**: Extracts newsletter content
- **create_tags**: Identifies tags from content
- **create_diy**: Creates DIY tutorial patterns
- **extract_recipe**: Extracts recipe information

### Gaming & Creative

- **create_npc**: Generates D&D 5E NPCs
- **create_rpg_summary**: Summarizes RPG sessions
- **summarize_rpg_session**: Similar to create_rpg_summary
- **create_logo**: Creates minimalist company logos
- **create_story_explanation**: Summarizes content in story format

---

## About Fabric

Fabric is an **independent open-source project** (MIT licensed) created by Daniel Miessler in January 2024. It's a framework for augmenting humans using AI, providing a modular system for solving specific problems using a crowdsourced set of AI prompts.

### Key Facts

- **License:** MIT (fully open source)
- **GitHub Stars:** 30,000+
- **Contributors:** ~300 developers worldwide
- **Patterns Available:** 200+

### Philosophy

Miessler's core insight is that *prompting is the center mass of AI* — not RAG or fine-tuning, but well-crafted, reusable prompts. Fabric provides a universally accessible layer of AI that anyone can use to enhance their life or work.

### Links & Resources

| Resource | Link |
|----------|------|
| **GitHub Repository** | [danielmiessler/fabric](https://github.com/danielmiessler/fabric) |
| **Origin Story** | [Why I Created Fabric](https://danielmiessler.com/blog/fabric-origin-story) |
| **Video Introduction** | [Hack Your Life with AI (David Bombal)](https://youtu.be/vF-MQmVxnCs) |
| **Positive Writeup** | [The Best AI Tool You've Never Heard Of](https://medium.com/@thomas_reid/an-introduction-to-fabric-the-best-ai-tool-youve-never-heard-of-94a0b4f59ac6) |
| **Getting Started Guide** | [Infralovers Overview](https://www.infralovers.com/blog/2024-06-25-fabric-overview/) |