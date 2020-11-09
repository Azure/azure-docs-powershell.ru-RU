---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314234"
---
# <span data-ttu-id="ff690-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ff690-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ff690-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff690-102">SYNOPSIS</span></span>
<span data-ttu-id="ff690-103">Удаление расписания пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ff690-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="ff690-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff690-104">SYNTAX</span></span>

### <span data-ttu-id="ff690-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff690-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff690-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff690-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff690-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff690-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff690-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff690-108">DESCRIPTION</span></span>
<span data-ttu-id="ff690-109">Командлет **Remove-AzDataBoxEdgeBandwidthSchedule** Удаляет расписание пропускной способности для пограничного устройства поля данных.</span><span class="sxs-lookup"><span data-stu-id="ff690-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="ff690-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff690-110">EXAMPLES</span></span>

### <span data-ttu-id="ff690-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff690-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="ff690-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff690-112">PARAMETERS</span></span>

### <span data-ttu-id="ff690-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff690-113">-AsJob</span></span>
<span data-ttu-id="ff690-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ff690-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff690-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff690-115">-DefaultProfile</span></span>
<span data-ttu-id="ff690-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff690-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff690-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="ff690-117">-DeviceName</span></span>
<span data-ttu-id="ff690-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="ff690-118">Device Name</span></span>

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

### <span data-ttu-id="ff690-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff690-119">-InputObject</span></span>
<span data-ttu-id="ff690-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="ff690-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff690-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff690-121">-Name</span></span>
<span data-ttu-id="ff690-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="ff690-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff690-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff690-123">-PassThru</span></span>
<span data-ttu-id="ff690-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="ff690-124">returns true if successful</span></span>

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

### <span data-ttu-id="ff690-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff690-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff690-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ff690-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ff690-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff690-127">-ResourceId</span></span>
<span data-ttu-id="ff690-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff690-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ff690-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff690-129">-Confirm</span></span>
<span data-ttu-id="ff690-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff690-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff690-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff690-131">-WhatIf</span></span>
<span data-ttu-id="ff690-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff690-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff690-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff690-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff690-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff690-134">CommonParameters</span></span>
<span data-ttu-id="ff690-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff690-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff690-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff690-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff690-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff690-137">INPUTS</span></span>

### <span data-ttu-id="ff690-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ff690-138">System.String</span></span>

### <span data-ttu-id="ff690-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ff690-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ff690-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff690-140">OUTPUTS</span></span>

### <span data-ttu-id="ff690-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff690-141">System.Boolean</span></span>

## <span data-ttu-id="ff690-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff690-142">NOTES</span></span>

## <span data-ttu-id="ff690-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff690-143">RELATED LINKS</span></span>
