---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506691"
---
# <span data-ttu-id="612e6-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="612e6-101">Get-AzSignalR</span></span>

## <span data-ttu-id="612e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="612e6-102">SYNOPSIS</span></span>
<span data-ttu-id="612e6-103">Получите определенную службу SignalR или все службы SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="612e6-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="612e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="612e6-104">SYNTAX</span></span>

### <span data-ttu-id="612e6-105">ListSignalrServiceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="612e6-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="612e6-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="612e6-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="612e6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="612e6-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="612e6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="612e6-108">DESCRIPTION</span></span>
<span data-ttu-id="612e6-109">Получите определенную службу SignalR или все службы SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="612e6-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="612e6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="612e6-110">EXAMPLES</span></span>

### <span data-ttu-id="612e6-111">Получить все службы SignalR в подписке</span><span class="sxs-lookup"><span data-stu-id="612e6-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="612e6-112">Получить все службы SignalR в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="612e6-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="612e6-113">Получить определенную службу SignalR</span><span class="sxs-lookup"><span data-stu-id="612e6-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="612e6-114">Получить определенную службу SignalR из группы ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="612e6-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="612e6-115">Группу ресурсов по умолчанию может установить \` Set-AzDefault -ResourceGroupName myResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="612e6-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="612e6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="612e6-116">PARAMETERS</span></span>

### <span data-ttu-id="612e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612e6-117">-DefaultProfile</span></span>
<span data-ttu-id="612e6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="612e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="612e6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="612e6-119">-Name</span></span>
<span data-ttu-id="612e6-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="612e6-120">SignalR service name.</span></span>

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

### <span data-ttu-id="612e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="612e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="612e6-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="612e6-122">Resource group name.</span></span>

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

### <span data-ttu-id="612e6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="612e6-123">-ResourceId</span></span>
<span data-ttu-id="612e6-124">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="612e6-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="612e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612e6-125">CommonParameters</span></span>
<span data-ttu-id="612e6-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="612e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612e6-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="612e6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612e6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="612e6-128">INPUTS</span></span>

### <span data-ttu-id="612e6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="612e6-129">System.String</span></span>
## <span data-ttu-id="612e6-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="612e6-130">OUTPUTS</span></span>

### <span data-ttu-id="612e6-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="612e6-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="612e6-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="612e6-132">NOTES</span></span>

## <span data-ttu-id="612e6-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="612e6-133">RELATED LINKS</span></span>
