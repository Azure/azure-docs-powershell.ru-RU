---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410044"
---
# <span data-ttu-id="f586c-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f586c-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="f586c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f586c-102">SYNOPSIS</span></span>
<span data-ttu-id="f586c-103">Удаляет обойму с устройства.</span><span class="sxs-lookup"><span data-stu-id="f586c-103">Removes a share from the device.</span></span>

## <span data-ttu-id="f586c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f586c-104">SYNTAX</span></span>

### <span data-ttu-id="f586c-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f586c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f586c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f586c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f586c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f586c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f586c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f586c-108">DESCRIPTION</span></span>
<span data-ttu-id="f586c-109">При **этом для устройства Stack** Edge удаляются связанные с ним edge-акции.</span><span class="sxs-lookup"><span data-stu-id="f586c-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="f586c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f586c-110">EXAMPLES</span></span>

### <span data-ttu-id="f586c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f586c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="f586c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f586c-112">PARAMETERS</span></span>

### <span data-ttu-id="f586c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f586c-113">-AsJob</span></span>
<span data-ttu-id="f586c-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f586c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f586c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f586c-115">-DefaultProfile</span></span>
<span data-ttu-id="f586c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f586c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f586c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f586c-117">-DeviceName</span></span>
<span data-ttu-id="f586c-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f586c-118">Device Name</span></span>

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

### <span data-ttu-id="f586c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f586c-119">-InputObject</span></span>
<span data-ttu-id="f586c-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="f586c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f586c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f586c-121">-Name</span></span>
<span data-ttu-id="f586c-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f586c-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f586c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f586c-123">-PassThru</span></span>
<span data-ttu-id="f586c-124">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="f586c-124">returns true if successful</span></span>

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

### <span data-ttu-id="f586c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f586c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f586c-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f586c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f586c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f586c-127">-ResourceId</span></span>
<span data-ttu-id="f586c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f586c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="f586c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f586c-129">-Confirm</span></span>
<span data-ttu-id="f586c-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f586c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f586c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f586c-131">-WhatIf</span></span>
<span data-ttu-id="f586c-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f586c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f586c-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f586c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f586c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f586c-134">CommonParameters</span></span>
<span data-ttu-id="f586c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f586c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f586c-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f586c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f586c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f586c-137">INPUTS</span></span>

### <span data-ttu-id="f586c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f586c-138">System.String</span></span>

### <span data-ttu-id="f586c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f586c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f586c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f586c-140">OUTPUTS</span></span>

### <span data-ttu-id="f586c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f586c-141">System.Boolean</span></span>

## <span data-ttu-id="f586c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f586c-142">NOTES</span></span>

## <span data-ttu-id="f586c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f586c-143">RELATED LINKS</span></span>