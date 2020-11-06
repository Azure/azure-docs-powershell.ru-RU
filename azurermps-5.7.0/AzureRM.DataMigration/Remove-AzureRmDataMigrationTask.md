---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566187"
---
# <span data-ttu-id="2d3e1-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2d3e1-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="2d3e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3e1-103">Удаление задачи службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d3e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d3e1-104">SYNTAX</span></span>

### <span data-ttu-id="2d3e1-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d3e1-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2d3e1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d3e1-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2d3e1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d3e1-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2d3e1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d3e1-108">DESCRIPTION</span></span>
<span data-ttu-id="2d3e1-109">Командлет Remove-AzureRmDataMigrationTask удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="2d3e1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d3e1-110">EXAMPLES</span></span>

### <span data-ttu-id="2d3e1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d3e1-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="2d3e1-112">В предыдущем примере задача службы миграции баз данных Azure с именем TestTask из Azure будет удалена с учетом параметра имени задачи.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="2d3e1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2d3e1-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="2d3e1-114">В предыдущем примере задача службы миграции баз данных Azure удаляется на основе объекта PSProjectTask, переданного в.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="2d3e1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d3e1-115">PARAMETERS</span></span>

### <span data-ttu-id="2d3e1-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d3e1-116">-Confirm</span></span>
<span data-ttu-id="2d3e1-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d3e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3e1-118">-DefaultProfile</span></span>
<span data-ttu-id="2d3e1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d3e1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2d3e1-120">-Force</span></span>
<span data-ttu-id="2d3e1-121">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="2d3e1-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2d3e1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d3e1-122">-InputObject</span></span>
<span data-ttu-id="2d3e1-123">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d3e1-124">-Name</span></span>
<span data-ttu-id="2d3e1-125">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d3e1-126">-PassThru</span></span>
<span data-ttu-id="2d3e1-127">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-127">Returns an true/false.</span></span>
<span data-ttu-id="2d3e1-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d3e1-129">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="2d3e1-129">-ProjectName</span></span>
<span data-ttu-id="2d3e1-130">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-130">The name of the project.</span></span>

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

### <span data-ttu-id="2d3e1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3e1-131">-ResourceGroupName</span></span>
<span data-ttu-id="2d3e1-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d3e1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d3e1-133">-ResourceId</span></span>
<span data-ttu-id="2d3e1-134">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="2d3e1-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2d3e1-135">-ServiceName</span></span>
<span data-ttu-id="2d3e1-136">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="2d3e1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d3e1-137">-WhatIf</span></span>
<span data-ttu-id="2d3e1-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d3e1-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d3e1-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2d3e1-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d3e1-140">INPUTS</span></span>

### <span data-ttu-id="2d3e1-141">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="2d3e1-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="2d3e1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2d3e1-142">System.String</span></span>


## <span data-ttu-id="2d3e1-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d3e1-143">OUTPUTS</span></span>

### <span data-ttu-id="2d3e1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d3e1-144">System.Boolean</span></span>


## <span data-ttu-id="2d3e1-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d3e1-145">NOTES</span></span>

## <span data-ttu-id="2d3e1-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d3e1-146">RELATED LINKS</span></span>


