---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 8ef763300d530c764aefc3fa18c6bbf2a781b4b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967699"
---
# <span data-ttu-id="d24a8-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d24a8-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="d24a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d24a8-103">Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="d24a8-103">Removes a Management Group</span></span>

## <span data-ttu-id="d24a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d24a8-104">SYNTAX</span></span>

### <span data-ttu-id="d24a8-105">GroupOperations (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d24a8-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24a8-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="d24a8-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d24a8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d24a8-107">DESCRIPTION</span></span>
<span data-ttu-id="d24a8-108">Для удаления группы управления будет удалена группа **Remove-AzManagementGroup.**</span><span class="sxs-lookup"><span data-stu-id="d24a8-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="d24a8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d24a8-109">EXAMPLES</span></span>

### <span data-ttu-id="d24a8-110">Пример 1. Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="d24a8-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="d24a8-111">Пример 2. Удаление группы управления путем перенаправления объектов PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d24a8-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="d24a8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d24a8-112">PARAMETERS</span></span>

### <span data-ttu-id="d24a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24a8-113">-DefaultProfile</span></span>
<span data-ttu-id="d24a8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d24a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d24a8-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="d24a8-115">-GroupName</span></span>
<span data-ttu-id="d24a8-116">ИД группы управления</span><span class="sxs-lookup"><span data-stu-id="d24a8-116">Management Group Id</span></span>

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

### <span data-ttu-id="d24a8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d24a8-117">-InputObject</span></span>
<span data-ttu-id="d24a8-118">Объект ввода из звонка "Получить"</span><span class="sxs-lookup"><span data-stu-id="d24a8-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="d24a8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d24a8-119">-PassThru</span></span>
<span data-ttu-id="d24a8-120">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="d24a8-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="d24a8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d24a8-121">-Confirm</span></span>
<span data-ttu-id="d24a8-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d24a8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24a8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24a8-123">-WhatIf</span></span>
<span data-ttu-id="d24a8-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d24a8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24a8-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d24a8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24a8-126">CommonParameters</span></span>
<span data-ttu-id="d24a8-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24a8-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d24a8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24a8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d24a8-129">INPUTS</span></span>

### <span data-ttu-id="d24a8-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d24a8-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="d24a8-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d24a8-131">OUTPUTS</span></span>

### <span data-ttu-id="d24a8-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d24a8-132">System.Boolean</span></span>

## <span data-ttu-id="d24a8-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d24a8-133">NOTES</span></span>

## <span data-ttu-id="d24a8-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d24a8-134">RELATED LINKS</span></span>
