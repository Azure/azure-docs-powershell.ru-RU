---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: f3b641e3e9229706f3010e7db95480423b06361c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913615"
---
# <span data-ttu-id="939db-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="939db-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="939db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="939db-102">SYNOPSIS</span></span>
<span data-ttu-id="939db-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="939db-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="939db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="939db-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="939db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="939db-105">DESCRIPTION</span></span>
<span data-ttu-id="939db-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="939db-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="939db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="939db-107">EXAMPLES</span></span>

### <span data-ttu-id="939db-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="939db-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="939db-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="939db-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="939db-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="939db-110">PARAMETERS</span></span>

### <span data-ttu-id="939db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="939db-111">-DefaultProfile</span></span>
<span data-ttu-id="939db-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="939db-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="939db-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="939db-113">-Name</span></span>
<span data-ttu-id="939db-114">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="939db-114">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939db-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="939db-115">-RouteFilter</span></span>
<span data-ttu-id="939db-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="939db-116">The RouteFilter</span></span>

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

### <span data-ttu-id="939db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939db-117">CommonParameters</span></span>
<span data-ttu-id="939db-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="939db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939db-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="939db-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939db-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="939db-120">INPUTS</span></span>

### <span data-ttu-id="939db-121">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="939db-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="939db-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="939db-122">OUTPUTS</span></span>

### <span data-ttu-id="939db-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="939db-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="939db-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="939db-124">NOTES</span></span>

## <span data-ttu-id="939db-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="939db-125">RELATED LINKS</span></span>

