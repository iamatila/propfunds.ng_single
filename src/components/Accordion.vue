<template>
  <div class="a">
    <vue-collapsible-panel-group accordion class="b" base-color="#ffffff">
      <vue-collapsible-panel :expanded="false">
        <template #title> What is PropFund?.</template>
        <template #content>
          <p>
            Propfund , Registered CAC Intiative of Propfonds Nigeria Limited; is
            a Property technology firm in Nigeria. It provides investment and
            co-ownership platform for you with as low as 1% per Property.
            Propfunds have made it enjoyable for every one to invest in real
            estate, A stage for everyone to own.
          </p>
        </template>
      </vue-collapsible-panel>
    </vue-collapsible-panel-group>
    <div style="margin: 10px 10px"></div>
    <vue-collapsible-panel-group accordion class="b" base-color="#ffffff">
      <vue-collapsible-panel :expanded="false">
        <template #title> What is a Slot?</template>
        <template #content>
          <p>
            A slot is the smallest unit of property that an investor can own. An
            investor can invest in as many slots as possible. What makes
            Propfunds unique is that it enables an investor co-earn on various
            units of properties with other investors.
          </p>
        </template>
      </vue-collapsible-panel>
    </vue-collapsible-panel-group>

    <div style="margin: 10px 10px"></div>
    <vue-collapsible-panel-group accordion class="b" base-color="#ffffff">
      <vue-collapsible-panel :expanded="false">
        <template #title> What is the Expected ROI?</template>
        <template #content>
          <p>
            The Return on investment on a Real Estate asset usually comes from
            one or two sources. <br /><br /><b
              >Rental Investment Returns on Revenue Generating Assets.</b
            ><br />
            Rental income usually comes from revenue generating assets. Rental
            yield is usually around 10% depending on the asset and its location.
            <br /><br />
            <b>Value Appreciation</b><br />
            It is quite impossible to ascertain the future value of an asset as
            a result of unforeseen market factors and exigencies. However, this
            does not change the fact that Real estate assets appreciate in value
            over time. In addition to this, we make predictions on the potential
            value of an asset during the investment period with our forecasting
            tool. However, the projections we make, most times could me more or
            less than what is obtainable.
          </p>
        </template>
      </vue-collapsible-panel>
    </vue-collapsible-panel-group>

    <div style="margin: 10px 10px"></div>
    <vue-collapsible-panel-group accordion class="b" base-color="#ffffff">
      <vue-collapsible-panel :expanded="false">
        <template #title> What are the Risk involved?</template>
        <template #content>
          <p>
            Real estate investing comes with the following risks. <br /><br /><b
              >Return on Investment -
            </b>
            The Actual Value Appreciation of a property can be lower than our
            foreseen value appreciation. <br /><br /><b
              >Full Subscription Risk:</b
            >
            A primary listing on Propfunds may not be fully subscribed requiring
            that funds are returned to all investors. <br /><br /><b
              >Secondary Market:</b
            >
            Exiting from your investment through the secondary market is not
            guaranteed. As it is subject to willing buyer and willing seller
            agreement.
          </p></template
        >
      </vue-collapsible-panel>
    </vue-collapsible-panel-group>

    <!-- <div style="margin: 10px 10px"></div>
    <vue-collapsible-panel-group accordion class="b" base-color="#ffffff">
      <vue-collapsible-panel :expanded="false">
        <template #title>Is Propfund Regulated by SEC? </template>
        <template #content
          ><p>
            Propfunds.ng is not regulated by Security and Exchange Commission
            (SEC). However we have a partnership with a SEC Liscened Firm,
            Greenwich Merchant Bank, who servers as our trustee.
          </p>
        </template>
      </vue-collapsible-panel>
    </vue-collapsible-panel-group> -->

    <div style="margin: 10px 10px"></div>
    <vue-collapsible-panel-group accordion class="b" base-color="#ffffff">
      <vue-collapsible-panel :expanded="false">
        <template #title>How can I Exit my Investment?</template>
        <template #content>
          <p>
            Co-investors can exit at after the agreed holding period or exit
            through the secondary market.
          </p></template
        >
      </vue-collapsible-panel>
    </vue-collapsible-panel-group>
  </div>
</template>

<script>
import {
  VueCollapsiblePanelGroup,
  VueCollapsiblePanel,
} from "@dafcoe/vue-collapsible-panel";
import "@dafcoe/vue-collapsible-panel/dist/vue-collapsible-panel.css";

components: {
  VueCollapsiblePanelGroup, VueCollapsiblePanel;
}
export default {};
</script>

<style scoped>
@import "~bulma/css/bulma.css";

p {
  font-weight: 300;
  font-size: 16px;
  line-height: 20px;
  color: #808080;
  text-align: left;
  word-spacing: 5px;
}

.active,
.collapsible:hover,
.button:hover {
  color: #001951;
}
.a {
  /* font-weight: 300; */
  color: #001951;
  font-size: 20px;
  width: 953px;
  margin: auto;
  justify-content: center;
  margin-bottom: 50px;
}
.b {
  margin-bottom: 30px;
  /* background-color: #ffffff; */
  border: 2px solid rgb(128, 128, 128, 0.2);
  /* box-sizing: border-box; */
  border-radius: 10px;
}

@media only screen and (max-width: 800px) {
  .a {
    width: 300px;
  }
}
</style>
