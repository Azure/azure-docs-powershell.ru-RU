---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236823"
---
# <span data-ttu-id="a6195-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a6195-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a6195-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6195-102">SYNOPSIS</span></span>
<span data-ttu-id="a6195-103">Удаление пограничного устройства с полем данных.</span><span class="sxs-lookup"><span data-stu-id="a6195-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="a6195-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6195-104">SYNTAX</span></span>

### <span data-ttu-id="a6195-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6195-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6195-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6195-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6195-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6195-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6195-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6195-108">DESCRIPTION</span></span>
<span data-ttu-id="a6195-109">Командлет **Remove-AzDataBoxEdgeDevice** удаляет конфигурацию пограничного устройства для поля данных.</span><span class="sxs-lookup"><span data-stu-id="a6195-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="a6195-110">Обратите внимание, что устройство можно удалить только после того, как вы размещаете заказ и перед тем как оно будет подготовлено корпорацией Майкрософт для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="a6195-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="a6195-111">Перед использованием этого [командлета](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) ознакомьтесь с документацией по удалению ресурса</span><span class="sxs-lookup"><span data-stu-id="a6195-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="a6195-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6195-112">EXAMPLES</span></span>

### <span data-ttu-id="a6195-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6195-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="a6195-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6195-114">PARAMETERS</span></span>

### <span data-ttu-id="a6195-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6195-115">-AsJob</span></span>
<span data-ttu-id="a6195-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a6195-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6195-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6195-117">-DefaultProfile</span></span>
<span data-ttu-id="a6195-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6195-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6195-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6195-119">-InputObject</span></span>
<span data-ttu-id="a6195-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="a6195-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6195-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6195-121">-Name</span></span>
<span data-ttu-id="a6195-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="a6195-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6195-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6195-123">-PassThru</span></span>
<span data-ttu-id="a6195-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="a6195-124">returns true if successful</span></span>

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

### <span data-ttu-id="a6195-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6195-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6195-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6195-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6195-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6195-127">-ResourceId</span></span>
<span data-ttu-id="a6195-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6195-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="a6195-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6195-129">-Confirm</span></span>
<span data-ttu-id="a6195-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6195-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6195-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6195-131">-WhatIf</span></span>
<span data-ttu-id="a6195-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6195-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6195-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6195-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6195-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6195-134">CommonParameters</span></span>
<span data-ttu-id="a6195-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6195-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6195-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6195-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6195-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6195-137">INPUTS</span></span>

### <span data-ttu-id="a6195-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a6195-138">System.String</span></span>

### <span data-ttu-id="a6195-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a6195-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a6195-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6195-140">OUTPUTS</span></span>

### <span data-ttu-id="a6195-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6195-141">System.Boolean</span></span>

## <span data-ttu-id="a6195-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6195-142">NOTES</span></span>

## <span data-ttu-id="a6195-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6195-143">RELATED LINKS</span></span>