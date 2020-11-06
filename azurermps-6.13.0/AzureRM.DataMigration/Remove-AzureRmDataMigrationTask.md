---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: 295ac647bcbe04e26e761e4fdf8fe2bd30282218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568922"
---
# <span data-ttu-id="0f8cd-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0f8cd-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="0f8cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8cd-103">Удаление задачи службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f8cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f8cd-104">SYNTAX</span></span>

### <span data-ttu-id="0f8cd-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f8cd-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f8cd-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f8cd-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f8cd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f8cd-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f8cd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f8cd-108">DESCRIPTION</span></span>
<span data-ttu-id="0f8cd-109">Командлет Remove-AzureRmDataMigrationTask удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="0f8cd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f8cd-110">EXAMPLES</span></span>

### <span data-ttu-id="0f8cd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f8cd-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="0f8cd-112">В предыдущем примере задача службы миграции баз данных Azure с именем TestTask из Azure будет удалена с учетом параметра имени задачи.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="0f8cd-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0f8cd-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="0f8cd-114">В предыдущем примере задача службы миграции баз данных Azure удаляется на основе объекта PSProjectTask, переданного в.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="0f8cd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f8cd-115">PARAMETERS</span></span>

### <span data-ttu-id="0f8cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8cd-116">-DefaultProfile</span></span>
<span data-ttu-id="0f8cd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8cd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0f8cd-118">-Force</span></span>
<span data-ttu-id="0f8cd-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="0f8cd-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0f8cd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f8cd-120">-InputObject</span></span>
<span data-ttu-id="0f8cd-121">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="0f8cd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f8cd-122">-Name</span></span>
<span data-ttu-id="0f8cd-123">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-123">The name of the task.</span></span>

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

### <span data-ttu-id="0f8cd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f8cd-124">-PassThru</span></span>
<span data-ttu-id="0f8cd-125">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-125">Returns an true/false.</span></span>
<span data-ttu-id="0f8cd-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f8cd-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="0f8cd-127">-ProjectName</span></span>
<span data-ttu-id="0f8cd-128">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-128">The name of the project.</span></span>

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

### <span data-ttu-id="0f8cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f8cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="0f8cd-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0f8cd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f8cd-131">-ResourceId</span></span>
<span data-ttu-id="0f8cd-132">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="0f8cd-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0f8cd-133">-ServiceName</span></span>
<span data-ttu-id="0f8cd-134">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="0f8cd-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f8cd-135">-Confirm</span></span>
<span data-ttu-id="0f8cd-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f8cd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f8cd-137">-WhatIf</span></span>
<span data-ttu-id="0f8cd-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f8cd-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f8cd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8cd-140">CommonParameters</span></span>
<span data-ttu-id="0f8cd-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f8cd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8cd-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8cd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8cd-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f8cd-143">INPUTS</span></span>

### <span data-ttu-id="0f8cd-144">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="0f8cd-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="0f8cd-145">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f8cd-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0f8cd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0f8cd-146">System.String</span></span>

## <span data-ttu-id="0f8cd-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f8cd-147">OUTPUTS</span></span>

### <span data-ttu-id="0f8cd-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f8cd-148">System.Boolean</span></span>

## <span data-ttu-id="0f8cd-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f8cd-149">NOTES</span></span>

## <span data-ttu-id="0f8cd-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f8cd-150">RELATED LINKS</span></span>
