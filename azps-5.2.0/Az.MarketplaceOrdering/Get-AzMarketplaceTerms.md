---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391031"
---
# <span data-ttu-id="121c9-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="121c9-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="121c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121c9-102">SYNOPSIS</span></span>
<span data-ttu-id="121c9-103">Получите условия соглашения по заданным ид издателя(Publisher), предложению id(Product) и плану id(Name).</span><span class="sxs-lookup"><span data-stu-id="121c9-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="121c9-104">Объект терминов, возвращаемый данной командой, передается в Set-AzMarketplaceTerms, чтобы принять юридические условия.</span><span class="sxs-lookup"><span data-stu-id="121c9-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="121c9-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="121c9-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="121c9-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="121c9-106">DESCRIPTION</span></span>
<span data-ttu-id="121c9-107">**Cmdlet Get-AzMarketplaceTerms** возвращает условия для данного id издателя(Publisher), offer id(Product) и plan id(Name) tuple.</span><span class="sxs-lookup"><span data-stu-id="121c9-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="121c9-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="121c9-108">EXAMPLES</span></span>

### <span data-ttu-id="121c9-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="121c9-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="121c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="121c9-110">PARAMETERS</span></span>

### <span data-ttu-id="121c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121c9-111">-DefaultProfile</span></span>
<span data-ttu-id="121c9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="121c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121c9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="121c9-113">-Name</span></span>
<span data-ttu-id="121c9-114">Развертывается строка идентификатора плана.</span><span class="sxs-lookup"><span data-stu-id="121c9-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121c9-115">-Product</span><span class="sxs-lookup"><span data-stu-id="121c9-115">-Product</span></span>
<span data-ttu-id="121c9-116">Развертывается строка идентификатора предложения изображения.</span><span class="sxs-lookup"><span data-stu-id="121c9-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121c9-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="121c9-117">-Publisher</span></span>
<span data-ttu-id="121c9-118">Развертываемая строка идентификатора изображения в Publisher.</span><span class="sxs-lookup"><span data-stu-id="121c9-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121c9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121c9-119">CommonParameters</span></span>
<span data-ttu-id="121c9-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121c9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121c9-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="121c9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121c9-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="121c9-122">INPUTS</span></span>

### <span data-ttu-id="121c9-123">Нет</span><span class="sxs-lookup"><span data-stu-id="121c9-123">None</span></span>

## <span data-ttu-id="121c9-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="121c9-124">OUTPUTS</span></span>

### <span data-ttu-id="121c9-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="121c9-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="121c9-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="121c9-126">NOTES</span></span>

## <span data-ttu-id="121c9-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="121c9-127">RELATED LINKS</span></span>
