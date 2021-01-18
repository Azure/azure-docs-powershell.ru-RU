---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505169"
---
# <span data-ttu-id="13b1e-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13b1e-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="13b1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="13b1e-103">Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="13b1e-103">Removes a Management Group</span></span>

## <span data-ttu-id="13b1e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="13b1e-104">SYNTAX</span></span>

### <span data-ttu-id="13b1e-105">GroupOperations (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13b1e-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b1e-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="13b1e-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b1e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13b1e-107">DESCRIPTION</span></span>
<span data-ttu-id="13b1e-108">Для удаления группы управления будет удалена группа **Remove-AzManagementGroup.**</span><span class="sxs-lookup"><span data-stu-id="13b1e-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="13b1e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="13b1e-109">EXAMPLES</span></span>

### <span data-ttu-id="13b1e-110">Пример 1. Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="13b1e-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="13b1e-111">Пример 2. Удаление группы управления путем перенаправления объектов PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13b1e-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="13b1e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b1e-112">PARAMETERS</span></span>

### <span data-ttu-id="13b1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b1e-113">-DefaultProfile</span></span>
<span data-ttu-id="13b1e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13b1e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b1e-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="13b1e-115">-GroupName</span></span>
<span data-ttu-id="13b1e-116">ИД группы управления</span><span class="sxs-lookup"><span data-stu-id="13b1e-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b1e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13b1e-117">-InputObject</span></span>
<span data-ttu-id="13b1e-118">Объект ввода из звонка "Получить"</span><span class="sxs-lookup"><span data-stu-id="13b1e-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b1e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13b1e-119">-PassThru</span></span>
<span data-ttu-id="13b1e-120">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="13b1e-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="13b1e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13b1e-121">-Confirm</span></span>
<span data-ttu-id="13b1e-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="13b1e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b1e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b1e-123">-WhatIf</span></span>
<span data-ttu-id="13b1e-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13b1e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13b1e-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="13b1e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b1e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b1e-126">CommonParameters</span></span>
<span data-ttu-id="13b1e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b1e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b1e-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13b1e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b1e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13b1e-129">INPUTS</span></span>

### <span data-ttu-id="13b1e-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="13b1e-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="13b1e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="13b1e-131">OUTPUTS</span></span>

### <span data-ttu-id="13b1e-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13b1e-132">System.Boolean</span></span>

## <span data-ttu-id="13b1e-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="13b1e-133">NOTES</span></span>

## <span data-ttu-id="13b1e-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13b1e-134">RELATED LINKS</span></span>
