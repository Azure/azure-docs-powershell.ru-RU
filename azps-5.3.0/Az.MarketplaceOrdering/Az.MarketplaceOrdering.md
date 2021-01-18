---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507116"
---
# <span data-ttu-id="a7f85-101">Az.MarketplaceOrdering Module</span><span class="sxs-lookup"><span data-stu-id="a7f85-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="a7f85-102">Описание</span><span class="sxs-lookup"><span data-stu-id="a7f85-102">Description</span></span>
<span data-ttu-id="a7f85-103">В разделах этой статьи ются командылеты Azure PowerShell для azure MarketplaceOrdering в платформе Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="a7f85-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="a7f85-104">Командлеты существуют в области имен Microsoft.Azure.Commands.MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="a7f85-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="a7f85-105">Эти cmdlets позволяют пользователям Azure принимать юридические условия для marketplace, предлагающие дополнительное программное развертывание для этих решений.</span><span class="sxs-lookup"><span data-stu-id="a7f85-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="a7f85-106">Пользователи также могут отклонить набор уже принятых юридических условий.</span><span class="sxs-lookup"><span data-stu-id="a7f85-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="a7f85-107">Az.MarketplaceOrdering Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a7f85-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="a7f85-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a7f85-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="a7f85-109">Получите условия соглашения по заданным ид издателя(Publisher), предложению id(Product) и плану id(Name).</span><span class="sxs-lookup"><span data-stu-id="a7f85-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a7f85-110">Объект терминов, возвращаемый данной командой, передается в Set-AzMarketplaceTerms, чтобы принять юридические условия.</span><span class="sxs-lookup"><span data-stu-id="a7f85-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="a7f85-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a7f85-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="a7f85-112">Принятие и отклонение условий для заданного имени издателя (Publisher), предложения id(Product) и плана id(Name).</span><span class="sxs-lookup"><span data-stu-id="a7f85-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a7f85-113">Используйте Get-AzMarketplaceTerms, чтобы получить условия соглашения.</span><span class="sxs-lookup"><span data-stu-id="a7f85-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

