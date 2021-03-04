---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: e7287cff34420c7885f5cddef95e4ca3b09e881f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955507"
---
# <span data-ttu-id="1b646-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="1b646-101">Get-AzSignalR</span></span>

## <span data-ttu-id="1b646-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b646-102">SYNOPSIS</span></span>
<span data-ttu-id="1b646-103">Получите определенную службу SignalR или все службы SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="1b646-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="1b646-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b646-104">SYNTAX</span></span>

### <span data-ttu-id="1b646-105">ListSignalRServiceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b646-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b646-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b646-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b646-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b646-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b646-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b646-108">DESCRIPTION</span></span>
<span data-ttu-id="1b646-109">Получите определенную службу SignalR или все службы SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="1b646-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="1b646-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b646-110">EXAMPLES</span></span>

### <span data-ttu-id="1b646-111">Получить все службы SignalR в подписке</span><span class="sxs-lookup"><span data-stu-id="1b646-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="1b646-112">Получить все службы SignalR в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="1b646-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="1b646-113">Получить определенную службу SignalR</span><span class="sxs-lookup"><span data-stu-id="1b646-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="1b646-114">Получить определенную службу SignalR из группы ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1b646-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="1b646-115">Группу ресурсов по умолчанию может установить \` Set-AzDefault -ResourceGroupName myResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="1b646-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="1b646-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b646-116">PARAMETERS</span></span>

### <span data-ttu-id="1b646-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b646-117">-DefaultProfile</span></span>
<span data-ttu-id="1b646-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b646-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b646-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1b646-119">-Name</span></span>
<span data-ttu-id="1b646-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="1b646-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b646-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b646-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b646-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b646-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b646-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b646-123">-ResourceId</span></span>
<span data-ttu-id="1b646-124">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="1b646-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b646-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b646-125">CommonParameters</span></span>
<span data-ttu-id="1b646-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b646-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b646-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b646-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b646-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b646-128">INPUTS</span></span>

### <span data-ttu-id="1b646-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1b646-129">System.String</span></span>
## <span data-ttu-id="1b646-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b646-130">OUTPUTS</span></span>

### <span data-ttu-id="1b646-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="1b646-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="1b646-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b646-132">NOTES</span></span>

## <span data-ttu-id="1b646-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b646-133">RELATED LINKS</span></span>
