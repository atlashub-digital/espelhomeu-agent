# EspelhoMeu Tool Contracts

These are logical contracts. Concrete API/MCP implementations may vary.

## 1. Content

### content.list_publications
Input:
- contact/user context
- optional entitlement filter

Output:
- publication refs
- title
- type
- access state
- preview state

### content.resolve_unit
Input:
- product_ref
- unit_ref

Output:
- authorized content projection only

Never return full protected content to unauthorized context.

### content.get_sample
Input:
- product_ref

Output:
- approved public/sample projection

---

## 2. Progress

### progress.get
Input:
- user_ref
- product_ref

### progress.start
Input:
- user_ref
- product_ref

### progress.complete_unit
Input:
- user_ref
- product_ref
- unit_ref
- idempotency_key

### progress.pause
### progress.resume

Progress tools must be idempotent where relevant.

---

## 3. Memory

### memory.read_relevant
Input:
- user_ref
- intent
- allowed_classes

Returns minimum relevant entries.

### memory.save
Input:
- class
- key
- value
- consent_scope
- source
- retention policy

Reject forbidden inferred memory.

### memory.delete
### memory.correct

---

## 4. Images

### image.analyze_current
Does not imply storage.

### image.save_evolution
Requires:
- authenticated owner/contact mapping;
- images.store consent;
- private storage.

### image.list_evolution
Returns authorized private image refs.

### image.delete_evolution

### image.compare
Accept only user-authorized image refs.

---

## 5. Commerce

### commerce.list_offers
Returns active backend-defined offers.

### commerce.get_offer
### commerce.start_checkout
### commerce.get_order_status

Agent cannot directly grant entitlement.

---

## 6. Entitlements

### entitlement.resolve
Backend authority.

Input:
- user/contact ref

Output:
- entitlement refs
- expiry where applicable

No LLM decision.

---

## 7. Consent

### consent.get
### consent.grant
### consent.revoke

Consent changes should be explicit and auditable.

---

## 8. Handoff

### handoff.request
Input:
- category
- concise summary
- urgency
- minimal required refs

### handoff.status
### handoff.resume_ai

---

## 9. Community

### community.get_context
Returns only public/group-safe context.

### community.publish_scheduled
Must use approved content and cadence.

### community.moderation_signal
Creates moderation event; does not expose private memory.

---

## 10. Audit

Tool calls should emit:
- correlation id;
- tenant;
- conversation id;
- tool name;
- outcome;
- latency;
- policy decision metadata.

Do not include unnecessary sensitive payloads in logs.
