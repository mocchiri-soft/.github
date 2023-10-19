# 脱PoC！閉域化対応ChatGPTアプリの本番構築で考えること
## 文章中に出てきたリンク
 * Azure OpenAIサービスの透明性ノート<br>
   https://learn.microsoft.com/en-us/legal/cognitive-services/openai/transparency-note

 * Azure OpenAIサービスの行動規範<br>
   https://learn.microsoft.com/en-us/legal/cognitive-services/openai/code-of-conduct

 * Private Endpoint - プライベートリンクリソース<br>
   https://learn.microsoft.com/ja-jp/azure/private-link/private-endpoint-overview#private-link-resource

 * VNet Integration / 仮想ネットワークにデプロイできるサービス<br>
   https://learn.microsoft.com/ja-jp/azure/virtual-network/virtual-network-for-azure-services#services-that-can-be-deployed-into-a-virtual-network

 * Announcing Public Preview of Azure API Management Basic v2 and Standard v2 Tiers<br>
    https://techcommunity.microsoft.com/t5/azure-integration-services-blog/announcing-public-preview-of-azure-api-management-basic-v2-and/ba-p/3950830

 * Azure Private EndpointのためのDNS構成パターン<br>
    https://qiita.com/Isato-Hiyama/items/6c61a65f12c9e7042bb2

 * Azure Open AIのプロンプトをノーコードで監視したい！<br>
   https://zenn.dev/microsoft/articles/azure-openai-nocode-logging

 * Azure OpenAI Serviceの死活監視は可能なのか<br>
   https://logico-jp.io/2023/09/27/is-it-possible-to-check-if-azure-openai-service-is-healthy/

 * Azure OpenAI Service の クォータ管理<br>
   https://zenn.dev/microsoft/articles/be24a299f46a4d

 * Azure OpenAI Serviceへの負荷分散<br>
   https://logico-jp.io/2023/06/08/request-load-balancing-for-azure-openai-service/

 * Load Balancing in Azure OpenAI Service(英語)<br>
   https://journeyofthegeek.com/2023/05/31/load-balancing-in-azure-openai-service/

 * Generative AI for Developers: Exploring New Tools and APIs in Azure OpenAI Service<br>
   https://techcommunity.microsoft.com/t5/azure-ai-services-blog/generative-ai-for-developers-exploring-new-tools-and-apis-in/ba-p/3817003

 * Azure OpenAI ServiceからのHTTPステータスに応じて、Azure API Managementで再試行したりフォールバックしたりしたい<br>
   https://logico-jp.io/2023/08/02/use-azure-api-management-policies-to-retry-and-fallback-azure-openai-service-based-on-http-status/

 * Power Platform から VNet を使用して Azure OpenAI へ通信する<br>
   https://qiita.com/Takashi_Masumori/items/a2c716c8529aca9993ef

 * azure-search-openai-demo<br>
   https://github.com/Azure-Samples/azure-search-openai-demo/

 * Azure アプリケーションの 10 の設計原則<br>
   https://learn.microsoft.com/ja-jp/azure/architecture/guide/design-principles/

 * Azure OpenAI Serviceの日本語記事まとめ<br>
    https://zenn.dev/microsoft/articles/azure-openai-japanese-blogs

 * Azureアーキテクチャセンター<br>
    https://learn.microsoft.com/ja-jp/azure/architecture/browse/


## 脚注リンク
- *1 https://qiita.com/lazy-kz/items/32e8e7c86bdce67beb48
- *2 https://xtech.nikkei.com/atcl/nxt/news/18/15476/
- *3 https://www.youtube.com/watch?v=ebls5x-gb0s
- *4 https://learn.microsoft.com/ja-jp/azure/architecture/guide/technology-choices/compute-decision-tree
- *5 https://learn.microsoft.com/ja-jp/azure/architecture/guide/technology-choices/data-store-decision-tree
- *6 https://learn.microsoft.com/ja-jp/azure/architecture/reference-architectures/hybrid-networking/hub-spoke
- *7 https://learn.microsoft.com/ja-jp/azure/virtual-network/virtual-network-manage-peering?tabs=peering-portal#requirements-and-constraints
- *8 https://learn.microsoft.com/ja-jp/azure/security/fundamentals/shared-responsibility
- *9 https://jpazpaas.github.io/blog/2023/05/10/Appservice-components.html
- *10 https://learn.microsoft.com/ja-jp/azure/virtual-network/what-is-ip-address-168-63-129-16
- *11 https://learn.microsoft.com/ja-jp/azure/private-link/private-endpoint-dns#on-premises-workloads-using-a-dns-forwarder
- *12 https://learn.microsoft.com/ja-jp/azure/private-link/private-endpoint-dns#on-premises-workloads-using-a-dns-forwarder
- *13 https://learn.microsoft.com/en-us/azure/dns/dns-private-resolver-overview
- *14 https://docs.github.com/ja/actions/hosting-your-own-runners/managing-self-hosted-runners/about-self-hosted-runners
- *15 https://learn.microsoft.com/ja-jp/azure/devops/pipelines/agents/agents?view=azure-devops&tabs=yaml%2Cbrowser#communication-with-azure-pipelines
- *16 https://docs.github.com/ja/enterprise-server@3.9/admin/configuration/configuring-network-settings/configuring-built-in-firewall-rules
- *17 https://learn.microsoft.com/ja-jp/azure/devops/organizations/security/allow-list-ip-url
- *18 https://learn.microsoft.com/ja-jp/azure/ai-services/openai/how-to/quota?tabs=rest#introduction-to-quota
- *19 https://learn.microsoft.com/ja-jp/azure/ai-services/openai/quotas-limits#regional-quota-limits
- *20 https://learn.microsoft.com/ja-jp/azure/ai-services/openai/how-to/quota?tabs=rest#introduction-to-quota
- *21 https://learn.microsoft.com/ja-jp/azure/ai-services/openai/quotas-limits#how-to-request-increases-to-the-default-quotas-and-limits
- *22 https://learn.microsoft.com/ja-jp/azure/architecture/guide/technology-choices/load-balancing-overview
- *23 https://logico-jp.io/2023/09/27/is-it-possible-to-check-if-azure-openai-service-is-healthy/
- *24 https://jpazpaas.github.io/blog/2023/05/11/what-is-appserviceauthentication.html
- *25 https://learn.microsoft.com/ja-jp/azure/api-management/validate-azure-ad-token-policy