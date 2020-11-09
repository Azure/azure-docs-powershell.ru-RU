---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244592"
---
# <span data-ttu-id="b07f7-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b07f7-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="b07f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b07f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b07f7-103">Удаление общего доступа с устройства.</span><span class="sxs-lookup"><span data-stu-id="b07f7-103">Removes a share from the device.</span></span>

## <span data-ttu-id="b07f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b07f7-104">SYNTAX</span></span>

### <span data-ttu-id="b07f7-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b07f7-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b07f7-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b07f7-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b07f7-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b07f7-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b07f7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07f7-108">DESCRIPTION</span></span>
<span data-ttu-id="b07f7-109">Командлет **Remove-AzDataBoxEdgeEdgeShare** удаляет связанные общие ресурсы Edge для поля с пограничным устройством данных.</span><span class="sxs-lookup"><span data-stu-id="b07f7-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="b07f7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b07f7-110">EXAMPLES</span></span>

### <span data-ttu-id="b07f7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b07f7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="b07f7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b07f7-112">PARAMETERS</span></span>

### <span data-ttu-id="b07f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b07f7-113">-AsJob</span></span>
<span data-ttu-id="b07f7-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b07f7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b07f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07f7-115">-DefaultProfile</span></span>
<span data-ttu-id="b07f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b07f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07f7-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="b07f7-117">-DeviceName</span></span>
<span data-ttu-id="b07f7-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="b07f7-118">Device Name</span></span>

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

### <span data-ttu-id="b07f7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b07f7-119">-InputObject</span></span>
<span data-ttu-id="b07f7-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="b07f7-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b07f7-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b07f7-121">-Name</span></span>
<span data-ttu-id="b07f7-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="b07f7-122">Resource Name</span></span>

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

### <span data-ttu-id="b07f7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b07f7-123">-PassThru</span></span>
<span data-ttu-id="b07f7-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="b07f7-124">returns true if successful</span></span>

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

### <span data-ttu-id="b07f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="b07f7-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b07f7-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b07f7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b07f7-127">-ResourceId</span></span>
<span data-ttu-id="b07f7-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b07f7-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07f7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b07f7-129">-Confirm</span></span>
<span data-ttu-id="b07f7-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b07f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07f7-131">-WhatIf</span></span>
<span data-ttu-id="b07f7-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b07f7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b07f7-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b07f7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07f7-134">CommonParameters</span></span>
<span data-ttu-id="b07f7-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b07f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07f7-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b07f7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07f7-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b07f7-137">INPUTS</span></span>

### <span data-ttu-id="b07f7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b07f7-138">System.String</span></span>

### <span data-ttu-id="b07f7-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b07f7-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="b07f7-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07f7-140">OUTPUTS</span></span>

### <span data-ttu-id="b07f7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b07f7-141">System.Boolean</span></span>

## <span data-ttu-id="b07f7-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b07f7-142">NOTES</span></span>

## <span data-ttu-id="b07f7-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b07f7-143">RELATED LINKS</span></span>