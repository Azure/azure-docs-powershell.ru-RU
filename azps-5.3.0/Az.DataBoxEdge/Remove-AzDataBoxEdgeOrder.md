---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519061"
---
# <span data-ttu-id="33570-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="33570-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="33570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33570-102">SYNOPSIS</span></span>
<span data-ttu-id="33570-103">Удаляет порядок устройства.</span><span class="sxs-lookup"><span data-stu-id="33570-103">Removes the order for a device.</span></span>

## <span data-ttu-id="33570-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33570-104">SYNTAX</span></span>

### <span data-ttu-id="33570-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33570-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33570-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33570-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33570-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33570-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33570-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33570-108">DESCRIPTION</span></span>
<span data-ttu-id="33570-109">**Cmdlet Remove-AzDataBoxEdgeOrder** удаляет существующий порядок для устройства Edge box данных.</span><span class="sxs-lookup"><span data-stu-id="33570-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="33570-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33570-110">EXAMPLES</span></span>

### <span data-ttu-id="33570-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33570-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="33570-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33570-112">PARAMETERS</span></span>

### <span data-ttu-id="33570-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33570-113">-AsJob</span></span>
<span data-ttu-id="33570-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="33570-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33570-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33570-115">-DefaultProfile</span></span>
<span data-ttu-id="33570-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33570-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33570-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="33570-117">-DeviceName</span></span>
<span data-ttu-id="33570-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="33570-118">Device Name</span></span>

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

### <span data-ttu-id="33570-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33570-119">-InputObject</span></span>
<span data-ttu-id="33570-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="33570-120">Input Object</span></span>

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

### <span data-ttu-id="33570-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33570-121">-PassThru</span></span>
<span data-ttu-id="33570-122">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="33570-122">returns true if successful</span></span>

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

### <span data-ttu-id="33570-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33570-123">-ResourceGroupName</span></span>
<span data-ttu-id="33570-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="33570-124">Resource Group Name</span></span>

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

### <span data-ttu-id="33570-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33570-125">-ResourceId</span></span>
<span data-ttu-id="33570-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="33570-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="33570-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33570-127">-Confirm</span></span>
<span data-ttu-id="33570-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33570-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33570-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33570-129">-WhatIf</span></span>
<span data-ttu-id="33570-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33570-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33570-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="33570-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33570-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33570-132">CommonParameters</span></span>
<span data-ttu-id="33570-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33570-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33570-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33570-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33570-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33570-135">INPUTS</span></span>

### <span data-ttu-id="33570-136">System.String</span><span class="sxs-lookup"><span data-stu-id="33570-136">System.String</span></span>

### <span data-ttu-id="33570-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="33570-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="33570-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33570-138">OUTPUTS</span></span>

### <span data-ttu-id="33570-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="33570-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="33570-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33570-140">NOTES</span></span>

## <span data-ttu-id="33570-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33570-141">RELATED LINKS</span></span>
