---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 5a9415b5590b6f78c5ca703dba8293c153de819d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998108"
---
# <span data-ttu-id="37227-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="37227-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="37227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37227-102">SYNOPSIS</span></span>
<span data-ttu-id="37227-103">Удаляет задание для работы с почтовым ящиком</span><span class="sxs-lookup"><span data-stu-id="37227-103">Deletes the databox job</span></span>

## <span data-ttu-id="37227-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37227-104">SYNTAX</span></span>

### <span data-ttu-id="37227-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37227-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37227-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37227-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37227-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37227-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37227-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37227-108">DESCRIPTION</span></span>
<span data-ttu-id="37227-109">Для удаления завершенного задания в почтовом ящике из списка заданий используется cmdlet **Remove-AzDataBoxJob.**</span><span class="sxs-lookup"><span data-stu-id="37227-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="37227-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37227-110">EXAMPLES</span></span>

### <span data-ttu-id="37227-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37227-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="37227-112">Удаление указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="37227-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="37227-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="37227-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="37227-114">Принудительно удаляет указанное задание для почтового ящика без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="37227-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="37227-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="37227-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="37227-116">Удаление указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="37227-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="37227-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37227-117">PARAMETERS</span></span>

### <span data-ttu-id="37227-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37227-118">-DefaultProfile</span></span>
<span data-ttu-id="37227-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37227-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37227-120">-Force</span><span class="sxs-lookup"><span data-stu-id="37227-120">-Force</span></span>
<span data-ttu-id="37227-121">Принудительное удаление без подтверждения</span><span class="sxs-lookup"><span data-stu-id="37227-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="37227-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37227-122">-InputObject</span></span>
<span data-ttu-id="37227-123">InputObject типа PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="37227-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37227-124">-Name</span><span class="sxs-lookup"><span data-stu-id="37227-124">-Name</span></span>
<span data-ttu-id="37227-125">Имя задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="37227-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37227-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37227-126">-PassThru</span></span>
<span data-ttu-id="37227-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="37227-127">PassThru</span></span>

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

### <span data-ttu-id="37227-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37227-128">-ResourceGroupName</span></span>
<span data-ttu-id="37227-129">Имя группы ресурсов задания в почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="37227-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37227-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37227-130">-ResourceId</span></span>
<span data-ttu-id="37227-131">ИД задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="37227-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37227-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37227-132">-Confirm</span></span>
<span data-ttu-id="37227-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37227-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37227-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37227-134">-WhatIf</span></span>
<span data-ttu-id="37227-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37227-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37227-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="37227-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37227-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37227-137">CommonParameters</span></span>
<span data-ttu-id="37227-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37227-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37227-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37227-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37227-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37227-140">INPUTS</span></span>

### <span data-ttu-id="37227-141">System.String</span><span class="sxs-lookup"><span data-stu-id="37227-141">System.String</span></span>

## <span data-ttu-id="37227-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37227-142">OUTPUTS</span></span>

### <span data-ttu-id="37227-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="37227-143">System.Void</span></span>

## <span data-ttu-id="37227-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37227-144">NOTES</span></span>

## <span data-ttu-id="37227-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37227-145">RELATED LINKS</span></span>
