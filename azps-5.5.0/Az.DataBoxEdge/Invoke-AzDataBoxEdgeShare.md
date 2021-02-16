---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228956"
---
# <span data-ttu-id="a17fa-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a17fa-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="a17fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a17fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a17fa-103">Вызывает определенные действия с обетом.</span><span class="sxs-lookup"><span data-stu-id="a17fa-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="a17fa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a17fa-104">SYNTAX</span></span>

### <span data-ttu-id="a17fa-105">InvokeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a17fa-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a17fa-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a17fa-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a17fa-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a17fa-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a17fa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a17fa-108">DESCRIPTION</span></span>
<span data-ttu-id="a17fa-109">**Cmdlet Invoke-AzDataBoxEdgeShare** вызывает действие для обновления данных на устройстве Edge Data Box.</span><span class="sxs-lookup"><span data-stu-id="a17fa-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="a17fa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a17fa-110">EXAMPLES</span></span>

### <span data-ttu-id="a17fa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a17fa-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="a17fa-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a17fa-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="a17fa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a17fa-113">PARAMETERS</span></span>

### <span data-ttu-id="a17fa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a17fa-114">-AsJob</span></span>
<span data-ttu-id="a17fa-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a17fa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a17fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a17fa-116">-DefaultProfile</span></span>
<span data-ttu-id="a17fa-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a17fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a17fa-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a17fa-118">-DeviceName</span></span>
<span data-ttu-id="a17fa-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="a17fa-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a17fa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a17fa-120">-InputObject</span></span>
<span data-ttu-id="a17fa-121">Объект Input</span><span class="sxs-lookup"><span data-stu-id="a17fa-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a17fa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a17fa-122">-Name</span></span>
<span data-ttu-id="a17fa-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="a17fa-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a17fa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a17fa-124">-PassThru</span></span>
<span data-ttu-id="a17fa-125">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="a17fa-125">returns true if successful</span></span>

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

### <span data-ttu-id="a17fa-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="a17fa-126">-RefreshData</span></span>
<span data-ttu-id="a17fa-127">Обновление метаданных для обмена данными из облака</span><span class="sxs-lookup"><span data-stu-id="a17fa-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="a17fa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a17fa-128">-ResourceGroupName</span></span>
<span data-ttu-id="a17fa-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a17fa-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a17fa-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a17fa-130">-ResourceId</span></span>
<span data-ttu-id="a17fa-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a17fa-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a17fa-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a17fa-132">-Confirm</span></span>
<span data-ttu-id="a17fa-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a17fa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a17fa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a17fa-134">-WhatIf</span></span>
<span data-ttu-id="a17fa-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a17fa-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a17fa-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a17fa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a17fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a17fa-137">CommonParameters</span></span>
<span data-ttu-id="a17fa-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a17fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a17fa-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a17fa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a17fa-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a17fa-140">INPUTS</span></span>

### <span data-ttu-id="a17fa-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a17fa-141">System.String</span></span>

### <span data-ttu-id="a17fa-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a17fa-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="a17fa-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a17fa-143">OUTPUTS</span></span>

### <span data-ttu-id="a17fa-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a17fa-144">System.Boolean</span></span>

## <span data-ttu-id="a17fa-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a17fa-145">NOTES</span></span>

## <span data-ttu-id="a17fa-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a17fa-146">RELATED LINKS</span></span>
