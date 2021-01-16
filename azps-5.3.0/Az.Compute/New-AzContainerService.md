---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509121"
---
# <span data-ttu-id="f0d49-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f0d49-101">New-AzContainerService</span></span>

## <span data-ttu-id="f0d49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d49-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d49-103">Создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="f0d49-103">Creates a container service.</span></span>

## <span data-ttu-id="f0d49-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0d49-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d49-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0d49-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d49-106">Для создания службы контейнеров будет создаваться **cmdlet New-AzContainerService.**</span><span class="sxs-lookup"><span data-stu-id="f0d49-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="f0d49-107">Укажите объект службы контейнеров, который можно создать с помощью New-AzContainerServiceConfig управления.</span><span class="sxs-lookup"><span data-stu-id="f0d49-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="f0d49-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0d49-108">EXAMPLES</span></span>

### <span data-ttu-id="f0d49-109">Пример 1. Создание службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="f0d49-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="f0d49-110">Первая команда создает группу ресурсов с именем ResourceGroup17 в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="f0d49-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="f0d49-111">Дополнительные сведения см. в New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f0d49-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f0d49-112">Вторая команда создает контейнер, а затем сохраняет его в $Container переменной.</span><span class="sxs-lookup"><span data-stu-id="f0d49-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="f0d49-113">Дополнительные сведения см. в New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="f0d49-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="f0d49-114">Конечная команда создает службу контейнера для контейнера, храняного в $Container.</span><span class="sxs-lookup"><span data-stu-id="f0d49-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="f0d49-115">Служба называется csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="f0d49-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="f0d49-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0d49-116">PARAMETERS</span></span>

### <span data-ttu-id="f0d49-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0d49-117">-AsJob</span></span>
<span data-ttu-id="f0d49-118">RRun в фоновом режиме и возврат задания для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f0d49-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f0d49-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f0d49-119">-ContainerService</span></span>
<span data-ttu-id="f0d49-120">Указывает объект службы контейнера, содержащий свойства для новой службы.</span><span class="sxs-lookup"><span data-stu-id="f0d49-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="f0d49-121">Чтобы получить объект **ContainerService,** используйте New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="f0d49-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="f0d49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d49-122">-DefaultProfile</span></span>
<span data-ttu-id="f0d49-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d49-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f0d49-124">-Name</span></span>
<span data-ttu-id="f0d49-125">Указывает имя службы контейнеров, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d49-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f0d49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d49-126">-ResourceGroupName</span></span>
<span data-ttu-id="f0d49-127">Определяет группу ресурсов, в которой этот cmdlet развертывает службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="f0d49-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="f0d49-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0d49-128">-Confirm</span></span>
<span data-ttu-id="f0d49-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f0d49-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d49-130">-WhatIf</span></span>
<span data-ttu-id="f0d49-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d49-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d49-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0d49-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d49-133">CommonParameters</span></span>
<span data-ttu-id="f0d49-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d49-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0d49-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d49-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0d49-136">INPUTS</span></span>

### <span data-ttu-id="f0d49-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f0d49-137">System.String</span></span>

### <span data-ttu-id="f0d49-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f0d49-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f0d49-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0d49-139">OUTPUTS</span></span>

### <span data-ttu-id="f0d49-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f0d49-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f0d49-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0d49-141">NOTES</span></span>

## <span data-ttu-id="f0d49-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0d49-142">RELATED LINKS</span></span>

[<span data-ttu-id="f0d49-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f0d49-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="f0d49-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="f0d49-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="f0d49-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f0d49-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="f0d49-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f0d49-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


