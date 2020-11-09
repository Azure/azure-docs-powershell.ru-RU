---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316648"
---
# <span data-ttu-id="201c8-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="201c8-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="201c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="201c8-102">SYNOPSIS</span></span>
<span data-ttu-id="201c8-103">Создание элемента области с областью конечной точки монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="201c8-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="201c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="201c8-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="201c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="201c8-105">DESCRIPTION</span></span>
<span data-ttu-id="201c8-106">Командлет New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject создает элемент области действия конечной точки.</span><span class="sxs-lookup"><span data-stu-id="201c8-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="201c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="201c8-107">EXAMPLES</span></span>

### <span data-ttu-id="201c8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="201c8-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="201c8-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="201c8-109">PARAMETERS</span></span>

### <span data-ttu-id="201c8-110">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="201c8-110">-Address</span></span>
<span data-ttu-id="201c8-111">Адрес элемента области.</span><span class="sxs-lookup"><span data-stu-id="201c8-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="201c8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201c8-112">-DefaultProfile</span></span>
<span data-ttu-id="201c8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="201c8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="201c8-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="201c8-114">-Confirm</span></span>
<span data-ttu-id="201c8-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="201c8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="201c8-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="201c8-116">-WhatIf</span></span>
<span data-ttu-id="201c8-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="201c8-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="201c8-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="201c8-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="201c8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201c8-119">CommonParameters</span></span>
<span data-ttu-id="201c8-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="201c8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201c8-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="201c8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201c8-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="201c8-122">INPUTS</span></span>

### <span data-ttu-id="201c8-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="201c8-123">None</span></span>

## <span data-ttu-id="201c8-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="201c8-124">OUTPUTS</span></span>

### <span data-ttu-id="201c8-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="201c8-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="201c8-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="201c8-126">NOTES</span></span>

## <span data-ttu-id="201c8-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="201c8-127">RELATED LINKS</span></span>
