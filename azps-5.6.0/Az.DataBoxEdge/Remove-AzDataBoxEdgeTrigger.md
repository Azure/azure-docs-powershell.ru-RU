---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 2e1b3e3db319f724e22673e4139b4cb290879d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004291"
---
# <span data-ttu-id="f0706-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f0706-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f0706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0706-102">SYNOPSIS</span></span>
<span data-ttu-id="f0706-103">Удаляет существующий триггер на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f0706-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="f0706-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0706-104">SYNTAX</span></span>

### <span data-ttu-id="f0706-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0706-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0706-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0706-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0706-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0706-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0706-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0706-108">DESCRIPTION</span></span>
<span data-ttu-id="f0706-109">С **его на устройстве Remove-AzDataBoxEdgeTrigger** удаляется существующий триггер на устройстве Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="f0706-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="f0706-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0706-110">EXAMPLES</span></span>

### <span data-ttu-id="f0706-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0706-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="f0706-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0706-112">PARAMETERS</span></span>

### <span data-ttu-id="f0706-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0706-113">-AsJob</span></span>
<span data-ttu-id="f0706-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f0706-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0706-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0706-115">-DefaultProfile</span></span>
<span data-ttu-id="f0706-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0706-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0706-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f0706-117">-DeviceName</span></span>
<span data-ttu-id="f0706-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f0706-118">Device Name</span></span>

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

### <span data-ttu-id="f0706-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0706-119">-InputObject</span></span>
<span data-ttu-id="f0706-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="f0706-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0706-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f0706-121">-Name</span></span>
<span data-ttu-id="f0706-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f0706-122">Resource Name</span></span>

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

### <span data-ttu-id="f0706-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0706-123">-PassThru</span></span>
<span data-ttu-id="f0706-124">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="f0706-124">returns true if successful</span></span>

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

### <span data-ttu-id="f0706-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0706-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0706-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0706-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f0706-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0706-127">-ResourceId</span></span>
<span data-ttu-id="f0706-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0706-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="f0706-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0706-129">-Confirm</span></span>
<span data-ttu-id="f0706-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0706-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0706-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0706-131">-WhatIf</span></span>
<span data-ttu-id="f0706-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0706-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0706-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0706-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0706-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0706-134">CommonParameters</span></span>
<span data-ttu-id="f0706-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0706-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0706-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0706-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0706-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0706-137">INPUTS</span></span>

### <span data-ttu-id="f0706-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f0706-138">System.String</span></span>

### <span data-ttu-id="f0706-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f0706-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f0706-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0706-140">OUTPUTS</span></span>

### <span data-ttu-id="f0706-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0706-141">System.Boolean</span></span>

## <span data-ttu-id="f0706-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0706-142">NOTES</span></span>

## <span data-ttu-id="f0706-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0706-143">RELATED LINKS</span></span>
