# Maintainer Guide

This guide is for maintainers and team members managing the YoLauncher issue tracker and community repository.

## Repository Purpose

This repository serves as the **public interface** for YoLauncher:
- Issue tracking for bug reports and feature requests
- Community engagement and support
- Roadmap visibility and transparency
- Documentation hosting

**Important**: The actual YoLauncher source code is maintained separately in a private repository.

## Daily Responsibilities

### Issue Triage

New issues should be reviewed regularly (ideally daily):

1. **Review new issues** tagged with `needs-triage`
2. **Validate submissions**:
   - Is the issue template filled out properly?
   - Is there enough information to understand the problem?
   - Is it a duplicate of an existing issue?
3. **Apply appropriate labels**:
   - Type: `bug`, `enhancement`, `question`, `documentation`
   - Priority: `critical`, `high`, `medium`, `low`
   - Status: `accepted`, `needs: more-info`, etc.
4. **Add to milestone** (if accepted for upcoming release)
5. **Respond to reporter**: Acknowledge the issue and provide updates

### Managing Labels

Use the provided label system consistently:

#### Issue Types
- `bug` - Something broken or not working
- `enhancement` - New features or improvements
- `question` - User questions or support
- `documentation` - Docs improvements

#### Priority
- `priority: critical` - Urgent, blocking users
- `priority: high` - Important, affects many users
- `priority: medium` - Should address soon
- `priority: low` - Nice to have

#### Status
- `needs-triage` - Needs initial review
- `status: accepted` - Confirmed, will address
- `status: in-progress` - Being worked on
- `status: completed` - Resolved
- `status: blocked` - Waiting on something
- `needs: more-info` - Need more details from reporter

### Community Engagement

- **Respond promptly**: Aim for initial response within 24-48 hours
- **Be professional**: Maintain a helpful, respectful tone
- **Provide updates**: Keep reporters informed of progress
- **Close resolved issues**: Mark as completed when fixed
- **Thank contributors**: Acknowledge helpful reports and suggestions

## Issue Management Workflow

### Bug Reports

1. **Validate the bug**:
   - Can you reproduce it?
   - Is it actually a bug or user error?
   - What version(s) are affected?

2. **Assess priority**:
   - How many users are affected?
   - Is there a workaround?
   - What's the severity?

3. **Track in private repo**:
   - Create corresponding issue/task in private codebase
   - Link issues for tracking (in private notes)

4. **Update public issue**:
   - Add to milestone if scheduled
   - Update status as work progresses
   - Close when fixed in a release

### Feature Requests

1. **Evaluate the request**:
   - Does it align with product vision?
   - How many users would benefit?
   - What's the implementation effort?

2. **Gather feedback**:
   - Ask clarifying questions
   - Get community input (👍 reactions)
   - Consider alternatives

3. **Make a decision**:
   - Accept: Add `status: accepted`, add to roadmap
   - Consider: Add `discussion` label
   - Decline: Add `wontfix`, explain reasoning

4. **Track and update**:
   - Add to appropriate milestone
   - Update as plans evolve
   - Close when implemented

### Questions

1. **Provide answers**:
   - Answer directly if straightforward
   - Link to documentation if available
   - Escalate to team if needed

2. **Improve documentation**:
   - If question is common, consider adding to docs
   - Create FAQ entries for frequent questions

3. **Close when resolved**:
   - Mark as completed when answered
   - Encourage reporter to confirm answer helped

## Milestones and Projects

### Creating Milestones

- Use semantic versioning: `v1.2.3`
- Include target date (can be adjusted)
- Write clear descriptions of release themes
- Add issues/PRs as they're scheduled

### Managing Projects

- Use project boards for sprint planning
- Columns: Backlog, Planned, In Progress, Done
- Move issues as status changes
- Review and update regularly

## Release Process

When a new version is released:

1. **Update issues**:
   - Close all fixed issues
   - Tag with milestone
   - Comment with release info

2. **Create release notes**:
   - List new features
   - List bug fixes
   - Include upgrade instructions
   - Credit contributors

3. **Communicate**:
   - Post release announcement
   - Update roadmap
   - Thank community

## Handling Difficult Situations

### Duplicate Issues

- Mark as `duplicate`
- Link to original issue
- Close with friendly message
- Ask reporter to follow original issue

### Invalid Issues

- Mark as `invalid`
- Explain why (kindly)
- Suggest correct approach if appropriate
- Close the issue

### Won't Fix

- Mark as `wontfix`
- Provide clear explanation
- Offer alternatives if possible
- Close respectfully

### Aggressive or Inappropriate Behavior

- Stay professional
- Refer to Code of Conduct
- Warn once if appropriate
- Block/report if behavior continues
- Document incidents

## Security Issues

**Critical**: Security issues should never be discussed in public issues.

If a security issue is reported publicly:
1. Ask reporter to delete and resubmit privately
2. Delete the public issue
3. Follow security policy process
4. Keep issue private until patched

## Using Label Sync

The `.github/labels.yml` file can be used with label management tools to keep labels consistent:

```bash
# Example using github-label-sync
npx github-label-sync --access-token [token] LiF-x/YoLauncher
```

## Best Practices

### Communication

- Be clear and concise
- Use friendly, professional tone
- Provide context and reasoning
- Set realistic expectations
- Follow up on commitments

### Organization

- Review open issues regularly
- Keep milestones up to date
- Update roadmap as plans change
- Archive completed milestones
- Clean up old issues

### Transparency

- Share what you can
- Explain decisions
- Be honest about timelines
- Admit mistakes
- Credit contributors

### Privacy

- Don't share proprietary code
- Don't discuss internal matters
- Don't share customer data
- Protect security vulnerabilities
- Respect confidential information

## Tools and Automation

Consider using:

- **Saved replies**: For common responses
- **Issue templates**: Already configured
- **Project automation**: Auto-move cards
- **Label sync**: Keep labels consistent
- **Bots**: For routine tasks (stale issues, etc.)

## Team Coordination

### Internal Communication

- Sync with development team regularly
- Share priority feedback
- Coordinate releases
- Escalate critical issues
- Share community feedback

### Handoff Notes

When transitioning maintainer duties:
- Document pending issues
- Share context on major items
- Explain any special situations
- Introduce new maintainer to community

## Resources

- GitHub Docs: https://docs.github.com
- GitHub Community Guidelines: https://docs.github.com/en/site-policy/github-terms/github-community-guidelines
- Issue and PR templates: https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests

## Questions?

If you're unsure about something:
- Ask other maintainers
- Check GitHub documentation
- Err on the side of being helpful
- Document learnings for future reference

---

Remember: This repository represents YoLauncher to the public. Your interactions here shape how users perceive the product and the organization. Be helpful, professional, and transparent within appropriate bounds.
