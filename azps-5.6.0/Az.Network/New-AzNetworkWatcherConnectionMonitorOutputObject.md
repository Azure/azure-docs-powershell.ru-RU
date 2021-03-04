---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 895659481999ab5801538bec3b88765e1d48aeca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958499"
---
# <span data-ttu-id="76a3e-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="76a3e-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="76a3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="76a3e-103">Создание объекта назначения для выводного монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="76a3e-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="76a3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76a3e-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a3e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="76a3e-106">С New-AzNetworkWatcherConnectionMonitorOutputObject создается объект назначения для выводного монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="76a3e-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="76a3e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76a3e-107">EXAMPLES</span></span>

### <span data-ttu-id="76a3e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76a3e-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="76a3e-109">Type : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="76a3e-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="76a3e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76a3e-110">PARAMETERS</span></span>

### <span data-ttu-id="76a3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a3e-111">-DefaultProfile</span></span>
<span data-ttu-id="76a3e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76a3e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a3e-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="76a3e-113">-OutputType</span></span>
<span data-ttu-id="76a3e-114">Тип вывода монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="76a3e-114">Connection monitor output destination type.</span></span> <span data-ttu-id="76a3e-115">В настоящее \" время поддерживается \" только workspace.</span><span class="sxs-lookup"><span data-stu-id="76a3e-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="76a3e-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="76a3e-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="76a3e-117">ИД ресурса рабочей области журнала аналитических данных.</span><span class="sxs-lookup"><span data-stu-id="76a3e-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="76a3e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76a3e-118">-Confirm</span></span>
<span data-ttu-id="76a3e-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="76a3e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a3e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a3e-120">-WhatIf</span></span>
<span data-ttu-id="76a3e-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76a3e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a3e-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76a3e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a3e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a3e-123">CommonParameters</span></span>
<span data-ttu-id="76a3e-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a3e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a3e-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76a3e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a3e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76a3e-126">INPUTS</span></span>

### <span data-ttu-id="76a3e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="76a3e-127">None</span></span>

## <span data-ttu-id="76a3e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76a3e-128">OUTPUTS</span></span>

### <span data-ttu-id="76a3e-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="76a3e-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="76a3e-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76a3e-130">NOTES</span></span>

## <span data-ttu-id="76a3e-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76a3e-131">RELATED LINKS</span></span>
