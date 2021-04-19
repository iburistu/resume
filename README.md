# resume

[![Automated Upload to S3](https://github.com/iburistu/resume/actions/workflows/compile.yml/badge.svg?branch=main&event=push)](https://github.com/iburistu/resume/actions/workflows/compile.yml)

This repository holds the .tex file of my resume. I got tired of going into Overleaf, editing my resume, downloading it, and uploading it to cloud storage. I figured that because my resume is already public, there's no harm in making the 'source' public as well.

There's a Github Action that compiles the .tex to a .pdf and uploads it to S3 for me on commits to the `main` branch. There's a bit of hackery going on to force the job to run all the way through - turns out the .tex file has errors and even though it technically compiles it returns a non-zero status code, causing the job to eject as a failure. So I force it to progress and upload the result to S3...

You can see the most recent resume [here](https://linkletter.s3.amazonaws.com/public/resume.pdf)!
