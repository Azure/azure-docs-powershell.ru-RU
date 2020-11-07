---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: 1ec2798f9da6d72cdf247a03c9c88029b5cc2081
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905253"
---
# <span data-ttu-id="6ed22-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="6ed22-101">Get-AzSignalR</span></span>

## <span data-ttu-id="6ed22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ed22-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed22-103">Получение определенной службы сигнала или всех служб SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="6ed22-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="6ed22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ed22-104">SYNTAX</span></span>

### <span data-ttu-id="6ed22-105">ListSignalRServiceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ed22-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ed22-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ed22-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ed22-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ed22-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ed22-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ed22-108">DESCRIPTION</span></span>
<span data-ttu-id="6ed22-109">Получение определенной службы сигнала или всех служб SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="6ed22-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="6ed22-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ed22-110">EXAMPLES</span></span>

### <span data-ttu-id="6ed22-111">Получение всех служб SignalR в подписке</span><span class="sxs-lookup"><span data-stu-id="6ed22-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="6ed22-112">Получение всех служб SignalR в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ed22-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="6ed22-113">Получение определенной службы сигнала</span><span class="sxs-lookup"><span data-stu-id="6ed22-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="6ed22-114">Получение специальных служб сигнала из группы ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6ed22-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="6ed22-115">Группа ресурсов по умолчанию может быть установлена с помощью \` Set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="6ed22-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="6ed22-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ed22-116">PARAMETERS</span></span>

### <span data-ttu-id="6ed22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed22-117">-DefaultProfile</span></span>
<span data-ttu-id="6ed22-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ed22-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6ed22-119">-Name</span></span>
<span data-ttu-id="6ed22-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="6ed22-120">SignalR service name.</span></span>

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

### <span data-ttu-id="6ed22-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ed22-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ed22-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ed22-122">Resource group name.</span></span>

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

### <span data-ttu-id="6ed22-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ed22-123">-ResourceId</span></span>
<span data-ttu-id="6ed22-124">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="6ed22-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="6ed22-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed22-125">CommonParameters</span></span>
<span data-ttu-id="6ed22-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ed22-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed22-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ed22-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed22-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ed22-128">INPUTS</span></span>

### <span data-ttu-id="6ed22-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6ed22-129">System.String</span></span>
## <span data-ttu-id="6ed22-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ed22-130">OUTPUTS</span></span>

### <span data-ttu-id="6ed22-131">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="6ed22-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="6ed22-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ed22-132">NOTES</span></span>

## <span data-ttu-id="6ed22-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ed22-133">RELATED LINKS</span></span>
