---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 5aada0f82b8d2a11486e3dde2f4b806f735979e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568175"
---
# <span data-ttu-id="c26b8-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="c26b8-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="c26b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c26b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c26b8-103">Удаление проекта службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="c26b8-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c26b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c26b8-104">SYNTAX</span></span>

### <span data-ttu-id="c26b8-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c26b8-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c26b8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c26b8-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c26b8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c26b8-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c26b8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26b8-108">DESCRIPTION</span></span>
<span data-ttu-id="c26b8-109">Командлет Remove-AzureRmDataMigrationProject удаляет проект службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="c26b8-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="c26b8-110">При указании параметра DeleteRunningTask удаляются все задачи службы миграции баз данных Azure, связанные с удаляемым проектом.</span><span class="sxs-lookup"><span data-stu-id="c26b8-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="c26b8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c26b8-111">EXAMPLES</span></span>

### <span data-ttu-id="c26b8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c26b8-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="c26b8-113">В приведенном выше примере проект службы миграции баз данных Azure удаляется из Azure на основе имени входного параметра myDMProject</span><span class="sxs-lookup"><span data-stu-id="c26b8-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="c26b8-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c26b8-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="c26b8-115">В приведенном выше примере удаляется проект службы миграции баз данных Azure на основе объекта PSProject в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="c26b8-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="c26b8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c26b8-116">PARAMETERS</span></span>

### <span data-ttu-id="c26b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26b8-117">-DefaultProfile</span></span>
<span data-ttu-id="c26b8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c26b8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c26b8-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="c26b8-119">-DeleteRunningTask</span></span>
<span data-ttu-id="c26b8-120">Удаление любой выполняемой задачи</span><span class="sxs-lookup"><span data-stu-id="c26b8-120">Delete any running task</span></span>

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

### <span data-ttu-id="c26b8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c26b8-121">-Force</span></span>
<span data-ttu-id="c26b8-122">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="c26b8-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c26b8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c26b8-123">-InputObject</span></span>
<span data-ttu-id="c26b8-124">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="c26b8-124">PSProject Object.</span></span>

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

### <span data-ttu-id="c26b8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c26b8-125">-Name</span></span>
<span data-ttu-id="c26b8-126">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="c26b8-126">The name of the project.</span></span>

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

### <span data-ttu-id="c26b8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c26b8-127">-PassThru</span></span>
<span data-ttu-id="c26b8-128">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="c26b8-128">Returns an true/false.</span></span>
<span data-ttu-id="c26b8-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c26b8-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c26b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="c26b8-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c26b8-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="c26b8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c26b8-132">-ResourceId</span></span>
<span data-ttu-id="c26b8-133">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="c26b8-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="c26b8-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c26b8-134">-ServiceName</span></span>
<span data-ttu-id="c26b8-135">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="c26b8-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c26b8-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c26b8-136">-Confirm</span></span>
<span data-ttu-id="c26b8-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c26b8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c26b8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c26b8-138">-WhatIf</span></span>
<span data-ttu-id="c26b8-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c26b8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c26b8-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c26b8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c26b8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26b8-141">CommonParameters</span></span>
<span data-ttu-id="c26b8-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c26b8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26b8-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c26b8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26b8-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c26b8-144">INPUTS</span></span>

### <span data-ttu-id="c26b8-145">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="c26b8-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="c26b8-146">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c26b8-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c26b8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c26b8-147">System.String</span></span>

## <span data-ttu-id="c26b8-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26b8-148">OUTPUTS</span></span>

### <span data-ttu-id="c26b8-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c26b8-149">System.Boolean</span></span>

## <span data-ttu-id="c26b8-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="c26b8-150">NOTES</span></span>

## <span data-ttu-id="c26b8-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c26b8-151">RELATED LINKS</span></span>
