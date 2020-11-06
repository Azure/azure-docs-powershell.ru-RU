---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d5acd58d9b36e3a581ec025b06e256652a9c4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560299"
---
# <span data-ttu-id="30dfc-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30dfc-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="30dfc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="30dfc-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="30dfc-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30dfc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30dfc-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30dfc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="30dfc-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="30dfc-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="30dfc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="30dfc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30dfc-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="30dfc-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="30dfc-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="30dfc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="30dfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30dfc-111">-DefaultProfile</span></span>
<span data-ttu-id="30dfc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30dfc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30dfc-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30dfc-113">-Name</span></span>
<span data-ttu-id="30dfc-114">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="30dfc-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="30dfc-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="30dfc-115">-RouteFilter</span></span>
<span data-ttu-id="30dfc-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="30dfc-116">The RouteFilter</span></span>

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

### <span data-ttu-id="30dfc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30dfc-117">CommonParameters</span></span>
<span data-ttu-id="30dfc-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30dfc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30dfc-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30dfc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30dfc-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30dfc-120">INPUTS</span></span>

### <span data-ttu-id="30dfc-121">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="30dfc-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="30dfc-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30dfc-122">OUTPUTS</span></span>

### <span data-ttu-id="30dfc-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="30dfc-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="30dfc-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="30dfc-124">NOTES</span></span>

## <span data-ttu-id="30dfc-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30dfc-125">RELATED LINKS</span></span>

