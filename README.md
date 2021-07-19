Note: this is a companion workflow for triggering auto-deploys of the site every time there is a new edit to any of the files in `tasks.json`. To know more go to [@ayshptk/blogengine](https://github.com/ayshptk/blogengine)

# How to use?
1. Download this code and add it to all the repos you want to trigger the deploy from, for your main website.
2. Go to vercel project settings of the site you want to trigger the deploy for
<img width="442" alt="Screenshot 2021-07-19 at 4 02 44 PM" src="https://user-images.githubusercontent.com/62694274/126147076-ffde663f-5227-4e89-88e3-07108e7af5de.png">
3. Click on the Git tab
<img width="218" alt="Screenshot 2021-07-19 at 4 03 12 PM" src="https://user-images.githubusercontent.com/62694274/126147127-61ae9f00-dbac-47cf-b290-04f9b01c272c.png">
4. Scroll down to Deploy Hooks section, give it a nice name, and write the name of the branch you want to trigger deploy for, and click on create hook.
<img width="796" alt="Screenshot 2021-07-19 at 4 32 56 PM" src="https://user-images.githubusercontent.com/62694274/126150561-69075f08-17f5-4748-a09b-75712ee1d099.png">
5. Copy this webhook and go to the github repo settings for each repo this action is going to be in. Scroll down and click on the `secrets` tab.

Click on add repository secret button and name the secret as `deploy`. Paste the webhook you copied in the `value` field. Hit save.
<img width="1002" alt="Screenshot 2021-07-19 at 4 35 29 PM" src="https://user-images.githubusercontent.com/62694274/126150830-03e2d867-777e-4266-9522-531959f94b2e.png">


That's it! Now every time there's a new commit to every repo you add this webhook to, it will trigger a deploy of the site you configured it to do. Note you only have to generate webhook once, and only for the repo you want to mirror this to. But you have to add this workflow and the secrets to every other repo you want to mirror files from. 

Good luck!

