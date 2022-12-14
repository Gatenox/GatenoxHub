# Apply via Gatenox

Instead of sending each user an invitation email ([send-invitation-for-review.md](send-invitation-for-review.md "mention")), you can add "Apply via Gatenox" button or link on your webpage / portal using your referral code ([referral-code.md](referral-code.md "mention")).

You can use the following button to inform users about verification processes via Gatenox:

<figure><img src="../../.gitbook/assets/apply_via_gatenox.png" alt="&#x22;Apply via Gatenox&#x22; button"><figcaption><p>"Apply via Gatenox" button</p></figcaption></figure>

{% tabs %}
{% tab title="button.html" %}
```
<a class="GatenoxButton" href="https://app.gatenox.com/referrals/join/GATENOX">
	<div class="GatenoxButton-caption">Apply via Gatenox</div>
</a>
```

The "GATENOX" code in href link should be replaced with your referral code. It is available to copy from "Settings" menu, tab "Company information" ([#where-is-my-referral-code](referral-code.md#where-is-my-referral-code "mention")).
{% endtab %}

{% tab title="button.css" %}
```
.GatenoxButton {
  margin: 0 auto;
  display: block;
  position: relative;

  height: 50px;
  width: 286px;
  border-radius: 10px;
  background-color: #6610F2;
  box-shadow: 0 5px 10px -5px rgba(0,0,0,0.2);
}

.GatenoxButton-caption {
  position: absolute;
  top: 9px;
  left: 62px;

  height: 30px;
  width: 224px;
  color: #FFFFFF;
  font-family: Roboto;
  font-size: 24px;
  line-height: 30px;
  font-weight: 100;
  text-align: center;

}
```
{% endtab %}
{% endtabs %}
