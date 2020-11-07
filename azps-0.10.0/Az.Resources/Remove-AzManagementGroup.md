---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 9ac7717769cef1ad147ea122ddedde3efd1e389f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910855"
---
# <span data-ttu-id="71169-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71169-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="71169-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71169-102">SYNOPSIS</span></span>
<span data-ttu-id="71169-103">Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="71169-103">Removes a Management Group</span></span>

## <span data-ttu-id="71169-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71169-104">SYNTAX</span></span>

### <span data-ttu-id="71169-105">GroupOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71169-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71169-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="71169-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71169-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71169-107">DESCRIPTION</span></span>
<span data-ttu-id="71169-108">Командлет **Remove-AzManagementGroup** удаляет группу управления.</span><span class="sxs-lookup"><span data-stu-id="71169-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="71169-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71169-109">EXAMPLES</span></span>

### <span data-ttu-id="71169-110">Пример 1: Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="71169-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="71169-111">Пример 2: Удаление группы управления с помощью объекта трубопроводов PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71169-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="71169-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71169-112">PARAMETERS</span></span>

### <span data-ttu-id="71169-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71169-113">-DefaultProfile</span></span>
<span data-ttu-id="71169-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71169-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71169-115">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="71169-115">-GroupName</span></span>
<span data-ttu-id="71169-116">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="71169-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71169-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71169-117">-InputObject</span></span>
<span data-ttu-id="71169-118">Объект input из вызова Get</span><span class="sxs-lookup"><span data-stu-id="71169-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="71169-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71169-119">-PassThru</span></span>
<span data-ttu-id="71169-120">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="71169-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="71169-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71169-121">-Confirm</span></span>
<span data-ttu-id="71169-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71169-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71169-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71169-123">-WhatIf</span></span>
<span data-ttu-id="71169-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71169-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71169-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71169-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71169-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71169-126">CommonParameters</span></span>
<span data-ttu-id="71169-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71169-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71169-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71169-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71169-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71169-129">INPUTS</span></span>

### <span data-ttu-id="71169-130">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71169-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="71169-131">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71169-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="71169-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71169-132">OUTPUTS</span></span>

### <span data-ttu-id="71169-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71169-133">System.Boolean</span></span>

## <span data-ttu-id="71169-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="71169-134">NOTES</span></span>

## <span data-ttu-id="71169-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71169-135">RELATED LINKS</span></span>
