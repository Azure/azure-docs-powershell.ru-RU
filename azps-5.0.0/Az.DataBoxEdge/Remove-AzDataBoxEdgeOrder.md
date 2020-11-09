---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314222"
---
# <span data-ttu-id="60b70-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="60b70-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="60b70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60b70-102">SYNOPSIS</span></span>
<span data-ttu-id="60b70-103">Удаление порядка устройства.</span><span class="sxs-lookup"><span data-stu-id="60b70-103">Removes the order for a device.</span></span>

## <span data-ttu-id="60b70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60b70-104">SYNTAX</span></span>

### <span data-ttu-id="60b70-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60b70-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b70-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60b70-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b70-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60b70-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b70-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60b70-108">DESCRIPTION</span></span>
<span data-ttu-id="60b70-109">Командлет **Remove-AzDataBoxEdgeOrder** удаляет существующий заказ на пограничном устройстве для поля данных.</span><span class="sxs-lookup"><span data-stu-id="60b70-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="60b70-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60b70-110">EXAMPLES</span></span>

### <span data-ttu-id="60b70-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60b70-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="60b70-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60b70-112">PARAMETERS</span></span>

### <span data-ttu-id="60b70-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60b70-113">-AsJob</span></span>
<span data-ttu-id="60b70-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="60b70-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60b70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b70-115">-DefaultProfile</span></span>
<span data-ttu-id="60b70-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60b70-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60b70-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="60b70-117">-DeviceName</span></span>
<span data-ttu-id="60b70-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="60b70-118">Device Name</span></span>

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

### <span data-ttu-id="60b70-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60b70-119">-InputObject</span></span>
<span data-ttu-id="60b70-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="60b70-120">Input Object</span></span>

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

### <span data-ttu-id="60b70-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60b70-121">-PassThru</span></span>
<span data-ttu-id="60b70-122">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="60b70-122">returns true if successful</span></span>

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

### <span data-ttu-id="60b70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b70-123">-ResourceGroupName</span></span>
<span data-ttu-id="60b70-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="60b70-124">Resource Group Name</span></span>

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

### <span data-ttu-id="60b70-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b70-125">-ResourceId</span></span>
<span data-ttu-id="60b70-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b70-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="60b70-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60b70-127">-Confirm</span></span>
<span data-ttu-id="60b70-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60b70-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b70-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b70-129">-WhatIf</span></span>
<span data-ttu-id="60b70-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60b70-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60b70-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60b70-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b70-132">CommonParameters</span></span>
<span data-ttu-id="60b70-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60b70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b70-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60b70-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b70-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60b70-135">INPUTS</span></span>

### <span data-ttu-id="60b70-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60b70-136">System.String</span></span>

### <span data-ttu-id="60b70-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="60b70-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="60b70-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60b70-138">OUTPUTS</span></span>

### <span data-ttu-id="60b70-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="60b70-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="60b70-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="60b70-140">NOTES</span></span>

## <span data-ttu-id="60b70-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60b70-141">RELATED LINKS</span></span>
