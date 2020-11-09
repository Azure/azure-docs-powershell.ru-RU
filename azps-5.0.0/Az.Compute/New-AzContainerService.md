---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246791"
---
# <span data-ttu-id="63163-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="63163-101">New-AzContainerService</span></span>

## <span data-ttu-id="63163-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63163-102">SYNOPSIS</span></span>
<span data-ttu-id="63163-103">Создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="63163-103">Creates a container service.</span></span>

## <span data-ttu-id="63163-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63163-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63163-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63163-105">DESCRIPTION</span></span>
<span data-ttu-id="63163-106">Командлет **New-AzContainerService** создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="63163-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="63163-107">Укажите объект службы контейнера, который можно создать с помощью командлета New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="63163-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="63163-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63163-108">EXAMPLES</span></span>

### <span data-ttu-id="63163-109">Пример 1: создание службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="63163-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="63163-110">Первая команда создает группу ресурсов с именем ResourceGroup17 в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="63163-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="63163-111">Дополнительные сведения можно найти в командлетах New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="63163-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="63163-112">Вторая команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="63163-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="63163-113">Дополнительные сведения можно найти в командлетах New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="63163-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="63163-114">В последней команде создается служба контейнеров для контейнера, хранящегося в $Container.</span><span class="sxs-lookup"><span data-stu-id="63163-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="63163-115">Служба называется csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="63163-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="63163-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63163-116">PARAMETERS</span></span>

### <span data-ttu-id="63163-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63163-117">-AsJob</span></span>
<span data-ttu-id="63163-118">Командлет RRun в фоновом режиме и возвращают задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="63163-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63163-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="63163-119">-ContainerService</span></span>
<span data-ttu-id="63163-120">Указывает объект службы контейнера, содержащий свойства для новой службы.</span><span class="sxs-lookup"><span data-stu-id="63163-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="63163-121">Чтобы получить объект **ContainerService** , используйте командлет New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="63163-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63163-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63163-122">-DefaultProfile</span></span>
<span data-ttu-id="63163-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63163-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63163-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63163-124">-Name</span></span>
<span data-ttu-id="63163-125">Указывает имя службы контейнеров, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="63163-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63163-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63163-126">-ResourceGroupName</span></span>
<span data-ttu-id="63163-127">Указывает группу ресурсов, в которой этот командлет развертывает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="63163-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63163-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63163-128">-Confirm</span></span>
<span data-ttu-id="63163-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63163-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63163-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63163-130">-WhatIf</span></span>
<span data-ttu-id="63163-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63163-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63163-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63163-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63163-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63163-133">CommonParameters</span></span>
<span data-ttu-id="63163-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63163-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63163-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63163-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63163-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63163-136">INPUTS</span></span>

### <span data-ttu-id="63163-137">System. String</span><span class="sxs-lookup"><span data-stu-id="63163-137">System.String</span></span>

### <span data-ttu-id="63163-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="63163-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="63163-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63163-139">OUTPUTS</span></span>

### <span data-ttu-id="63163-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="63163-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="63163-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="63163-141">NOTES</span></span>

## <span data-ttu-id="63163-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63163-142">RELATED LINKS</span></span>

[<span data-ttu-id="63163-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="63163-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="63163-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="63163-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="63163-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="63163-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="63163-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="63163-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)

