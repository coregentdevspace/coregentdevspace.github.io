---
title: "Getting started: Backlog Hygiene for Jira"
permalink: /backlog-hygiene/docs
---

# Getting started with Backlog Hygiene for Jira

Backlog Hygiene sweeps your Jira backlog and suggests:
- duplicates to merge;
- obsolete work items to close (made moot by work already done);
- stale, low-value items to close.

You review each suggestion and approve or reject it. **Nothing changes in Jira until you approve.**


---

## 1. Who can do what

| Action | Who |
|---|---|
| Open the **Backlog Hygiene** page and read the review queue | Anyone who can open the page in Jira |
| **Run sweep now**, **Resume sweep**, **Approve**, **Reject**, change **Sweep settings** and **Close settings** | **Jira administrators** only |

Changes approved in the queue are made by the app (shown as the app user in Jira history). The comment it adds says the change was approved.

## 2. First-time setup (about 2 minutes)

1. In Jira, open **Apps → Backlog Hygiene**.
2. Next to **Sweep settings**, select **Show**.
3. Under **Projects to sweep**, choose the projects to clean up. The app can only see projects it has access to.
4. Check the defaults and change them if you like:
   - **Stale after (days without activity):** 180. Open items with no activity for this long are checked for staleness (30–1095).
   - **Run the sweep automatically every week:** on.
   - **Weekly run day (UTC):** Monday.
   - **Show suggestions from confidence:** 70%. Lower-confidence suggestions are hidden; the page tells you how many.
5. Select **Save sweep settings**.
6. Optional: next to **Close settings**, select **Show** to choose how approved changes close items in each project (see section 5).

## 3. Your first sweep

Select **Run sweep now**. The sweep runs in the background, so you can leave the page. The **Latest sweep** box shows what it's doing:
- **Reading work items**;
- **Summarising items**, with a progress bar;
- **Finding candidates**;
- **Judging candidates**, with a progress bar;
- **Finished**.

**How long it takes:** the first sweep reads and judges everything. Atlassian limits how fast an app can use AI, so expect roughly:

| Open work items | First sweep |
|---|---|
| 300 | under an hour |
| 3,000 | about 2–3 hours |

**Later sweeps are much faster.** They only re-check items that changed since the last sweep. A typical week takes minutes.

**During the free trial**, a sweep covers your **500 most recently active open items**. The page shows **Trial sweep: a sample of your backlog**. After purchase, the next sweep covers the whole backlog.

**If a sweep stops** (for example after a platform interruption), the page shows a warning with a **Resume sweep** button. Resuming continues where it stopped and keeps the work already done. A sweep with no progress for 20 minutes counts as stopped. The daily check also resumes stopped sweeps automatically, up to three times.

## 4. Reviewing the queue

The **Review queue** lists the suggestions from the latest finished sweep, highest confidence first. Each row shows:
- **Suggestion:** what to do, and the items involved, with links.
  - **Merge duplicate (close the second, keep the first):** both items describe the same problem or request. The first item is kept; the second is closed.
  - **Close as obsolete:** the item was made moot by work already done. The row names the item that superseded it, if any.
  - **Close as stale:** old, no recent activity, little value left.
- **Why:** the reason, and for merges any details from the duplicate that will be carried over.
- **Confidence.**
- **Decision:** **Approve** and **Reject**, or the outcome: **To review**, **Applied**, **Rejected**, **Failed**.

**What Approve does:**

| Suggestion | Changes in Jira |
|---|---|
| Merge duplicate | Links the closed item as **duplicates** the kept item. Adds a comment on the kept item with the reason and the details carried over, and a comment on the closed item. Closes the duplicate (see section 5). |
| Close as obsolete / stale | Links it to the item that superseded it (if any), adds a comment with the reason, and closes it. |

**What Reject does:** hides the suggestion permanently. It won't be suggested again in later sweeps.

If an approval shows **Failed**, the reason is shown in the row. Some steps may already have happened (for example the link); check the item and approve again or finish it by hand.

## 5. Close settings: fitting your workflows

Workflows differ between projects, so each project has its own close settings (under **Close settings → Show**):

- **Close to status:** the Done status to move items to. **Automatic (first Done status)** uses the first transition into a Done-category status.
- **Resolution: Duplicates (merge)**, **Resolution: Obsolete / superseded**, **Resolution: Stale, low value:** the resolution to set for each kind of close. Defaults: Duplicate, Won't Do, Won't Do. You can also choose **Don't set a resolution**.
- **If the workflow cannot set the resolution, add a label…:** many workflows have no resolution screen on their Done transition, so a resolution can't be set when closing. With this on, the app adds a label instead: `hygiene-duplicate`, `hygiene-obsolete` or `hygiene-stale`.

Select **Save** for each project you change.

**Finding everything the app closed** (JQL):

```
labels in (hygiene-duplicate, hygiene-obsolete, hygiene-stale)
```

or, where the resolution could be set:

```
resolution in (Duplicate, "Won't Do") AND comment ~ "Backlog Hygiene"
```

## 6. Weekly sweeps

With **Run the sweep automatically every week** on, the app checks once a day and runs a sweep on your **Weekly run day (UTC)**. If a sweep already ran in the last 6 days, or one is still running, it waits. Turn it off to sweep only when you select **Run sweep now**.

## 7. FAQ

**Does it use our Rovo credits?**
No. The app uses AI through Atlassian's Forge platform, and the vendor pays for that usage.

**Where does our data go?**
Nowhere outside Atlassian. The app runs entirely on Atlassian Forge ("Runs on Atlassian") and has no servers of its own. See the [privacy policy](privacy) for what it reads and stores, and for how long.

**Can it change items without asking?**
No. Every change needs a Jira administrator to select **Approve**.

**Why don't I see some suggestions?**
Suggestions below **Show suggestions from confidence** are hidden; the page says how many. Rejected suggestions are hidden permanently. The queue shows only the latest finished sweep.

**It suggested something wrong. What should I do?**
Select **Reject**. That suggestion won't come back.

**Which items does it look at?**
Open items in the selected projects, plus done items updated in the last 12 months (used to recognise items made obsolete by finished work). It doesn't read attachments or user profiles.

**Can I undo an approval?**
Not with one click. Reopen the item in Jira, and remove the link and the `hygiene-*` label if they were added. The app's comment records what it did.

## 8. Support

Email coregent.devspace+support@gmail.com: include your Jira site URL and, if relevant, the time of the sweep or the item keys.
