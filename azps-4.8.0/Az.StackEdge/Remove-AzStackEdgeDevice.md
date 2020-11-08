---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243823"
---
# <span data-ttu-id="e2166-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e2166-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="e2166-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2166-102">SYNOPSIS</span></span>
<span data-ttu-id="e2166-103">Удаление краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="e2166-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="e2166-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2166-104">SYNTAX</span></span>

### <span data-ttu-id="e2166-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2166-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2166-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2166-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2166-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2166-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2166-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2166-108">DESCRIPTION</span></span>
<span data-ttu-id="e2166-109">Командлет **Remove-AzStackEdgeDevice** удаляет конфигурацию для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="e2166-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="e2166-110">Обратите внимание, что устройство можно удалить только после того, как вы размещаете заказ и перед тем как оно будет подготовлено корпорацией Майкрософт для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="e2166-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="e2166-111">Перед использованием этого [командлета](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) ознакомьтесь с документацией по удалению ресурса</span><span class="sxs-lookup"><span data-stu-id="e2166-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="e2166-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2166-112">EXAMPLES</span></span>

### <span data-ttu-id="e2166-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2166-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="e2166-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2166-114">PARAMETERS</span></span>

### <span data-ttu-id="e2166-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2166-115">-AsJob</span></span>
<span data-ttu-id="e2166-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e2166-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2166-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2166-117">-DefaultProfile</span></span>
<span data-ttu-id="e2166-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2166-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2166-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e2166-119">-DeviceObject</span></span>
<span data-ttu-id="e2166-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="e2166-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2166-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2166-121">-Name</span></span>
<span data-ttu-id="e2166-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="e2166-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2166-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2166-123">-PassThru</span></span>
<span data-ttu-id="e2166-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="e2166-124">returns true if successful</span></span>

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

### <span data-ttu-id="e2166-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2166-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2166-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2166-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2166-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2166-127">-ResourceId</span></span>
<span data-ttu-id="e2166-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2166-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2166-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2166-129">-Confirm</span></span>
<span data-ttu-id="e2166-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2166-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2166-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2166-131">-WhatIf</span></span>
<span data-ttu-id="e2166-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2166-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2166-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2166-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2166-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2166-134">CommonParameters</span></span>
<span data-ttu-id="e2166-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2166-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2166-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2166-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2166-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2166-137">INPUTS</span></span>

### <span data-ttu-id="e2166-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e2166-138">System.String</span></span>

### <span data-ttu-id="e2166-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e2166-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="e2166-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2166-140">OUTPUTS</span></span>

### <span data-ttu-id="e2166-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2166-141">System.Boolean</span></span>

## <span data-ttu-id="e2166-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2166-142">NOTES</span></span>

## <span data-ttu-id="e2166-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2166-143">RELATED LINKS</span></span>
