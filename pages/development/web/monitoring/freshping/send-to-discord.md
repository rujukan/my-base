# Freshping Alert to Discord through Zapier

I monitor some of my services through FreshPing. Freshping itself is already helpful when alerting downtime through emails. But who still regularly check emails all the time anyway? I want to improve it further by integrating it to my personal Discord server. So, every time a new down alert is triggered, I want to be notified through Discord. This is all possible with ✨ Webhooks ✨ and Zapier.

## How to Setup

1. Setup a Zapier account.
2. Add new zaps.
3. In zaps creation wizard, add new trigger, choose Freshping.
   ![Zapier Pick Trigger Freshping](/images/freshping-zapier-discord/zapier-pick-trigger-freshping.png)
   ![Zapier Trigger Freshping New Alert Event](/images/freshping-zapier-discord/zapier-trigger-freshping-new-alert-event.png)
4. Open Test Trigger tab, Zapier will provide a webhook to be integrated with the corresponding Freshping dashboard. Follow the instructions below the webhook URL.
   ![Zapier Trigger Freshping Webhook](/images/freshping-zapier-discord/zapier-trigger-freshping-webhook.png)
5. Go to the Freshping dashboard, go to settings > integrations. Paste the webhook url from zapier.
   ![Freshping Create Integration](/images/freshping-zapier-discord/freshping-create-integration.png)
   ![Freshping add webhook](/images/freshping-zapier-discord/freshping-add-webhook.png)
6. Test the trigger, if it worked, continue to next step.
7. Add new action, choose Discord.
8. Connect and authorize access to a Discord server.
9. Choose a channel, setup the message content, customize according to needs.
   ![Zapier Trigger Freshping Alert to Discord Channel](/images/freshping-zapier-discord/zapier-send-freshping-alert-to-discord-channel.png)
10. Test the action.
11. Voila!
    ![Discord Alert](/images/freshping-zapier-discord/discord-alert.png)

## Notes

This guide is not limited to Freshping, Zapier, and Discord. Any platform with webhook integration enabled can be connected. For example we can setup notification to Slack, or from New Relic to Slack, or from GitLab to Discord, or from Netlify to Discord. Some integrations might need Zapier or similar service, some can be connected directly, the combinations is endless.
