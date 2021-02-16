---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238363"
---
# <span data-ttu-id="26e65-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="26e65-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="26e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e65-102">SYNOPSIS</span></span>
<span data-ttu-id="26e65-103">Удаляет обойму с устройства.</span><span class="sxs-lookup"><span data-stu-id="26e65-103">Removes a share from the device.</span></span>

## <span data-ttu-id="26e65-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26e65-104">SYNTAX</span></span>

### <span data-ttu-id="26e65-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26e65-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e65-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e65-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e65-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e65-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e65-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26e65-108">DESCRIPTION</span></span>
<span data-ttu-id="26e65-109">Для устройства Edge Data Box удаляются связанные с ним edge shares **(Удалить-AzDataBoxEdgeEdgeShare).**</span><span class="sxs-lookup"><span data-stu-id="26e65-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="26e65-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26e65-110">EXAMPLES</span></span>

### <span data-ttu-id="26e65-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26e65-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="26e65-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26e65-112">PARAMETERS</span></span>

### <span data-ttu-id="26e65-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26e65-113">-AsJob</span></span>
<span data-ttu-id="26e65-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="26e65-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26e65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e65-115">-DefaultProfile</span></span>
<span data-ttu-id="26e65-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26e65-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e65-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="26e65-117">-DeviceName</span></span>
<span data-ttu-id="26e65-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="26e65-118">Device Name</span></span>

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

### <span data-ttu-id="26e65-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26e65-119">-InputObject</span></span>
<span data-ttu-id="26e65-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="26e65-120">Input Object</span></span>

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

### <span data-ttu-id="26e65-121">-Name</span><span class="sxs-lookup"><span data-stu-id="26e65-121">-Name</span></span>
<span data-ttu-id="26e65-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="26e65-122">Resource Name</span></span>

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

### <span data-ttu-id="26e65-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e65-123">-PassThru</span></span>
<span data-ttu-id="26e65-124">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="26e65-124">returns true if successful</span></span>

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

### <span data-ttu-id="26e65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e65-125">-ResourceGroupName</span></span>
<span data-ttu-id="26e65-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="26e65-126">Resource Group Name</span></span>

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

### <span data-ttu-id="26e65-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e65-127">-ResourceId</span></span>
<span data-ttu-id="26e65-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e65-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="26e65-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26e65-129">-Confirm</span></span>
<span data-ttu-id="26e65-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="26e65-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e65-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e65-131">-WhatIf</span></span>
<span data-ttu-id="26e65-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e65-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26e65-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26e65-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e65-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e65-134">CommonParameters</span></span>
<span data-ttu-id="26e65-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e65-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e65-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26e65-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e65-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26e65-137">INPUTS</span></span>

### <span data-ttu-id="26e65-138">System.String</span><span class="sxs-lookup"><span data-stu-id="26e65-138">System.String</span></span>

### <span data-ttu-id="26e65-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="26e65-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="26e65-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26e65-140">OUTPUTS</span></span>

### <span data-ttu-id="26e65-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26e65-141">System.Boolean</span></span>

## <span data-ttu-id="26e65-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26e65-142">NOTES</span></span>

## <span data-ttu-id="26e65-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26e65-143">RELATED LINKS</span></span>
