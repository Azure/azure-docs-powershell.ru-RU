---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410055"
---
# <span data-ttu-id="62330-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="62330-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="62330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62330-102">SYNOPSIS</span></span>
<span data-ttu-id="62330-103">Удаляет связанную роль IoT для устройства.</span><span class="sxs-lookup"><span data-stu-id="62330-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="62330-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62330-104">SYNTAX</span></span>

### <span data-ttu-id="62330-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62330-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62330-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62330-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62330-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62330-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62330-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62330-108">DESCRIPTION</span></span>
<span data-ttu-id="62330-109">Для устройства с Stack Edge связанная с ней роль IoT удаляется с его **cmdlet AzStackEdgeRole.**</span><span class="sxs-lookup"><span data-stu-id="62330-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="62330-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62330-110">EXAMPLES</span></span>

### <span data-ttu-id="62330-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62330-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="62330-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62330-112">PARAMETERS</span></span>

### <span data-ttu-id="62330-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62330-113">-AsJob</span></span>
<span data-ttu-id="62330-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="62330-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62330-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62330-115">-DefaultProfile</span></span>
<span data-ttu-id="62330-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62330-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62330-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="62330-117">-DeviceName</span></span>
<span data-ttu-id="62330-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="62330-118">Device Name</span></span>

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

### <span data-ttu-id="62330-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62330-119">-InputObject</span></span>
<span data-ttu-id="62330-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="62330-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62330-121">-Name</span><span class="sxs-lookup"><span data-stu-id="62330-121">-Name</span></span>
<span data-ttu-id="62330-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="62330-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62330-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62330-123">-PassThru</span></span>
<span data-ttu-id="62330-124">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="62330-124">returns true if successful</span></span>

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

### <span data-ttu-id="62330-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62330-125">-ResourceGroupName</span></span>
<span data-ttu-id="62330-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="62330-126">Resource Group Name</span></span>

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

### <span data-ttu-id="62330-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62330-127">-ResourceId</span></span>
<span data-ttu-id="62330-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="62330-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="62330-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62330-129">-Confirm</span></span>
<span data-ttu-id="62330-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="62330-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62330-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62330-131">-WhatIf</span></span>
<span data-ttu-id="62330-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62330-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62330-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62330-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62330-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62330-134">CommonParameters</span></span>
<span data-ttu-id="62330-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62330-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62330-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62330-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62330-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62330-137">INPUTS</span></span>

### <span data-ttu-id="62330-138">System.String</span><span class="sxs-lookup"><span data-stu-id="62330-138">System.String</span></span>

### <span data-ttu-id="62330-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="62330-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="62330-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62330-140">OUTPUTS</span></span>

### <span data-ttu-id="62330-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="62330-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="62330-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62330-142">NOTES</span></span>

## <span data-ttu-id="62330-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62330-143">RELATED LINKS</span></span>
