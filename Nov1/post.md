Part of deploying code is taking away the manual labor

# Automating Away the Tedious: A CI/CD Journey (3/5)

Early deployment process:
1. Code changes locally
2. SSH into EC2
3. rsync files
4. Restart services
5. Cross fingers
6. Repeat for every change

Not exactly cutting edge. Time to modernize.

[Insert CI/CD workflow diagram]

The new pipeline:
- Push to main triggers GitHub Actions
- Frontend: 
  → Build
  → Deploy to S3
  → Invalidate CloudFront cache
- Backend:
  → Build Docker image
  → Push to DockerHub
  → Auto-pull on EC2
  → Restart container

Key components:
```yaml
systemd service for runner:
- Always-on GitHub Actions runner
- Auto-restarts if crashes
- Monitors for new workflows

systemd service for backend:
- Watches DockerHub for updates
- Pulls new images automatically
- Handles container lifecycle
```

The result? Push code, get coffee, find it deployed. No SSH required.

Lessons learned:
- Self-hosted runners > Cloud runners for this use case
- systemd is your friend for process management
- Proper environment separation is crucial
- Automated > Manual, every time

Next post: Security considerations and best practices in a cloud environment.

#DevOps #Automation #GitHub #AWS