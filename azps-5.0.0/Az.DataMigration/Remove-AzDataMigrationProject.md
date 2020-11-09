---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313106"
---
# <span data-ttu-id="9a498-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="9a498-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="9a498-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a498-102">SYNOPSIS</span></span>
<span data-ttu-id="9a498-103">Удаление проекта службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="9a498-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="9a498-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a498-104">SYNTAX</span></span>

### <span data-ttu-id="9a498-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a498-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a498-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a498-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a498-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a498-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a498-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a498-108">DESCRIPTION</span></span>
<span data-ttu-id="9a498-109">Командлет Remove-AzDataMigrationProject удаляет проект службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="9a498-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="9a498-110">При указании параметра DeleteRunningTask удаляются все задачи службы миграции баз данных Azure, связанные с удаляемым проектом.</span><span class="sxs-lookup"><span data-stu-id="9a498-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="9a498-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a498-111">EXAMPLES</span></span>

### <span data-ttu-id="9a498-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a498-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="9a498-113">В приведенном выше примере проект службы миграции баз данных Azure удаляется из Azure на основе имени входного параметра myDMProject</span><span class="sxs-lookup"><span data-stu-id="9a498-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="9a498-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9a498-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="9a498-115">В приведенном выше примере удаляется проект службы миграции баз данных Azure на основе объекта PSProject в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="9a498-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="9a498-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a498-116">PARAMETERS</span></span>

### <span data-ttu-id="9a498-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a498-117">-DefaultProfile</span></span>
<span data-ttu-id="9a498-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a498-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a498-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="9a498-119">-DeleteRunningTask</span></span>
<span data-ttu-id="9a498-120">Удаление любой выполняемой задачи</span><span class="sxs-lookup"><span data-stu-id="9a498-120">Delete any running task</span></span>

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

### <span data-ttu-id="9a498-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9a498-121">-Force</span></span>
<span data-ttu-id="9a498-122">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="9a498-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9a498-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a498-123">-InputObject</span></span>
<span data-ttu-id="9a498-124">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="9a498-124">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a498-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a498-125">-Name</span></span>
<span data-ttu-id="9a498-126">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="9a498-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a498-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a498-127">-PassThru</span></span>
<span data-ttu-id="9a498-128">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="9a498-128">Returns an true/false.</span></span>
<span data-ttu-id="9a498-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9a498-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a498-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a498-130">-ResourceGroupName</span></span>
<span data-ttu-id="9a498-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a498-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a498-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a498-132">-ResourceId</span></span>
<span data-ttu-id="9a498-133">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="9a498-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="9a498-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9a498-134">-ServiceName</span></span>
<span data-ttu-id="9a498-135">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="9a498-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9a498-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a498-136">-Confirm</span></span>
<span data-ttu-id="9a498-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a498-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a498-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a498-138">-WhatIf</span></span>
<span data-ttu-id="9a498-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a498-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a498-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a498-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a498-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a498-141">CommonParameters</span></span>
<span data-ttu-id="9a498-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a498-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a498-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a498-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a498-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a498-144">INPUTS</span></span>

### <span data-ttu-id="9a498-145">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="9a498-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="9a498-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9a498-146">System.String</span></span>

## <span data-ttu-id="9a498-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a498-147">OUTPUTS</span></span>

### <span data-ttu-id="9a498-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a498-148">System.Boolean</span></span>

## <span data-ttu-id="9a498-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a498-149">NOTES</span></span>

## <span data-ttu-id="9a498-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a498-150">RELATED LINKS</span></span>
