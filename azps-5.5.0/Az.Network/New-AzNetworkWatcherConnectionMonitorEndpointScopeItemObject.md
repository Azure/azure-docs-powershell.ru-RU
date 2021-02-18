---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218505"
---
# <span data-ttu-id="150d0-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="150d0-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="150d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="150d0-102">SYNOPSIS</span></span>
<span data-ttu-id="150d0-103">Создает элемент области действия для конечной точки монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="150d0-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="150d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="150d0-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="150d0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="150d0-105">DESCRIPTION</span></span>
<span data-ttu-id="150d0-106">С New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject создается элемент конечной точки.</span><span class="sxs-lookup"><span data-stu-id="150d0-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="150d0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="150d0-107">EXAMPLES</span></span>

### <span data-ttu-id="150d0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="150d0-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="150d0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="150d0-109">PARAMETERS</span></span>

### <span data-ttu-id="150d0-110">-Address</span><span class="sxs-lookup"><span data-stu-id="150d0-110">-Address</span></span>
<span data-ttu-id="150d0-111">Адрес элемента области.</span><span class="sxs-lookup"><span data-stu-id="150d0-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="150d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150d0-112">-DefaultProfile</span></span>
<span data-ttu-id="150d0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="150d0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="150d0-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="150d0-114">-Confirm</span></span>
<span data-ttu-id="150d0-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="150d0-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="150d0-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="150d0-116">-WhatIf</span></span>
<span data-ttu-id="150d0-117">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="150d0-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="150d0-118">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="150d0-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="150d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150d0-119">CommonParameters</span></span>
<span data-ttu-id="150d0-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150d0-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="150d0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150d0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="150d0-122">INPUTS</span></span>

### <span data-ttu-id="150d0-123">Нет</span><span class="sxs-lookup"><span data-stu-id="150d0-123">None</span></span>

## <span data-ttu-id="150d0-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="150d0-124">OUTPUTS</span></span>

### <span data-ttu-id="150d0-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="150d0-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="150d0-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="150d0-126">NOTES</span></span>

## <span data-ttu-id="150d0-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="150d0-127">RELATED LINKS</span></span>
