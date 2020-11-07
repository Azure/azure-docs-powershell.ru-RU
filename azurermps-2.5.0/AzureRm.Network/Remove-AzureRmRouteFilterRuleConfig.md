---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914022"
---
# <span data-ttu-id="17352-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17352-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="17352-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17352-102">SYNOPSIS</span></span>
<span data-ttu-id="17352-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="17352-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17352-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17352-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17352-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17352-105">DESCRIPTION</span></span>
<span data-ttu-id="17352-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="17352-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="17352-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17352-107">EXAMPLES</span></span>

### <span data-ttu-id="17352-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17352-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="17352-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="17352-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="17352-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17352-110">PARAMETERS</span></span>

### <span data-ttu-id="17352-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17352-111">-DefaultProfile</span></span>
<span data-ttu-id="17352-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17352-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17352-113">-Force</span><span class="sxs-lookup"><span data-stu-id="17352-113">-Force</span></span>
<span data-ttu-id="17352-114">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="17352-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17352-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17352-115">-Name</span></span>
<span data-ttu-id="17352-116">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="17352-116">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17352-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="17352-117">-RouteFilter</span></span>
<span data-ttu-id="17352-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="17352-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17352-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17352-119">-Confirm</span></span>
<span data-ttu-id="17352-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17352-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17352-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17352-121">-WhatIf</span></span>
<span data-ttu-id="17352-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17352-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17352-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17352-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17352-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17352-124">CommonParameters</span></span>
<span data-ttu-id="17352-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17352-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17352-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17352-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17352-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17352-127">INPUTS</span></span>

### <span data-ttu-id="17352-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="17352-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="17352-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17352-129">OUTPUTS</span></span>

### <span data-ttu-id="17352-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="17352-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="17352-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="17352-131">NOTES</span></span>

## <span data-ttu-id="17352-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17352-132">RELATED LINKS</span></span>

