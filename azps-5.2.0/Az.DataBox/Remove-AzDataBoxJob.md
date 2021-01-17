---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395844"
---
# <span data-ttu-id="d7b73-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d7b73-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="d7b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7b73-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b73-103">Удаление задания почтового ящика</span><span class="sxs-lookup"><span data-stu-id="d7b73-103">Deletes the databox job</span></span>

## <span data-ttu-id="d7b73-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7b73-104">SYNTAX</span></span>

### <span data-ttu-id="d7b73-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7b73-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7b73-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7b73-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7b73-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7b73-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b73-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7b73-108">DESCRIPTION</span></span>
<span data-ttu-id="d7b73-109">Для удаления завершенного задания в почтовом ящике из списка заданий используется cmdlet **Remove-AzDataBoxJob.**</span><span class="sxs-lookup"><span data-stu-id="d7b73-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="d7b73-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7b73-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b73-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7b73-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="d7b73-112">Удаление указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="d7b73-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="d7b73-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d7b73-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="d7b73-114">Принудительно удаляет указанное задание для почтового ящика без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d7b73-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="d7b73-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d7b73-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="d7b73-116">Удаление указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="d7b73-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="d7b73-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7b73-117">PARAMETERS</span></span>

### <span data-ttu-id="d7b73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b73-118">-DefaultProfile</span></span>
<span data-ttu-id="d7b73-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b73-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b73-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d7b73-120">-Force</span></span>
<span data-ttu-id="d7b73-121">Принудительное удаление без подтверждения</span><span class="sxs-lookup"><span data-stu-id="d7b73-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="d7b73-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7b73-122">-InputObject</span></span>
<span data-ttu-id="d7b73-123">InputObject типа PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d7b73-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="d7b73-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b73-124">-Name</span></span>
<span data-ttu-id="d7b73-125">Имя задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="d7b73-125">Databox Job Name</span></span>

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

### <span data-ttu-id="d7b73-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7b73-126">-PassThru</span></span>
<span data-ttu-id="d7b73-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="d7b73-127">PassThru</span></span>

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

### <span data-ttu-id="d7b73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b73-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7b73-129">Имя группы ресурсов задания в почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="d7b73-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="d7b73-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7b73-130">-ResourceId</span></span>
<span data-ttu-id="d7b73-131">ИД задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="d7b73-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="d7b73-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7b73-132">-Confirm</span></span>
<span data-ttu-id="d7b73-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b73-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b73-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b73-134">-WhatIf</span></span>
<span data-ttu-id="d7b73-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b73-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7b73-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d7b73-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b73-137">CommonParameters</span></span>
<span data-ttu-id="d7b73-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b73-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7b73-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b73-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7b73-140">INPUTS</span></span>

### <span data-ttu-id="d7b73-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d7b73-141">System.String</span></span>

## <span data-ttu-id="d7b73-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7b73-142">OUTPUTS</span></span>

### <span data-ttu-id="d7b73-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="d7b73-143">System.Void</span></span>

## <span data-ttu-id="d7b73-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7b73-144">NOTES</span></span>

## <span data-ttu-id="d7b73-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7b73-145">RELATED LINKS</span></span>
