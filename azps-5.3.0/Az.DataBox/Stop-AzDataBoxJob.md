---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519113"
---
# <span data-ttu-id="4eb9e-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="4eb9e-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="4eb9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb9e-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb9e-103">Если задание отменено, задание отменяется.</span><span class="sxs-lookup"><span data-stu-id="4eb9e-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="4eb9e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4eb9e-104">SYNTAX</span></span>

### <span data-ttu-id="4eb9e-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4eb9e-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb9e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb9e-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb9e-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb9e-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb9e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4eb9e-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb9e-109">Для отмены задания используется **cmdlet Stop-AzDataBoxJob.**</span><span class="sxs-lookup"><span data-stu-id="4eb9e-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="4eb9e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4eb9e-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb9e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4eb9e-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="4eb9e-112">Отмена указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="4eb9e-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="4eb9e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4eb9e-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="4eb9e-114">Принудительно отменяет указанное задание для почтового ящика без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4eb9e-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="4eb9e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4eb9e-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="4eb9e-116">Отмена указанного задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="4eb9e-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="4eb9e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb9e-117">PARAMETERS</span></span>

### <span data-ttu-id="4eb9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb9e-118">-DefaultProfile</span></span>
<span data-ttu-id="4eb9e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb9e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4eb9e-120">-Force</span></span>
<span data-ttu-id="4eb9e-121">Принудительно остановить без подтверждения</span><span class="sxs-lookup"><span data-stu-id="4eb9e-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="4eb9e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb9e-122">-InputObject</span></span>
<span data-ttu-id="4eb9e-123">InputObject of type PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="4eb9e-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="4eb9e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb9e-124">-Name</span></span>
<span data-ttu-id="4eb9e-125">Имя задания для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="4eb9e-125">Databox Job Name</span></span>

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

### <span data-ttu-id="4eb9e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eb9e-126">-PassThru</span></span>
<span data-ttu-id="4eb9e-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="4eb9e-127">PassThru</span></span>

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

### <span data-ttu-id="4eb9e-128">-Причина</span><span class="sxs-lookup"><span data-stu-id="4eb9e-128">-Reason</span></span>
<span data-ttu-id="4eb9e-129">Причина отмены</span><span class="sxs-lookup"><span data-stu-id="4eb9e-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="4eb9e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb9e-130">-ResourceGroupName</span></span>
<span data-ttu-id="4eb9e-131">Имя группы ресурсов задания в почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="4eb9e-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="4eb9e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb9e-132">-ResourceId</span></span>
<span data-ttu-id="4eb9e-133">Databox Resource Id</span><span class="sxs-lookup"><span data-stu-id="4eb9e-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="4eb9e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eb9e-134">-Confirm</span></span>
<span data-ttu-id="4eb9e-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4eb9e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb9e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb9e-136">-WhatIf</span></span>
<span data-ttu-id="4eb9e-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb9e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4eb9e-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4eb9e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb9e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb9e-139">CommonParameters</span></span>
<span data-ttu-id="4eb9e-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb9e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb9e-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eb9e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb9e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb9e-142">INPUTS</span></span>

### <span data-ttu-id="4eb9e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb9e-143">System.String</span></span>

## <span data-ttu-id="4eb9e-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb9e-144">OUTPUTS</span></span>

### <span data-ttu-id="4eb9e-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="4eb9e-145">System.Void</span></span>

## <span data-ttu-id="4eb9e-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4eb9e-146">NOTES</span></span>

## <span data-ttu-id="4eb9e-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4eb9e-147">RELATED LINKS</span></span>
