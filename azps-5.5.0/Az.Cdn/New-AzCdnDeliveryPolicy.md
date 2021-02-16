---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211948"
---
# <span data-ttu-id="0c050-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="0c050-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="0c050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c050-102">SYNOPSIS</span></span>
<span data-ttu-id="0c050-103">Создает политику доставки.</span><span class="sxs-lookup"><span data-stu-id="0c050-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="0c050-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c050-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c050-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c050-105">DESCRIPTION</span></span>
<span data-ttu-id="0c050-106">Для создания конечной точки CDN создается политика доставки точки **New-AzCdnDeliveryPolicy.**</span><span class="sxs-lookup"><span data-stu-id="0c050-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="0c050-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c050-107">EXAMPLES</span></span>

### <span data-ttu-id="0c050-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c050-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="0c050-109">Создание образца политики доставки</span><span class="sxs-lookup"><span data-stu-id="0c050-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="0c050-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c050-110">PARAMETERS</span></span>

### <span data-ttu-id="0c050-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c050-111">-DefaultProfile</span></span>
<span data-ttu-id="0c050-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c050-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c050-113">-Description</span><span class="sxs-lookup"><span data-stu-id="0c050-113">-Description</span></span>
<span data-ttu-id="0c050-114">Описание политики</span><span class="sxs-lookup"><span data-stu-id="0c050-114">Description of the policy</span></span>

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

### <span data-ttu-id="0c050-115">-Правило</span><span class="sxs-lookup"><span data-stu-id="0c050-115">-Rule</span></span>
<span data-ttu-id="0c050-116">Списокrules о доставке.</span><span class="sxs-lookup"><span data-stu-id="0c050-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="0c050-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c050-117">CommonParameters</span></span>
<span data-ttu-id="0c050-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c050-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c050-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c050-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c050-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c050-120">INPUTS</span></span>

### <span data-ttu-id="0c050-121">Нет</span><span class="sxs-lookup"><span data-stu-id="0c050-121">None</span></span>

## <span data-ttu-id="0c050-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c050-122">OUTPUTS</span></span>

### <span data-ttu-id="0c050-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="0c050-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="0c050-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c050-124">NOTES</span></span>

## <span data-ttu-id="0c050-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c050-125">RELATED LINKS</span></span>
