---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: acb7e9b453b94381f4f5a2a0edf49e32258809ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996761"
---
# <span data-ttu-id="4d2dd-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="4d2dd-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="4d2dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="4d2dd-103">Удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="4d2dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d2dd-104">SYNTAX</span></span>

### <span data-ttu-id="4d2dd-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d2dd-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d2dd-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d2dd-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d2dd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d2dd-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d2dd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d2dd-108">DESCRIPTION</span></span>
<span data-ttu-id="4d2dd-109">Этот Remove-AzDataMigrationTask удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="4d2dd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d2dd-110">EXAMPLES</span></span>

### <span data-ttu-id="4d2dd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d2dd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="4d2dd-112">В предыдущем примере задача службы миграции баз данных Azure TestTask удаляется из Azure на основе параметра имени задачи.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="4d2dd-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4d2dd-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="4d2dd-114">В предыдущем примере удаляется задача службы миграции баз данных Azure на основе переданного объекта PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="4d2dd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d2dd-115">PARAMETERS</span></span>

### <span data-ttu-id="4d2dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d2dd-116">-DefaultProfile</span></span>
<span data-ttu-id="4d2dd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d2dd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4d2dd-118">-Force</span></span>
<span data-ttu-id="4d2dd-119">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="4d2dd-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4d2dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d2dd-120">-InputObject</span></span>
<span data-ttu-id="4d2dd-121">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="4d2dd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4d2dd-122">-Name</span></span>
<span data-ttu-id="4d2dd-123">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-123">The name of the task.</span></span>

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

### <span data-ttu-id="4d2dd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d2dd-124">-PassThru</span></span>
<span data-ttu-id="4d2dd-125">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="4d2dd-125">Returns an true/false.</span></span>
<span data-ttu-id="4d2dd-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d2dd-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="4d2dd-127">-ProjectName</span></span>
<span data-ttu-id="4d2dd-128">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-128">The name of the project.</span></span>

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

### <span data-ttu-id="4d2dd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d2dd-129">-ResourceGroupName</span></span>
<span data-ttu-id="4d2dd-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d2dd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d2dd-131">-ResourceId</span></span>
<span data-ttu-id="4d2dd-132">ИД ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="4d2dd-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4d2dd-133">-ServiceName</span></span>
<span data-ttu-id="4d2dd-134">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="4d2dd-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d2dd-135">-Confirm</span></span>
<span data-ttu-id="4d2dd-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d2dd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d2dd-137">-WhatIf</span></span>
<span data-ttu-id="4d2dd-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d2dd-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d2dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d2dd-140">CommonParameters</span></span>
<span data-ttu-id="4d2dd-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d2dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d2dd-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d2dd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d2dd-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d2dd-143">INPUTS</span></span>

### <span data-ttu-id="4d2dd-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="4d2dd-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="4d2dd-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4d2dd-145">System.String</span></span>

## <span data-ttu-id="4d2dd-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d2dd-146">OUTPUTS</span></span>

### <span data-ttu-id="4d2dd-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d2dd-147">System.Boolean</span></span>

## <span data-ttu-id="4d2dd-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d2dd-148">NOTES</span></span>

## <span data-ttu-id="4d2dd-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d2dd-149">RELATED LINKS</span></span>
