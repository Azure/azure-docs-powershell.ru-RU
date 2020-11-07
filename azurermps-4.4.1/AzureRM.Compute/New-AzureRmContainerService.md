---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: d908f99e9a1eaa191b45ed08cdb69ebf40b21756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732072"
---
# <span data-ttu-id="71a2d-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="71a2d-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="71a2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="71a2d-103">Создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="71a2d-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71a2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71a2d-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71a2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="71a2d-106">Командлет **New-AzureRmContainerService** создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="71a2d-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="71a2d-107">Укажите объект службы контейнера, который можно создать с помощью командлета New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="71a2d-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="71a2d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71a2d-108">EXAMPLES</span></span>

### <span data-ttu-id="71a2d-109">Пример 1: создание службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="71a2d-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="71a2d-110">Первая команда создает группу ресурсов с именем ResourceGroup17 в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="71a2d-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="71a2d-111">Дополнительные сведения можно найти в командлетах New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71a2d-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="71a2d-112">Вторая команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="71a2d-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="71a2d-113">Дополнительные сведения можно найти в командлетах New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="71a2d-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="71a2d-114">В последней команде создается служба контейнеров для контейнера, хранящегося в $Container.</span><span class="sxs-lookup"><span data-stu-id="71a2d-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="71a2d-115">Служба называется csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="71a2d-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="71a2d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71a2d-116">PARAMETERS</span></span>

### <span data-ttu-id="71a2d-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="71a2d-117">-ContainerService</span></span>
<span data-ttu-id="71a2d-118">Указывает объект службы контейнера, содержащий свойства для новой службы.</span><span class="sxs-lookup"><span data-stu-id="71a2d-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="71a2d-119">Чтобы получить объект **ContainerService** , используйте командлет New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="71a2d-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a2d-120">-DefaultProfile</span></span>
<span data-ttu-id="71a2d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71a2d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71a2d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71a2d-122">-Name</span></span>
<span data-ttu-id="71a2d-123">Указывает имя службы контейнеров, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="71a2d-123">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="71a2d-125">Указывает группу ресурсов, в которой этот командлет развертывает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="71a2d-125">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="71a2d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71a2d-126">-Confirm</span></span>
<span data-ttu-id="71a2d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71a2d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a2d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a2d-128">-WhatIf</span></span>
<span data-ttu-id="71a2d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71a2d-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="71a2d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71a2d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a2d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a2d-131">CommonParameters</span></span>
<span data-ttu-id="71a2d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71a2d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a2d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a2d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a2d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71a2d-134">INPUTS</span></span>

## <span data-ttu-id="71a2d-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a2d-135">OUTPUTS</span></span>

## <span data-ttu-id="71a2d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="71a2d-136">NOTES</span></span>

## <span data-ttu-id="71a2d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71a2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="71a2d-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="71a2d-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="71a2d-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="71a2d-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="71a2d-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="71a2d-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="71a2d-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="71a2d-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


