---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236831"
---
# <span data-ttu-id="7335f-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="7335f-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="7335f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7335f-102">SYNOPSIS</span></span>
<span data-ttu-id="7335f-103">Отменяет текущее задание databox, если задание находится в состоянии отмены.</span><span class="sxs-lookup"><span data-stu-id="7335f-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="7335f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7335f-104">SYNTAX</span></span>

### <span data-ttu-id="7335f-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7335f-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7335f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7335f-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7335f-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7335f-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7335f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7335f-108">DESCRIPTION</span></span>
<span data-ttu-id="7335f-109">Командлет **Stop-AzDataBoxJob** используется для отмены задания databox.</span><span class="sxs-lookup"><span data-stu-id="7335f-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="7335f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7335f-110">EXAMPLES</span></span>

### <span data-ttu-id="7335f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7335f-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="7335f-112">Отменяет указанное задание databox</span><span class="sxs-lookup"><span data-stu-id="7335f-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="7335f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7335f-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="7335f-114">Отменяет указанное задание databox принудительно без подтверждения</span><span class="sxs-lookup"><span data-stu-id="7335f-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="7335f-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7335f-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="7335f-116">Отменяет указанное задание databox</span><span class="sxs-lookup"><span data-stu-id="7335f-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="7335f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7335f-117">PARAMETERS</span></span>

### <span data-ttu-id="7335f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7335f-118">-DefaultProfile</span></span>
<span data-ttu-id="7335f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7335f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7335f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7335f-120">-Force</span></span>
<span data-ttu-id="7335f-121">Принудительная остановка без подтверждения</span><span class="sxs-lookup"><span data-stu-id="7335f-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="7335f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7335f-122">-InputObject</span></span>
<span data-ttu-id="7335f-123">InputObject типа PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="7335f-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="7335f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7335f-124">-Name</span></span>
<span data-ttu-id="7335f-125">Название задания Databox</span><span class="sxs-lookup"><span data-stu-id="7335f-125">Databox Job Name</span></span>

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

### <span data-ttu-id="7335f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7335f-126">-PassThru</span></span>
<span data-ttu-id="7335f-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="7335f-127">PassThru</span></span>

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

### <span data-ttu-id="7335f-128">-Причина</span><span class="sxs-lookup"><span data-stu-id="7335f-128">-Reason</span></span>
<span data-ttu-id="7335f-129">Причина отмены</span><span class="sxs-lookup"><span data-stu-id="7335f-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7335f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7335f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7335f-131">Имя группы ресурсов "работа Databox"</span><span class="sxs-lookup"><span data-stu-id="7335f-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="7335f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7335f-132">-ResourceId</span></span>
<span data-ttu-id="7335f-133">Идентификатор ресурса Databox</span><span class="sxs-lookup"><span data-stu-id="7335f-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="7335f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7335f-134">-Confirm</span></span>
<span data-ttu-id="7335f-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7335f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7335f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7335f-136">-WhatIf</span></span>
<span data-ttu-id="7335f-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7335f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7335f-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7335f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7335f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7335f-139">CommonParameters</span></span>
<span data-ttu-id="7335f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7335f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7335f-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7335f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7335f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7335f-142">INPUTS</span></span>

### <span data-ttu-id="7335f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7335f-143">System.String</span></span>

## <span data-ttu-id="7335f-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7335f-144">OUTPUTS</span></span>

### <span data-ttu-id="7335f-145">System. void</span><span class="sxs-lookup"><span data-stu-id="7335f-145">System.Void</span></span>

## <span data-ttu-id="7335f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="7335f-146">NOTES</span></span>

## <span data-ttu-id="7335f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7335f-147">RELATED LINKS</span></span>
