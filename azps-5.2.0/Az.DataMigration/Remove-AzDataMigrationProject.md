---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407028"
---
# <span data-ttu-id="cc6f2-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="cc6f2-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="cc6f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6f2-103">Удаляет проект службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="cc6f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc6f2-104">SYNTAX</span></span>

### <span data-ttu-id="cc6f2-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc6f2-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc6f2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc6f2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc6f2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc6f2-108">DESCRIPTION</span></span>
<span data-ttu-id="cc6f2-109">Новый Remove-AzDataMigrationProject удаляет проект службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="cc6f2-110">При этом будут удалены все удаляемые задачи службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="cc6f2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc6f2-111">EXAMPLES</span></span>

### <span data-ttu-id="cc6f2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc6f2-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="cc6f2-113">В примере выше проект службы миграции баз данных Azure под названием myDMProject удаляется из Azure на основе имени в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="cc6f2-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc6f2-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="cc6f2-115">В примере выше проект службы миграции баз данных Azure, основанный на объекте PSProject, удаляется в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="cc6f2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-116">PARAMETERS</span></span>

### <span data-ttu-id="cc6f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6f2-117">-DefaultProfile</span></span>
<span data-ttu-id="cc6f2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc6f2-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="cc6f2-119">-DeleteRunningTask</span></span>
<span data-ttu-id="cc6f2-120">Удаление любой запущенной задачи</span><span class="sxs-lookup"><span data-stu-id="cc6f2-120">Delete any running task</span></span>

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

### <span data-ttu-id="cc6f2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cc6f2-121">-Force</span></span>
<span data-ttu-id="cc6f2-122">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="cc6f2-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cc6f2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc6f2-123">-InputObject</span></span>
<span data-ttu-id="cc6f2-124">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-124">PSProject Object.</span></span>

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

### <span data-ttu-id="cc6f2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cc6f2-125">-Name</span></span>
<span data-ttu-id="cc6f2-126">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-126">The name of the project.</span></span>

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

### <span data-ttu-id="cc6f2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc6f2-127">-PassThru</span></span>
<span data-ttu-id="cc6f2-128">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="cc6f2-128">Returns an true/false.</span></span>
<span data-ttu-id="cc6f2-129">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc6f2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6f2-130">-ResourceGroupName</span></span>
<span data-ttu-id="cc6f2-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc6f2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc6f2-132">-ResourceId</span></span>
<span data-ttu-id="cc6f2-133">ИД ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="cc6f2-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cc6f2-134">-ServiceName</span></span>
<span data-ttu-id="cc6f2-135">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="cc6f2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc6f2-136">-Confirm</span></span>
<span data-ttu-id="cc6f2-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc6f2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc6f2-138">-WhatIf</span></span>
<span data-ttu-id="cc6f2-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc6f2-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc6f2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6f2-141">CommonParameters</span></span>
<span data-ttu-id="cc6f2-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6f2-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc6f2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6f2-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-144">INPUTS</span></span>

### <span data-ttu-id="cc6f2-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="cc6f2-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="cc6f2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="cc6f2-146">System.String</span></span>

## <span data-ttu-id="cc6f2-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-147">OUTPUTS</span></span>

### <span data-ttu-id="cc6f2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc6f2-148">System.Boolean</span></span>

## <span data-ttu-id="cc6f2-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc6f2-149">NOTES</span></span>

## <span data-ttu-id="cc6f2-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc6f2-150">RELATED LINKS</span></span>
