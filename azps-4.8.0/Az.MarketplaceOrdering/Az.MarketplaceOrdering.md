---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243516"
---
# <span data-ttu-id="4b976-101">AZ. MarketplaceOrdering Module</span><span class="sxs-lookup"><span data-stu-id="4b976-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="4b976-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="4b976-102">Description</span></span>
<span data-ttu-id="4b976-103">В этом разделе приведены командлеты PowerShell Azure для Azure MarketplaceOrdering в платформе диспетчера ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="4b976-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="4b976-104">Командлеты существуют в пространстве имен Microsoft. Azure. Commands. MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="4b976-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="4b976-105">Эти командлеты позволяют пользователям Azure принимать юридические условия для рынка, предоставляя более удобное программное развертывание для этих решений.</span><span class="sxs-lookup"><span data-stu-id="4b976-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="4b976-106">Пользователи также могут отклонить набор юридических слов, которые уже были приняты.</span><span class="sxs-lookup"><span data-stu-id="4b976-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="4b976-107">Командлеты AZ. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4b976-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="4b976-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="4b976-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="4b976-109">Получите условия соглашения для определенного кода издателя (издателя), идентификатора предложения (продукта) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="4b976-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="4b976-110">Объект условий, возвращаемый этой командой, должен быть передан в Set-AzMarketplaceTerms, чтобы принимать юридические условия.</span><span class="sxs-lookup"><span data-stu-id="4b976-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="4b976-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="4b976-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="4b976-112">Принять или отклонить условия для определенного идентификатора издателя (издателя), идентификатора предложения (продукта) и кода плана (имя).</span><span class="sxs-lookup"><span data-stu-id="4b976-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="4b976-113">Пожалуйста, используй Get-AzMarketplaceTerms, чтобы получить условия соглашения.</span><span class="sxs-lookup"><span data-stu-id="4b976-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>
