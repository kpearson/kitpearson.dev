<section class="py-20 px-6 bg-slate-50">
  <div class="max-w-4xl mx-auto">
    <div class="bg-white rounded-lg shadow-lg p-8 md:p-12 border-l-4 border-blue-600">
      <div class="mb-8">
        <div class="text-5xl font-bold text-blue-600 mb-2">$300 → $13</div>
        <div class="text-xl text-slate-600">per user, per month.</div>
      </div>

      <div class="prose prose-slate max-w-none space-y-4 text-lg leading-relaxed">
        <p>
          I built an AI application where users stayed for <strong>hours</strong> — not minutes. Long, complex conversations with real engagement. The kind of usage metrics founders dream about.
        </p>

        <p>Then the AWS bill arrived.</p>

        <p>
          Token usage was growing quadratically. Every message reprocessed the entire conversation history. My best customers — the ones getting the most value — were the most expensive to serve. The better the product performed, the shorter my runway became.
        </p>

        <p class="font-semibold text-slate-900">
          8 weeks of capital left. Growing user base. Costs accelerating.
        </p>

        <p>I rebuilt the entire context architecture:</p>

        <ul class="list-disc pl-6 space-y-2 text-base">
          <li>Multi-tier model strategy — cost-effective models for context curation, frontier models only where they matter</li>
          <li>Dynamic RAG with similarity search instead of brute-force history passing</li>
          <li>Hierarchical memory system replacing full conversation replay</li>
          <li>4K token caps with intelligent summarization</li>
          <li>Prompt restructuring that made caching actually reduce costs (it increased them by 20% initially)</li>
        </ul>

        <p class="font-semibold text-slate-900">
          Result: 96% cost reduction. 50% gross margins. Profitable unit economics.
        </p>

        <p>
          No degradation in user experience. Same hours-long sessions. Same engagement. The AI still "remembers" — it just doesn't reread everything every time.
        </p>

        <p class="text-base">
          The infrastructure runs on 15+ AWS services — ECS, Aurora with pgvector, ElastiCache, CloudFront, WAF, Bedrock — at 99.9% uptime. Total infrastructure cost: $2/user/month.
        </p>

        <p class="font-semibold text-slate-900">
          Most companies running production AI workloads have this same problem and don't know it yet. They built fast, shipped, and haven't looked at the bill. When they do, the math won't work.
        </p>

        <p class="text-xl font-semibold text-blue-600">
          I find the money they're wasting and fix the architecture that's causing it.
        </p>
      </div>
    </div>
  </div>
</section>
