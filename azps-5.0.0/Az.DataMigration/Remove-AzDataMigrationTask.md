---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313100"
---
# <span data-ttu-id="c2861-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c2861-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="c2861-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2861-102">SYNOPSIS</span></span>
<span data-ttu-id="c2861-103">Удаление задачи службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="c2861-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="c2861-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2861-104">SYNTAX</span></span>

### <span data-ttu-id="c2861-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2861-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2861-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2861-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2861-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2861-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2861-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2861-108">DESCRIPTION</span></span>
<span data-ttu-id="c2861-109">Командлет Remove-AzDataMigrationTask удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="c2861-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="c2861-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2861-110">EXAMPLES</span></span>

### <span data-ttu-id="c2861-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2861-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="c2861-112">В предыдущем примере задача службы миграции баз данных Azure с именем TestTask из Azure будет удалена с учетом параметра имени задачи.</span><span class="sxs-lookup"><span data-stu-id="c2861-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="c2861-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c2861-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="c2861-114">В предыдущем примере задача службы миграции баз данных Azure удаляется на основе объекта PSProjectTask, переданного в.</span><span class="sxs-lookup"><span data-stu-id="c2861-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="c2861-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2861-115">PARAMETERS</span></span>

### <span data-ttu-id="c2861-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2861-116">-DefaultProfile</span></span>
<span data-ttu-id="c2861-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2861-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2861-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c2861-118">-Force</span></span>
<span data-ttu-id="c2861-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="c2861-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c2861-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2861-120">-InputObject</span></span>
<span data-ttu-id="c2861-121">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="c2861-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2861-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2861-122">-Name</span></span>
<span data-ttu-id="c2861-123">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="c2861-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2861-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2861-124">-PassThru</span></span>
<span data-ttu-id="c2861-125">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="c2861-125">Returns an true/false.</span></span>
<span data-ttu-id="c2861-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c2861-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2861-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c2861-127">-ProjectName</span></span>
<span data-ttu-id="c2861-128">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="c2861-128">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2861-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2861-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2861-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2861-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2861-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2861-131">-ResourceId</span></span>
<span data-ttu-id="c2861-132">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="c2861-132">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2861-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c2861-133">-ServiceName</span></span>
<span data-ttu-id="c2861-134">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="c2861-134">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2861-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2861-135">-Confirm</span></span>
<span data-ttu-id="c2861-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2861-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2861-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2861-137">-WhatIf</span></span>
<span data-ttu-id="c2861-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2861-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2861-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2861-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2861-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2861-140">CommonParameters</span></span>
<span data-ttu-id="c2861-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2861-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2861-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2861-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2861-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2861-143">INPUTS</span></span>

### <span data-ttu-id="c2861-144">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c2861-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="c2861-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c2861-145">System.String</span></span>

## <span data-ttu-id="c2861-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2861-146">OUTPUTS</span></span>

### <span data-ttu-id="c2861-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2861-147">System.Boolean</span></span>

## <span data-ttu-id="c2861-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2861-148">NOTES</span></span>

## <span data-ttu-id="c2861-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2861-149">RELATED LINKS</span></span>
