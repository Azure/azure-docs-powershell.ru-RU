---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238426"
---
# <span data-ttu-id="49955-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="49955-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="49955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49955-102">SYNOPSIS</span></span>
<span data-ttu-id="49955-103">Удаляет задание для работы с почтовым ящиком</span><span class="sxs-lookup"><span data-stu-id="49955-103">Deletes the databox job</span></span>

## <span data-ttu-id="49955-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49955-104">SYNTAX</span></span>

### <span data-ttu-id="49955-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49955-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49955-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49955-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49955-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49955-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49955-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49955-108">DESCRIPTION</span></span>
<span data-ttu-id="49955-109">Для удаления завершенного задания в почтовом ящике из списка заданий используется cmdlet **Remove-AzDataBoxJob.**</span><span class="sxs-lookup"><span data-stu-id="49955-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="49955-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49955-110">EXAMPLES</span></span>

### <span data-ttu-id="49955-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49955-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="49955-112">Удаление указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="49955-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="49955-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="49955-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="49955-114">Принудительно удаляет указанное задание для почтового ящика без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="49955-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="49955-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="49955-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="49955-116">Удаление указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="49955-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="49955-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49955-117">PARAMETERS</span></span>

### <span data-ttu-id="49955-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49955-118">-DefaultProfile</span></span>
<span data-ttu-id="49955-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49955-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49955-120">-Force</span><span class="sxs-lookup"><span data-stu-id="49955-120">-Force</span></span>
<span data-ttu-id="49955-121">Принудительное удаление без подтверждения</span><span class="sxs-lookup"><span data-stu-id="49955-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="49955-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49955-122">-InputObject</span></span>
<span data-ttu-id="49955-123">InputObject of type PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="49955-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="49955-124">-Name</span><span class="sxs-lookup"><span data-stu-id="49955-124">-Name</span></span>
<span data-ttu-id="49955-125">Имя задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="49955-125">Databox Job Name</span></span>

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

### <span data-ttu-id="49955-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49955-126">-PassThru</span></span>
<span data-ttu-id="49955-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="49955-127">PassThru</span></span>

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

### <span data-ttu-id="49955-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49955-128">-ResourceGroupName</span></span>
<span data-ttu-id="49955-129">Имя группы ресурсов задания в почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="49955-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="49955-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49955-130">-ResourceId</span></span>
<span data-ttu-id="49955-131">ИД задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="49955-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="49955-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49955-132">-Confirm</span></span>
<span data-ttu-id="49955-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49955-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49955-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49955-134">-WhatIf</span></span>
<span data-ttu-id="49955-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49955-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49955-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="49955-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49955-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49955-137">CommonParameters</span></span>
<span data-ttu-id="49955-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49955-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49955-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49955-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49955-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49955-140">INPUTS</span></span>

### <span data-ttu-id="49955-141">System.String</span><span class="sxs-lookup"><span data-stu-id="49955-141">System.String</span></span>

## <span data-ttu-id="49955-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49955-142">OUTPUTS</span></span>

### <span data-ttu-id="49955-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="49955-143">System.Void</span></span>

## <span data-ttu-id="49955-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49955-144">NOTES</span></span>

## <span data-ttu-id="49955-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49955-145">RELATED LINKS</span></span>
