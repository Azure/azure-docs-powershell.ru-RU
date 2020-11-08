---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074572"
---
# <span data-ttu-id="e5a22-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e5a22-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="e5a22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5a22-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a22-103">Удаление порядка устройства.</span><span class="sxs-lookup"><span data-stu-id="e5a22-103">Removes the order for a device.</span></span>

## <span data-ttu-id="e5a22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5a22-104">SYNTAX</span></span>

### <span data-ttu-id="e5a22-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5a22-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5a22-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a22-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5a22-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a22-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a22-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5a22-108">DESCRIPTION</span></span>
<span data-ttu-id="e5a22-109">Командлет **Remove-AzDataBoxEdgeOrder** удаляет существующий заказ на пограничном устройстве для поля данных.</span><span class="sxs-lookup"><span data-stu-id="e5a22-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="e5a22-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5a22-110">EXAMPLES</span></span>

### <span data-ttu-id="e5a22-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5a22-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="e5a22-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5a22-112">PARAMETERS</span></span>

### <span data-ttu-id="e5a22-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5a22-113">-AsJob</span></span>
<span data-ttu-id="e5a22-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e5a22-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5a22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a22-115">-DefaultProfile</span></span>
<span data-ttu-id="e5a22-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5a22-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="e5a22-117">-DeviceName</span></span>
<span data-ttu-id="e5a22-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="e5a22-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5a22-119">-InputObject</span></span>
<span data-ttu-id="e5a22-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="e5a22-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a22-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5a22-121">-PassThru</span></span>
<span data-ttu-id="e5a22-122">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="e5a22-122">returns true if successful</span></span>

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

### <span data-ttu-id="e5a22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a22-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5a22-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5a22-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e5a22-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5a22-125">-ResourceId</span></span>
<span data-ttu-id="e5a22-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5a22-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="e5a22-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5a22-127">-Confirm</span></span>
<span data-ttu-id="e5a22-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5a22-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a22-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a22-129">-WhatIf</span></span>
<span data-ttu-id="e5a22-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5a22-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5a22-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5a22-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a22-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a22-132">CommonParameters</span></span>
<span data-ttu-id="e5a22-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5a22-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a22-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5a22-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a22-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5a22-135">INPUTS</span></span>

### <span data-ttu-id="e5a22-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e5a22-136">System.String</span></span>

### <span data-ttu-id="e5a22-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e5a22-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="e5a22-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5a22-138">OUTPUTS</span></span>

### <span data-ttu-id="e5a22-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e5a22-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="e5a22-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5a22-140">NOTES</span></span>

## <span data-ttu-id="e5a22-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5a22-141">RELATED LINKS</span></span>
