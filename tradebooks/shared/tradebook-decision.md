# Tradebook Decision Process

Use this document to decide which tradebooks are applicable to this stock today, then open the relevant tradebook file for the full execution rules. Tradebooks in scope:
- [`Gap and Go`](../gap_and_go.md)
- [`Gap and Crap`](../gap_and_crap.md)  
- [`Gap Give and Go`](../gap_give_and_go.md)

## Decision Table for Gap Up Stocks

Main consideration for a gap up stocks: whether/where are the sellers going to show up? There are two possible conditions for sellers to show up early after market opens. We want to ask the following questions:

Q1: Whether there have been previous buyers having too much profit.
Q2: Whether the stock gapped right into into heavy resistance.

- If the answer is clearly yes, that's a good candidate for Gap and Crap. 
- If the answer is clearly no, that's a good candidate for Gap and Go. 
- If not sure, then it's probably not a good stock for my system. 

Note that each question should have its own answer and they don't have to align. Like if a stock gapped up way above all time high, then it's a clear yes for Q1 but also a clear no for Q2, and that makes it applicable to both gap_and_go and gap_and_crap

<!-- Side-by-side needs HTML: pipe tables can’t do lists in cells. Alternative: two &lt;div style="display:grid; grid-template-columns:1fr 1fr; gap:1rem"&gt; columns with &lt;h4&gt; + &lt;ul&gt; each. -->
<table>
  <tbody>
    <tr>
      <td scope="col"><strong>Gap and Crap</strong></td>
      <td scope="col"><strong>Gap and Go</strong></td>
    </tr>
    <tr class="doc-row-head">
      <th scope="row">Too much profit from large players</th>
      <th scope="row">No major profit taking expected for today</th>
    </tr>
    <tr>
      <td>
        <ul>
          <li><code>[recent rally without pullback]</code> — daily, weekly, or monthly</li>
          <li><code>[earnings]</code> — may not be enough if it’s just earnings</li>
          <li><code>[extended gap up]</code> (&gt;1 or 2 ATR)</li>
        </ul>
      </td>
      <td>
        <ul>
          <li><code>[near above consolidation range]</code> or <code>[near below consolidation range top]</code></li>
          <li><code>[recent pullback]</code> — moved to a previous resistance and pulled back as expected; if we get above the pullback high, that resistance can be gone. Sometimes it’s far above the previous pullback high; it still means there was a recent pullback.</li>
          <li><code>[recent consolidation]</code> — consolidation before the gap up</li>
          <li><code>[near above a previous key event level]</code></li>
          <li><code>[previous inside day]</code> — previous day was inside the day before; gap near above the 2-day high</li>
        </ul>
      </td>
    </tr>
    <tr class="doc-row-head">
      <th scope="row">Gap to area with heavy resistance </th>
      <th scope="row">No major resistance from here</th>
    </tr>
    <tr>
      <td>
        <ul>
          <li>Gap up to <code>[heavy supply zone]</code> — range created by 10+ days or a few large volume days</li>
          <li>Gap up to the <code>[top edge of current range]</code></li>
          <li><code>[near below previous key event level]</code></li>
        </ul>
      </td>
      <td>
        <ul>
          <li><code>[all time high]</code> — open above the all-time high, but not too far above; too far above attracts more sellers</li>
          <li><code>[light zone above]</code></li>
          <li><code>[acceleration level]</code></li>
        </ul>
      </td>
    </tr>
    <tr class="doc-row-head">
      <th scope="row">Early signs of selling today</th>
      <th scope="row">Early signs of buying today</th>
    </tr>
    <tr>
      <td>
        <ul>
          <li>Downtrend in premarket, below VWAP into the open</li>
          <li>Lost VWAP right before the open</li>
          <li>Tried to get back above VWAP and lost it right before the open</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Gap up and hold above VWAP, premarket mostly flat</li>
          <li><code>[reclaim vwap near premarket end]</code> — one dip below VWAP, then back above for the open</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Best Elements for Tradebooks
- [`Gap and Go`](../gap_and_go.md):
  - was consolidating on daily chart before the gap up
  - there was a key level from a previous key event
- [`Gap and Crap`](../gap_and_crap.md):
  - clear resistance from daily chart
  - large gap to create space for gap fill
  - clear buying from the recent rally

## Decision Table for Gap Down Stocks
<table>
  <tbody>
    <tr>
      <td scope="col"><strong>Gap down and go up</strong></td>
      <td scope="col"><strong>Gap down and go down</strong></td>
    </tr>
    <tr class="doc-row-head">
      <th scope="row">Gap to area with heavy support</th>
      <th scope="row">No major support from here</th>
    </tr>
    <tr>
      <td>
        <ul>
          <li><code>[near above support]</code> — obvious support line on the daily chart</li>
          <li><code>[near above key event level]</code> — level created by previous key events</li>
          <li><code>[near above zone]</code> — no single clear line, just a zone (can be choppy); pick a clear line within the zone</li>
        </ul>
      </td>
      <td>
        <ul>
          <li><code>[near below consolidation range]</code> or <code>[near below consolidation range top]</code></li>
          <li>
            <code>[buyers trapped]</code> — buyers entered above a level; gap down below traps them. Often easy to see on the daily chart.
            <ul>
              <li>If far below prior support, VWAP continuation can work — still respect VWAP and the high from the last VWAP pop.</li>
            </ul>
          </li>
          <li><code>[previous inside day]</code> — previous day inside the day before; gap near below the 2-day low</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Consideration Notes

- Gap and Crap: expect massive selling / profit taking from the open
- Gap and Go: expect very small profit taking and new buyers will come in soon after a shallow pullback
- Gap, Give and Go: expect some amount of profit taking from the open and buyers will come in later or at a lower price level to get a better deal