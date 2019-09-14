# serverless-github-action

A Github Serverless CLI action for making deploying (and other serverless operations) easy!

## Usage

In your workflow yml file add a step entry with:

```
    - name: serverless deploy
      uses: tegud/serverless-github-action@1.52.0
      with:
        args: deploy
      env:
        AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
        AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```

You'll need to adjust for your cloud provider of choice, and ensure that your secrets are set up in the Settings/Secrets section in github.

**NOTE**: Use Secerts, dont commit your credentials!

## Why not the official one?

I created this action because I didn't want to have a 50s of npm installing serverless cli every deployment, this action uses an image with the CLI already installed globally, reducing action time.
