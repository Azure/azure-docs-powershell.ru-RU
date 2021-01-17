---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405087"
---
# <span data-ttu-id="e5afe-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="e5afe-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="e5afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5afe-102">SYNOPSIS</span></span>
<span data-ttu-id="e5afe-103">Вызов отступа для концентратора IoT в геосопозиционном регионе аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="e5afe-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="e5afe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5afe-104">SYNTAX</span></span>

### <span data-ttu-id="e5afe-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5afe-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5afe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5afe-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5afe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5afe-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5afe-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5afe-108">DESCRIPTION</span></span>
<span data-ttu-id="e5afe-109">Он активирует отбой концентратор IoT на дополнительное место.</span><span class="sxs-lookup"><span data-stu-id="e5afe-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="e5afe-110">Это действие приведет к простою решения и потере данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="e5afe-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="e5afe-111">Операция является длительной, и ее можно завершить в течение нескольких минут.</span><span class="sxs-lookup"><span data-stu-id="e5afe-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="e5afe-112">Будьте осторожны с осторожностью при его использовании.</span><span class="sxs-lookup"><span data-stu-id="e5afe-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="e5afe-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5afe-113">EXAMPLES</span></span>

### <span data-ttu-id="e5afe-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5afe-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e5afe-115">Инициирование отладки концентратора IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e5afe-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e5afe-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5afe-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="e5afe-117">Инициирование отладки концентратора IoT "myiothub" в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="e5afe-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="e5afe-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5afe-118">PARAMETERS</span></span>

### <span data-ttu-id="e5afe-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5afe-119">-AsJob</span></span>
<span data-ttu-id="e5afe-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e5afe-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5afe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5afe-121">-DefaultProfile</span></span>
<span data-ttu-id="e5afe-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5afe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5afe-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5afe-123">-InputObject</span></span>
<span data-ttu-id="e5afe-124">Объект Iot Hub</span><span class="sxs-lookup"><span data-stu-id="e5afe-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="e5afe-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e5afe-125">-Name</span></span>
<span data-ttu-id="e5afe-126">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="e5afe-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e5afe-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5afe-127">-PassThru</span></span>
<span data-ttu-id="e5afe-128">Разрешает возвращать boolean object.</span><span class="sxs-lookup"><span data-stu-id="e5afe-128">Allows to return the boolean object.</span></span> <span data-ttu-id="e5afe-129">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e5afe-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5afe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5afe-130">-ResourceGroupName</span></span>
<span data-ttu-id="e5afe-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5afe-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e5afe-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5afe-132">-ResourceId</span></span>
<span data-ttu-id="e5afe-133">Iot Hub Resource Id</span><span class="sxs-lookup"><span data-stu-id="e5afe-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="e5afe-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5afe-134">-Confirm</span></span>
<span data-ttu-id="e5afe-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5afe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5afe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5afe-136">-WhatIf</span></span>
<span data-ttu-id="e5afe-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5afe-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5afe-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e5afe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5afe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5afe-139">CommonParameters</span></span>
<span data-ttu-id="e5afe-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5afe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5afe-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5afe-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5afe-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5afe-142">INPUTS</span></span>

### <span data-ttu-id="e5afe-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5afe-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5afe-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e5afe-144">System.String</span></span>

## <span data-ttu-id="e5afe-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5afe-145">OUTPUTS</span></span>

### <span data-ttu-id="e5afe-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5afe-146">System.Boolean</span></span>

## <span data-ttu-id="e5afe-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5afe-147">NOTES</span></span>

## <span data-ttu-id="e5afe-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5afe-148">RELATED LINKS</span></span>
