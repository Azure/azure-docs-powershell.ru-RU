---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243001"
---
# <span data-ttu-id="5a3bd-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="5a3bd-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="5a3bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3bd-103">Создание целевого объекта вывода монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="5a3bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a3bd-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a3bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a3bd-105">DESCRIPTION</span></span>
<span data-ttu-id="5a3bd-106">Командлет New-AzNetworkWatcherConnectionMonitorOutputObject создает объект назначения вывода монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="5a3bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a3bd-107">EXAMPLES</span></span>

### <span data-ttu-id="5a3bd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a3bd-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="5a3bd-109">Тип: "Рабочая область" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="5a3bd-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="5a3bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a3bd-110">PARAMETERS</span></span>

### <span data-ttu-id="5a3bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a3bd-111">-DefaultProfile</span></span>
<span data-ttu-id="5a3bd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a3bd-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="5a3bd-113">-OutputType</span></span>
<span data-ttu-id="5a3bd-114">Тип назначения выходных данных монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-114">Connection monitor output destination type.</span></span> <span data-ttu-id="5a3bd-115">В настоящее время \" поддерживается только Рабочая область \" .</span><span class="sxs-lookup"><span data-stu-id="5a3bd-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="5a3bd-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="5a3bd-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="5a3bd-117">Идентификатор ресурса рабочей области для аналитики журнала.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="5a3bd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a3bd-118">-Confirm</span></span>
<span data-ttu-id="5a3bd-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a3bd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a3bd-120">-WhatIf</span></span>
<span data-ttu-id="5a3bd-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a3bd-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a3bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3bd-123">CommonParameters</span></span>
<span data-ttu-id="5a3bd-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a3bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3bd-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a3bd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3bd-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a3bd-126">INPUTS</span></span>

### <span data-ttu-id="5a3bd-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="5a3bd-127">None</span></span>

## <span data-ttu-id="5a3bd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a3bd-128">OUTPUTS</span></span>

### <span data-ttu-id="5a3bd-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="5a3bd-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="5a3bd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a3bd-130">NOTES</span></span>

## <span data-ttu-id="5a3bd-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a3bd-131">RELATED LINKS</span></span>
