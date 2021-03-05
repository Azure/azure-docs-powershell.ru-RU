---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: eb9865d69d51fffc7488379bada256a812503a24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981224"
---
# <span data-ttu-id="ba354-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="ba354-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="ba354-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba354-102">SYNOPSIS</span></span>
<span data-ttu-id="ba354-103">Возвращает доступные skus для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ba354-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="ba354-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba354-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba354-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba354-105">DESCRIPTION</span></span>
<span data-ttu-id="ba354-106">С **помощью cmdlet Get-AzCognitiveServicesAccountSku** можно получить доступную коды skKu для учетной записи Службы когнитивных функций.</span><span class="sxs-lookup"><span data-stu-id="ba354-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="ba354-107">SKU — это план уровня для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ba354-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="ba354-108">В нем определяются цена, ограничение и ставка для счета.</span><span class="sxs-lookup"><span data-stu-id="ba354-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="ba354-109">F0 SKU — это бесплатный уровень.</span><span class="sxs-lookup"><span data-stu-id="ba354-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="ba354-110">Платные уровни: S0, S1, S2 и другие.</span><span class="sxs-lookup"><span data-stu-id="ba354-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="ba354-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba354-111">EXAMPLES</span></span>

### <span data-ttu-id="ba354-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba354-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="ba354-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba354-113">PARAMETERS</span></span>

### <span data-ttu-id="ba354-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba354-114">-DefaultProfile</span></span>
<span data-ttu-id="ba354-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba354-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba354-116">-Location</span><span class="sxs-lookup"><span data-stu-id="ba354-116">-Location</span></span>
<span data-ttu-id="ba354-117">Расположение учетной записи службы когнитивных функций.</span><span class="sxs-lookup"><span data-stu-id="ba354-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="ba354-118">-Type</span><span class="sxs-lookup"><span data-stu-id="ba354-118">-Type</span></span>
<span data-ttu-id="ba354-119">Тип учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="ba354-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="ba354-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba354-120">CommonParameters</span></span>
<span data-ttu-id="ba354-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba354-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba354-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba354-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba354-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba354-123">INPUTS</span></span>

### <span data-ttu-id="ba354-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ba354-124">System.String</span></span>

## <span data-ttu-id="ba354-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba354-125">OUTPUTS</span></span>

### <span data-ttu-id="ba354-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="ba354-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="ba354-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba354-127">NOTES</span></span>

## <span data-ttu-id="ba354-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba354-128">RELATED LINKS</span></span>
