---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 6d1a891dbef40a6556e3a8f2ca122f2c3b46cb28
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913492"
---
# <span data-ttu-id="17298-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="17298-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="17298-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17298-102">SYNOPSIS</span></span>
<span data-ttu-id="17298-103">Создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="17298-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17298-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17298-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17298-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17298-105">DESCRIPTION</span></span>
<span data-ttu-id="17298-106">Командлет **New-AzureRmContainerService** создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="17298-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="17298-107">Укажите объект службы контейнера, который можно создать с помощью командлета New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="17298-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="17298-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17298-108">EXAMPLES</span></span>

### <span data-ttu-id="17298-109">Пример 1: создание службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="17298-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="17298-110">Первая команда создает группу ресурсов с именем ResourceGroup17 в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="17298-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="17298-111">Дополнительные сведения можно найти в командлетах New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="17298-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="17298-112">Вторая команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="17298-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="17298-113">Дополнительные сведения можно найти в командлетах New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="17298-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="17298-114">В последней команде создается служба контейнеров для контейнера, хранящегося в $Container.</span><span class="sxs-lookup"><span data-stu-id="17298-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="17298-115">Служба называется csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="17298-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="17298-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17298-116">PARAMETERS</span></span>

### <span data-ttu-id="17298-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17298-117">-AsJob</span></span>
<span data-ttu-id="17298-118">Командлет RRun в фоновом режиме и возвращают задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="17298-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17298-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="17298-119">-ContainerService</span></span>
<span data-ttu-id="17298-120">Указывает объект службы контейнера, содержащий свойства для новой службы.</span><span class="sxs-lookup"><span data-stu-id="17298-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="17298-121">Чтобы получить объект **ContainerService** , используйте командлет New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="17298-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17298-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17298-122">-DefaultProfile</span></span>
<span data-ttu-id="17298-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17298-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17298-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17298-124">-Name</span></span>
<span data-ttu-id="17298-125">Указывает имя службы контейнеров, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="17298-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17298-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17298-126">-ResourceGroupName</span></span>
<span data-ttu-id="17298-127">Указывает группу ресурсов, в которой этот командлет развертывает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="17298-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17298-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17298-128">-Confirm</span></span>
<span data-ttu-id="17298-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17298-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17298-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17298-130">-WhatIf</span></span>
<span data-ttu-id="17298-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17298-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="17298-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17298-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17298-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17298-133">CommonParameters</span></span>
<span data-ttu-id="17298-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17298-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17298-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17298-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17298-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17298-136">INPUTS</span></span>

### <span data-ttu-id="17298-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="17298-137">ContainerService</span></span>
<span data-ttu-id="17298-138">Параметр "ContainerService" принимает значение типа "ContainerService" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="17298-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="17298-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17298-139">OUTPUTS</span></span>

### <span data-ttu-id="17298-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="17298-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="17298-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="17298-141">NOTES</span></span>

## <span data-ttu-id="17298-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17298-142">RELATED LINKS</span></span>

[<span data-ttu-id="17298-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="17298-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="17298-144">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="17298-144">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="17298-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="17298-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="17298-146">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="17298-146">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


