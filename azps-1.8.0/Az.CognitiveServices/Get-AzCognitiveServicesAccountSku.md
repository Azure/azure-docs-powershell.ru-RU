---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: d041d18713efa4d094a46747a9697eb76dcea578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901418"
---
# <span data-ttu-id="f0c0d-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="f0c0d-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="f0c0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c0d-103">Возвращает доступные SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="f0c0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0c0d-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0c0d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c0d-106">Командлет **Get-AzCognitiveServicesAccountSku** получает доступные SKU для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="f0c0d-107">SKU — это ярусный план для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="f0c0d-108">Она определяет цену, ограничение на звонки и ставку для счета.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="f0c0d-109">F0 SKU является бесплатным уровнем.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="f0c0d-110">Оплаченные уровни включают в себя S0, S1, S2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="f0c0d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0c0d-111">EXAMPLES</span></span>

### <span data-ttu-id="f0c0d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0c0d-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="f0c0d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0c0d-113">PARAMETERS</span></span>

### <span data-ttu-id="f0c0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c0d-114">-DefaultProfile</span></span>
<span data-ttu-id="f0c0d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f0c0d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0c0d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="f0c0d-116">-Location</span></span>
<span data-ttu-id="f0c0d-117">Расположение учетной записи для пересчета служб.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c0d-118">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f0c0d-118">-Type</span></span>
<span data-ttu-id="f0c0d-119">Тип учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c0d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c0d-120">CommonParameters</span></span>
<span data-ttu-id="f0c0d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0c0d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c0d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c0d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c0d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0c0d-123">INPUTS</span></span>

### <span data-ttu-id="f0c0d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c0d-124">System.String</span></span>

## <span data-ttu-id="f0c0d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0c0d-125">OUTPUTS</span></span>

### <span data-ttu-id="f0c0d-126">Microsoft. Azure. Management. CognitiveServices. Models. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="f0c0d-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="f0c0d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0c0d-127">NOTES</span></span>

## <span data-ttu-id="f0c0d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0c0d-128">RELATED LINKS</span></span>
