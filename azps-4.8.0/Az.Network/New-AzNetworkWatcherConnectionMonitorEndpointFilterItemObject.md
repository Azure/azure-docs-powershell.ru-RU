---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078901"
---
# <span data-ttu-id="b1c83-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="b1c83-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="b1c83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1c83-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c83-103">Создание элемента фильтра конечной точки монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="b1c83-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="b1c83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1c83-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c83-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1c83-105">DESCRIPTION</span></span>
<span data-ttu-id="b1c83-106">Командлет New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject создает элемент фильтра конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b1c83-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="b1c83-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1c83-107">EXAMPLES</span></span>

### <span data-ttu-id="b1c83-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1c83-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="b1c83-109">Тип: AgentAddress адрес: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="b1c83-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="b1c83-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1c83-110">PARAMETERS</span></span>

### <span data-ttu-id="b1c83-111">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="b1c83-111">-Address</span></span>
<span data-ttu-id="b1c83-112">Адрес элемента фильтра.</span><span class="sxs-lookup"><span data-stu-id="b1c83-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="b1c83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c83-113">-DefaultProfile</span></span>
<span data-ttu-id="b1c83-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c83-115">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="b1c83-115">-Type</span></span>
<span data-ttu-id="b1c83-116">Тип элемента, включенного в фильтр.</span><span class="sxs-lookup"><span data-stu-id="b1c83-116">The type of item included in the filter.</span></span> <span data-ttu-id="b1c83-117">В настоящее время поддерживается только "AgentAddress".</span><span class="sxs-lookup"><span data-stu-id="b1c83-117">Currently only 'AgentAddress' is supported.</span></span>

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

### <span data-ttu-id="b1c83-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1c83-118">-Confirm</span></span>
<span data-ttu-id="b1c83-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1c83-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c83-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c83-120">-WhatIf</span></span>
<span data-ttu-id="b1c83-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1c83-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c83-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1c83-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c83-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c83-123">CommonParameters</span></span>
<span data-ttu-id="b1c83-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1c83-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c83-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1c83-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c83-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1c83-126">INPUTS</span></span>

### <span data-ttu-id="b1c83-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="b1c83-127">None</span></span>

## <span data-ttu-id="b1c83-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1c83-128">OUTPUTS</span></span>

### <span data-ttu-id="b1c83-129">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="b1c83-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="b1c83-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1c83-130">NOTES</span></span>

## <span data-ttu-id="b1c83-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1c83-131">RELATED LINKS</span></span>