---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: b8f453200f2365272461373214ec92580212c4b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911483"
---
# <span data-ttu-id="fb000-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb000-101">New-AzContainerService</span></span>

## <span data-ttu-id="fb000-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb000-102">SYNOPSIS</span></span>
<span data-ttu-id="fb000-103">Создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="fb000-103">Creates a container service.</span></span>

## <span data-ttu-id="fb000-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb000-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb000-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb000-105">DESCRIPTION</span></span>
<span data-ttu-id="fb000-106">Командлет **New-AzContainerService** создает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="fb000-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="fb000-107">Укажите объект службы контейнера, который можно создать с помощью командлета New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="fb000-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="fb000-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb000-108">EXAMPLES</span></span>

### <span data-ttu-id="fb000-109">Пример 1: создание службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="fb000-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="fb000-110">Первая команда создает группу ресурсов с именем ResourceGroup17 в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="fb000-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="fb000-111">Дополнительные сведения можно найти в командлетах New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fb000-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="fb000-112">Вторая команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="fb000-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="fb000-113">Дополнительные сведения можно найти в командлетах New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="fb000-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="fb000-114">В последней команде создается служба контейнеров для контейнера, хранящегося в $Container.</span><span class="sxs-lookup"><span data-stu-id="fb000-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="fb000-115">Служба называется csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="fb000-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="fb000-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb000-116">PARAMETERS</span></span>

### <span data-ttu-id="fb000-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb000-117">-AsJob</span></span>
<span data-ttu-id="fb000-118">Командлет RRun в фоновом режиме и возвращают задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb000-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fb000-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="fb000-119">-ContainerService</span></span>
<span data-ttu-id="fb000-120">Указывает объект службы контейнера, содержащий свойства для новой службы.</span><span class="sxs-lookup"><span data-stu-id="fb000-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="fb000-121">Чтобы получить объект **ContainerService** , используйте командлет New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="fb000-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="fb000-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb000-122">-DefaultProfile</span></span>
<span data-ttu-id="fb000-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb000-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb000-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb000-124">-Name</span></span>
<span data-ttu-id="fb000-125">Указывает имя службы контейнеров, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fb000-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fb000-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb000-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb000-127">Указывает группу ресурсов, в которой этот командлет развертывает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="fb000-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="fb000-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb000-128">-Confirm</span></span>
<span data-ttu-id="fb000-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb000-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb000-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb000-130">-WhatIf</span></span>
<span data-ttu-id="fb000-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb000-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fb000-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb000-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb000-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb000-133">CommonParameters</span></span>
<span data-ttu-id="fb000-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb000-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb000-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb000-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb000-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb000-136">INPUTS</span></span>

### <span data-ttu-id="fb000-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="fb000-137">ContainerService</span></span>
<span data-ttu-id="fb000-138">Параметр "ContainerService" принимает значение типа "ContainerService" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fb000-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="fb000-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb000-139">OUTPUTS</span></span>

### <span data-ttu-id="fb000-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="fb000-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="fb000-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb000-141">NOTES</span></span>

## <span data-ttu-id="fb000-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb000-142">RELATED LINKS</span></span>

[<span data-ttu-id="fb000-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb000-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="fb000-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="fb000-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="fb000-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb000-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="fb000-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb000-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


