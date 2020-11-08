---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236245"
---
# <span data-ttu-id="98a36-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="98a36-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="98a36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98a36-102">SYNOPSIS</span></span>
<span data-ttu-id="98a36-103">Создание политики доставки.</span><span class="sxs-lookup"><span data-stu-id="98a36-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="98a36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98a36-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a36-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98a36-105">DESCRIPTION</span></span>
<span data-ttu-id="98a36-106">Командлет **New-AzCdnDeliveryPolicy** создает политику доставки для создания КОНЕЧНОЙ точки CDN.</span><span class="sxs-lookup"><span data-stu-id="98a36-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="98a36-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98a36-107">EXAMPLES</span></span>

### <span data-ttu-id="98a36-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98a36-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="98a36-109">Создание образца политики доставки</span><span class="sxs-lookup"><span data-stu-id="98a36-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="98a36-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98a36-110">PARAMETERS</span></span>

### <span data-ttu-id="98a36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a36-111">-DefaultProfile</span></span>
<span data-ttu-id="98a36-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98a36-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98a36-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="98a36-113">-Description</span></span>
<span data-ttu-id="98a36-114">Описание политики</span><span class="sxs-lookup"><span data-stu-id="98a36-114">Description of the policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a36-115">-Правило</span><span class="sxs-lookup"><span data-stu-id="98a36-115">-Rule</span></span>
<span data-ttu-id="98a36-116">Список deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="98a36-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a36-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a36-117">CommonParameters</span></span>
<span data-ttu-id="98a36-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98a36-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a36-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98a36-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a36-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98a36-120">INPUTS</span></span>

### <span data-ttu-id="98a36-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="98a36-121">None</span></span>

## <span data-ttu-id="98a36-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98a36-122">OUTPUTS</span></span>

### <span data-ttu-id="98a36-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="98a36-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="98a36-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="98a36-124">NOTES</span></span>

## <span data-ttu-id="98a36-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98a36-125">RELATED LINKS</span></span>
