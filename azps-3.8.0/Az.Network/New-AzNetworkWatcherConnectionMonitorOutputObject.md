---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065490"
---
# <span data-ttu-id="e7dd8-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="e7dd8-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="e7dd8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e7dd8-103">Создание целевого объекта вывода монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="e7dd8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7dd8-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7dd8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="e7dd8-106">Командлет New-AzNetworkWatcherConnectionMonitorOutputObject создает объект назначения вывода монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="e7dd8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7dd8-107">EXAMPLES</span></span>

### <span data-ttu-id="e7dd8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7dd8-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="e7dd8-109">Тип: "Рабочая область" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="e7dd8-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="e7dd8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7dd8-110">PARAMETERS</span></span>

### <span data-ttu-id="e7dd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7dd8-111">-DefaultProfile</span></span>
<span data-ttu-id="e7dd8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7dd8-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="e7dd8-113">-OutputType</span></span>
<span data-ttu-id="e7dd8-114">Тип назначения выходных данных монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-114">Connection monitor output destination type.</span></span> <span data-ttu-id="e7dd8-115">В настоящее время \" поддерживается только Рабочая область \" .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="e7dd8-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e7dd8-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="e7dd8-117">Идентификатор ресурса рабочей области для аналитики журнала.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="e7dd8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7dd8-118">-Confirm</span></span>
<span data-ttu-id="e7dd8-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7dd8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7dd8-120">-WhatIf</span></span>
<span data-ttu-id="e7dd8-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7dd8-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7dd8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7dd8-123">CommonParameters</span></span>
<span data-ttu-id="e7dd8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7dd8-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7dd8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7dd8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7dd8-126">INPUTS</span></span>

### <span data-ttu-id="e7dd8-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="e7dd8-127">None</span></span>

## <span data-ttu-id="e7dd8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7dd8-128">OUTPUTS</span></span>

### <span data-ttu-id="e7dd8-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="e7dd8-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="e7dd8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7dd8-130">NOTES</span></span>

## <span data-ttu-id="e7dd8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7dd8-131">RELATED LINKS</span></span>
