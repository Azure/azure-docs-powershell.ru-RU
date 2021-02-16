---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214908"
---
# <span data-ttu-id="28163-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="28163-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="28163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28163-102">SYNOPSIS</span></span>
<span data-ttu-id="28163-103">Удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="28163-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="28163-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28163-104">SYNTAX</span></span>

### <span data-ttu-id="28163-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28163-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28163-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28163-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28163-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28163-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28163-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28163-108">DESCRIPTION</span></span>
<span data-ttu-id="28163-109">Этот Remove-AzDataMigrationTask удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="28163-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="28163-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28163-110">EXAMPLES</span></span>

### <span data-ttu-id="28163-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28163-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="28163-112">В предыдущем примере задача службы миграции баз данных Azure TestTask удаляется из Azure на основе параметра имени задачи.</span><span class="sxs-lookup"><span data-stu-id="28163-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="28163-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="28163-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="28163-114">В предыдущем примере удаляется задача службы миграции баз данных Azure на основе переданного объекта PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="28163-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="28163-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28163-115">PARAMETERS</span></span>

### <span data-ttu-id="28163-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28163-116">-DefaultProfile</span></span>
<span data-ttu-id="28163-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28163-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28163-118">-Force</span><span class="sxs-lookup"><span data-stu-id="28163-118">-Force</span></span>
<span data-ttu-id="28163-119">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="28163-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="28163-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28163-120">-InputObject</span></span>
<span data-ttu-id="28163-121">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="28163-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="28163-122">-Name</span><span class="sxs-lookup"><span data-stu-id="28163-122">-Name</span></span>
<span data-ttu-id="28163-123">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="28163-123">The name of the task.</span></span>

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

### <span data-ttu-id="28163-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28163-124">-PassThru</span></span>
<span data-ttu-id="28163-125">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="28163-125">Returns an true/false.</span></span>
<span data-ttu-id="28163-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="28163-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28163-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="28163-127">-ProjectName</span></span>
<span data-ttu-id="28163-128">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="28163-128">The name of the project.</span></span>

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

### <span data-ttu-id="28163-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28163-129">-ResourceGroupName</span></span>
<span data-ttu-id="28163-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28163-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="28163-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28163-131">-ResourceId</span></span>
<span data-ttu-id="28163-132">ИД ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="28163-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="28163-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28163-133">-ServiceName</span></span>
<span data-ttu-id="28163-134">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="28163-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="28163-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28163-135">-Confirm</span></span>
<span data-ttu-id="28163-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28163-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28163-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28163-137">-WhatIf</span></span>
<span data-ttu-id="28163-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28163-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28163-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="28163-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28163-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28163-140">CommonParameters</span></span>
<span data-ttu-id="28163-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28163-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28163-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28163-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28163-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28163-143">INPUTS</span></span>

### <span data-ttu-id="28163-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="28163-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="28163-145">System.String</span><span class="sxs-lookup"><span data-stu-id="28163-145">System.String</span></span>

## <span data-ttu-id="28163-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28163-146">OUTPUTS</span></span>

### <span data-ttu-id="28163-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28163-147">System.Boolean</span></span>

## <span data-ttu-id="28163-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28163-148">NOTES</span></span>

## <span data-ttu-id="28163-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28163-149">RELATED LINKS</span></span>
