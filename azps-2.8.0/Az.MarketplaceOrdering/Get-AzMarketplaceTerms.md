---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 730861b055259fd0aee5490de2421abe96afc10b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720380"
---
# <span data-ttu-id="6439b-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="6439b-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="6439b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6439b-102">SYNOPSIS</span></span>
<span data-ttu-id="6439b-103">Получите условия соглашения для определенного кода издателя (издателя), идентификатора предложения (продукта) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="6439b-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="6439b-104">Объект условий, возвращаемый этой командой, должен быть передан в Set-AzMarketplaceTerms, чтобы принимать юридические условия.</span><span class="sxs-lookup"><span data-stu-id="6439b-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="6439b-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6439b-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6439b-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6439b-106">DESCRIPTION</span></span>
<span data-ttu-id="6439b-107">Командлет **Get-AzMarketplaceTerms** возвращает условия для данного идентификатора издателя (издателя), кода предложения ID (Product) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="6439b-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="6439b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6439b-108">EXAMPLES</span></span>

### <span data-ttu-id="6439b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6439b-109">Example 1</span></span>
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

## <span data-ttu-id="6439b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6439b-110">PARAMETERS</span></span>

### <span data-ttu-id="6439b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6439b-111">-DefaultProfile</span></span>
<span data-ttu-id="6439b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6439b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6439b-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6439b-113">-Name</span></span>
<span data-ttu-id="6439b-114">Строка идентификатора плана развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="6439b-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="6439b-115">-Product</span><span class="sxs-lookup"><span data-stu-id="6439b-115">-Product</span></span>
<span data-ttu-id="6439b-116">Строка идентификатора предложения с развернутым изображением.</span><span class="sxs-lookup"><span data-stu-id="6439b-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="6439b-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6439b-117">-Publisher</span></span>
<span data-ttu-id="6439b-118">Строка идентификатора издателя развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="6439b-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="6439b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6439b-119">CommonParameters</span></span>
<span data-ttu-id="6439b-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6439b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6439b-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6439b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6439b-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6439b-122">INPUTS</span></span>

### <span data-ttu-id="6439b-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="6439b-123">None</span></span>

## <span data-ttu-id="6439b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6439b-124">OUTPUTS</span></span>

### <span data-ttu-id="6439b-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="6439b-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="6439b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="6439b-126">NOTES</span></span>

## <span data-ttu-id="6439b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6439b-127">RELATED LINKS</span></span>
