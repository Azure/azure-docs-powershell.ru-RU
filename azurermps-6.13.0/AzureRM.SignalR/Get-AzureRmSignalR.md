---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565347"
---
# <span data-ttu-id="57c7f-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="57c7f-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="57c7f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="57c7f-103">Получение определенной службы сигнала или всех служб SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="57c7f-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57c7f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57c7f-104">SYNTAX</span></span>

### <span data-ttu-id="57c7f-105">ListSignalRServiceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57c7f-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57c7f-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c7f-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57c7f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c7f-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57c7f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="57c7f-109">Получение определенной службы сигнала или всех служб SignalR в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="57c7f-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="57c7f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57c7f-110">EXAMPLES</span></span>

### <span data-ttu-id="57c7f-111">Получение всех служб SignalR в подписке</span><span class="sxs-lookup"><span data-stu-id="57c7f-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="57c7f-112">Получение всех служб SignalR в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="57c7f-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="57c7f-113">Получение определенной службы сигнала</span><span class="sxs-lookup"><span data-stu-id="57c7f-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="57c7f-114">Получение специальных служб сигнала из группы ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="57c7f-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="57c7f-115">Группа ресурсов по умолчанию может быть настроена `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="57c7f-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="57c7f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57c7f-116">PARAMETERS</span></span>

### <span data-ttu-id="57c7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c7f-117">-DefaultProfile</span></span>
<span data-ttu-id="57c7f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57c7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c7f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57c7f-119">-Name</span></span>
<span data-ttu-id="57c7f-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="57c7f-120">SignalR service name.</span></span>

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

### <span data-ttu-id="57c7f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c7f-121">-ResourceGroupName</span></span>
<span data-ttu-id="57c7f-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57c7f-122">Resource group name.</span></span>

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

### <span data-ttu-id="57c7f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57c7f-123">-ResourceId</span></span>
<span data-ttu-id="57c7f-124">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="57c7f-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="57c7f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c7f-125">CommonParameters</span></span>
<span data-ttu-id="57c7f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57c7f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c7f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c7f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c7f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57c7f-128">INPUTS</span></span>

### <span data-ttu-id="57c7f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="57c7f-129">System.String</span></span>
<span data-ttu-id="57c7f-130">Параметры: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57c7f-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="57c7f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57c7f-131">OUTPUTS</span></span>

### <span data-ttu-id="57c7f-132">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="57c7f-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="57c7f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="57c7f-133">NOTES</span></span>

## <span data-ttu-id="57c7f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57c7f-134">RELATED LINKS</span></span>
