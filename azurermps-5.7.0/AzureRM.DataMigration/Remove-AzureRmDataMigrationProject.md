---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568587"
---
# <span data-ttu-id="e2387-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e2387-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="e2387-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2387-102">SYNOPSIS</span></span>
<span data-ttu-id="e2387-103">Удаление проекта службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="e2387-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2387-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2387-104">SYNTAX</span></span>

### <span data-ttu-id="e2387-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2387-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e2387-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2387-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e2387-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2387-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e2387-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2387-108">DESCRIPTION</span></span>
<span data-ttu-id="e2387-109">Командлет Remove-AzureRmDataMigrationProject удаляет проект службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="e2387-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="e2387-110">При указании параметра DeleteRunningTask удаляются все задачи службы миграции баз данных Azure, связанные с удаляемым проектом.</span><span class="sxs-lookup"><span data-stu-id="e2387-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="e2387-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2387-111">EXAMPLES</span></span>

### <span data-ttu-id="e2387-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2387-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="e2387-113">В приведенном выше примере проект службы миграции баз данных Azure удаляется из Azure на основе имени входного параметра myDMProject</span><span class="sxs-lookup"><span data-stu-id="e2387-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="e2387-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2387-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="e2387-115">В приведенном выше примере удаляется проект службы миграции баз данных Azure на основе объекта PSProject в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="e2387-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="e2387-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2387-116">PARAMETERS</span></span>

### <span data-ttu-id="e2387-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2387-117">-Confirm</span></span>
<span data-ttu-id="e2387-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2387-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2387-119">-DefaultProfile</span></span>
<span data-ttu-id="e2387-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2387-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="e2387-121">-DeleteRunningTask</span></span>
<span data-ttu-id="e2387-122">Удаление любой выполняемой задачи</span><span class="sxs-lookup"><span data-stu-id="e2387-122">Delete any running task</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e2387-123">-Force</span></span>
<span data-ttu-id="e2387-124">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="e2387-124">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2387-125">-InputObject</span></span>
<span data-ttu-id="e2387-126">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="e2387-126">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2387-127">-Name</span></span>
<span data-ttu-id="e2387-128">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="e2387-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2387-129">-PassThru</span></span>
<span data-ttu-id="e2387-130">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="e2387-130">Returns an true/false.</span></span>
<span data-ttu-id="e2387-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e2387-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2387-132">-ResourceGroupName</span></span>
<span data-ttu-id="e2387-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2387-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2387-134">-ResourceId</span></span>
<span data-ttu-id="e2387-135">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="e2387-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e2387-136">-ServiceName</span></span>
<span data-ttu-id="e2387-137">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="e2387-137">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2387-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2387-138">-WhatIf</span></span>
<span data-ttu-id="e2387-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2387-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2387-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2387-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e2387-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2387-141">INPUTS</span></span>

### <span data-ttu-id="e2387-142">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="e2387-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="e2387-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e2387-143">System.String</span></span>


## <span data-ttu-id="e2387-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2387-144">OUTPUTS</span></span>

### <span data-ttu-id="e2387-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2387-145">System.Boolean</span></span>


## <span data-ttu-id="e2387-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2387-146">NOTES</span></span>

## <span data-ttu-id="e2387-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2387-147">RELATED LINKS</span></span>

