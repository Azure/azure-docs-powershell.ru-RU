---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504961"
---
# <span data-ttu-id="f295a-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f295a-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="f295a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f295a-102">SYNOPSIS</span></span>
<span data-ttu-id="f295a-103">Вызывает определенные действия с обетом.</span><span class="sxs-lookup"><span data-stu-id="f295a-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="f295a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f295a-104">SYNTAX</span></span>

### <span data-ttu-id="f295a-105">InvokeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f295a-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f295a-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f295a-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295a-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f295a-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f295a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f295a-108">DESCRIPTION</span></span>
<span data-ttu-id="f295a-109">Для обновления данных на устройстве Stack Edge вызывается действие **Invoke-AzStackEdgeShare.**</span><span class="sxs-lookup"><span data-stu-id="f295a-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="f295a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f295a-110">EXAMPLES</span></span>

### <span data-ttu-id="f295a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f295a-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="f295a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f295a-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="f295a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f295a-113">PARAMETERS</span></span>

### <span data-ttu-id="f295a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f295a-114">-AsJob</span></span>
<span data-ttu-id="f295a-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f295a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f295a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f295a-116">-DefaultProfile</span></span>
<span data-ttu-id="f295a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f295a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f295a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f295a-118">-DeviceName</span></span>
<span data-ttu-id="f295a-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f295a-119">Device Name</span></span>

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

### <span data-ttu-id="f295a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f295a-120">-InputObject</span></span>
<span data-ttu-id="f295a-121">Объект Input</span><span class="sxs-lookup"><span data-stu-id="f295a-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f295a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f295a-122">-Name</span></span>
<span data-ttu-id="f295a-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f295a-123">Resource Name</span></span>

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

### <span data-ttu-id="f295a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f295a-124">-PassThru</span></span>
<span data-ttu-id="f295a-125">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="f295a-125">returns true if successful</span></span>

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

### <span data-ttu-id="f295a-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="f295a-126">-RefreshData</span></span>
<span data-ttu-id="f295a-127">Обновление метаданных для обмена данными из облака</span><span class="sxs-lookup"><span data-stu-id="f295a-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="f295a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f295a-128">-ResourceGroupName</span></span>
<span data-ttu-id="f295a-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f295a-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f295a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f295a-130">-ResourceId</span></span>
<span data-ttu-id="f295a-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f295a-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="f295a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f295a-132">-Confirm</span></span>
<span data-ttu-id="f295a-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f295a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f295a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f295a-134">-WhatIf</span></span>
<span data-ttu-id="f295a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f295a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f295a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f295a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f295a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f295a-137">CommonParameters</span></span>
<span data-ttu-id="f295a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f295a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f295a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f295a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f295a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f295a-140">INPUTS</span></span>

### <span data-ttu-id="f295a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f295a-141">System.String</span></span>

### <span data-ttu-id="f295a-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f295a-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f295a-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f295a-143">OUTPUTS</span></span>

### <span data-ttu-id="f295a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f295a-144">System.Boolean</span></span>

## <span data-ttu-id="f295a-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f295a-145">NOTES</span></span>

## <span data-ttu-id="f295a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f295a-146">RELATED LINKS</span></span>
