---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066634"
---
# <span data-ttu-id="506a8-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="506a8-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="506a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="506a8-102">SYNOPSIS</span></span>
<span data-ttu-id="506a8-103">Удаляет задание databox</span><span class="sxs-lookup"><span data-stu-id="506a8-103">Deletes the databox job</span></span>

## <span data-ttu-id="506a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="506a8-104">SYNTAX</span></span>

### <span data-ttu-id="506a8-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="506a8-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="506a8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="506a8-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="506a8-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="506a8-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="506a8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="506a8-108">DESCRIPTION</span></span>
<span data-ttu-id="506a8-109">Командлет **Remove-AzDataBoxJob** используется для удаления завершенного задания databox из списка заданий databox.</span><span class="sxs-lookup"><span data-stu-id="506a8-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="506a8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="506a8-110">EXAMPLES</span></span>

### <span data-ttu-id="506a8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="506a8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="506a8-112">Удаляет указанное задание databox</span><span class="sxs-lookup"><span data-stu-id="506a8-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="506a8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="506a8-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="506a8-114">Принудительно удаляет указанное задание databox, не требуя подтверждения</span><span class="sxs-lookup"><span data-stu-id="506a8-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="506a8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="506a8-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="506a8-116">Удаляет указанное задание databox</span><span class="sxs-lookup"><span data-stu-id="506a8-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="506a8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="506a8-117">PARAMETERS</span></span>

### <span data-ttu-id="506a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506a8-118">-DefaultProfile</span></span>
<span data-ttu-id="506a8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="506a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="506a8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="506a8-120">-Force</span></span>
<span data-ttu-id="506a8-121">Принудительное удаление без подтверждения</span><span class="sxs-lookup"><span data-stu-id="506a8-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="506a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="506a8-122">-InputObject</span></span>
<span data-ttu-id="506a8-123">InputObject типа PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="506a8-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="506a8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="506a8-124">-Name</span></span>
<span data-ttu-id="506a8-125">Название задания Databox</span><span class="sxs-lookup"><span data-stu-id="506a8-125">Databox Job Name</span></span>

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

### <span data-ttu-id="506a8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="506a8-126">-PassThru</span></span>
<span data-ttu-id="506a8-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="506a8-127">PassThru</span></span>

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

### <span data-ttu-id="506a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="506a8-129">Имя группы ресурсов "работа Databox"</span><span class="sxs-lookup"><span data-stu-id="506a8-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="506a8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="506a8-130">-ResourceId</span></span>
<span data-ttu-id="506a8-131">Код ресурса задания Databox</span><span class="sxs-lookup"><span data-stu-id="506a8-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="506a8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="506a8-132">-Confirm</span></span>
<span data-ttu-id="506a8-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="506a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="506a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="506a8-134">-WhatIf</span></span>
<span data-ttu-id="506a8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="506a8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="506a8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="506a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="506a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506a8-137">CommonParameters</span></span>
<span data-ttu-id="506a8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="506a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506a8-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="506a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506a8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="506a8-140">INPUTS</span></span>

### <span data-ttu-id="506a8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="506a8-141">System.String</span></span>

## <span data-ttu-id="506a8-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="506a8-142">OUTPUTS</span></span>

### <span data-ttu-id="506a8-143">System. void</span><span class="sxs-lookup"><span data-stu-id="506a8-143">System.Void</span></span>

## <span data-ttu-id="506a8-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="506a8-144">NOTES</span></span>

## <span data-ttu-id="506a8-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="506a8-145">RELATED LINKS</span></span>
