---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/get-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: f23912ed21105015e69b94b27c5c5cc7899ed044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560135"
---
# <span data-ttu-id="0d60e-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="0d60e-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="0d60e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d60e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d60e-103">Получите условия соглашения для определенного кода издателя (издателя), идентификатора предложения (продукта) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="0d60e-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="0d60e-104">Объект условий, возвращаемый этой командой, должен быть передан в Set-AzureRmMarketplaceTerms, чтобы принимать юридические условия.</span><span class="sxs-lookup"><span data-stu-id="0d60e-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d60e-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d60e-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d60e-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d60e-106">DESCRIPTION</span></span>
<span data-ttu-id="0d60e-107">Командлет **Get-AzureRmMarketplaceTerms** возвращает условия для данного идентификатора издателя (издателя), кода предложения ID (Product) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="0d60e-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="0d60e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d60e-108">EXAMPLES</span></span>

### <span data-ttu-id="0d60e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d60e-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="0d60e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d60e-110">PARAMETERS</span></span>

### <span data-ttu-id="0d60e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d60e-111">-DefaultProfile</span></span>
<span data-ttu-id="0d60e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d60e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d60e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d60e-113">-Name</span></span>
<span data-ttu-id="0d60e-114">Строка идентификатора плана развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="0d60e-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="0d60e-115">-Product</span><span class="sxs-lookup"><span data-stu-id="0d60e-115">-Product</span></span>
<span data-ttu-id="0d60e-116">Строка идентификатора предложения с развернутым изображением.</span><span class="sxs-lookup"><span data-stu-id="0d60e-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="0d60e-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0d60e-117">-Publisher</span></span>
<span data-ttu-id="0d60e-118">Строка идентификатора издателя развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="0d60e-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="0d60e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d60e-119">CommonParameters</span></span>
<span data-ttu-id="0d60e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d60e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d60e-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d60e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d60e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d60e-122">INPUTS</span></span>

### <span data-ttu-id="0d60e-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="0d60e-123">None</span></span>

## <span data-ttu-id="0d60e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d60e-124">OUTPUTS</span></span>

### <span data-ttu-id="0d60e-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="0d60e-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="0d60e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d60e-126">NOTES</span></span>

## <span data-ttu-id="0d60e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d60e-127">RELATED LINKS</span></span>
