---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242733"
---
# <span data-ttu-id="d13c6-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="d13c6-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="d13c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d13c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d13c6-103">Вызовите процесс отработки отказа для центра Интернета вещей в области географического восстановления.</span><span class="sxs-lookup"><span data-stu-id="d13c6-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="d13c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d13c6-104">SYNTAX</span></span>

### <span data-ttu-id="d13c6-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d13c6-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d13c6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d13c6-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d13c6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d13c6-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d13c6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d13c6-108">DESCRIPTION</span></span>
<span data-ttu-id="d13c6-109">Он будет инициировать отработку отказа центра Интернета вещей в дополнительном расположении.</span><span class="sxs-lookup"><span data-stu-id="d13c6-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="d13c6-110">Это действие приведет к потере времени и телеметрии для вашего решения.</span><span class="sxs-lookup"><span data-stu-id="d13c6-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="d13c6-111">Это длительная операция, выполнение которой может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="d13c6-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="d13c6-112">Будьте внимательны при использовании этой функции.</span><span class="sxs-lookup"><span data-stu-id="d13c6-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="d13c6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d13c6-113">EXAMPLES</span></span>

### <span data-ttu-id="d13c6-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d13c6-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d13c6-115">Инициация отказоустойчивого процесса для центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d13c6-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d13c6-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d13c6-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="d13c6-117">Инициация отработки отказа в разделе "myiothub" центра Интернета вещей в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d13c6-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="d13c6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d13c6-118">PARAMETERS</span></span>

### <span data-ttu-id="d13c6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d13c6-119">-AsJob</span></span>
<span data-ttu-id="d13c6-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d13c6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d13c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13c6-121">-DefaultProfile</span></span>
<span data-ttu-id="d13c6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d13c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d13c6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d13c6-123">-InputObject</span></span>
<span data-ttu-id="d13c6-124">Объект центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="d13c6-124">Iot Hub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d13c6-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d13c6-125">-Name</span></span>
<span data-ttu-id="d13c6-126">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="d13c6-126">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13c6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d13c6-127">-PassThru</span></span>
<span data-ttu-id="d13c6-128">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="d13c6-128">Allows to return the boolean object.</span></span> <span data-ttu-id="d13c6-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d13c6-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d13c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d13c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="d13c6-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d13c6-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13c6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d13c6-132">-ResourceId</span></span>
<span data-ttu-id="d13c6-133">Идентификатор ресурса центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="d13c6-133">Iot Hub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13c6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d13c6-134">-Confirm</span></span>
<span data-ttu-id="d13c6-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d13c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d13c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d13c6-136">-WhatIf</span></span>
<span data-ttu-id="d13c6-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d13c6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d13c6-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d13c6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d13c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13c6-139">CommonParameters</span></span>
<span data-ttu-id="d13c6-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d13c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13c6-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13c6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13c6-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d13c6-142">INPUTS</span></span>

### <span data-ttu-id="d13c6-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d13c6-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d13c6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d13c6-144">System.String</span></span>

## <span data-ttu-id="d13c6-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d13c6-145">OUTPUTS</span></span>

### <span data-ttu-id="d13c6-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d13c6-146">System.Boolean</span></span>

## <span data-ttu-id="d13c6-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="d13c6-147">NOTES</span></span>

## <span data-ttu-id="d13c6-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d13c6-148">RELATED LINKS</span></span>
