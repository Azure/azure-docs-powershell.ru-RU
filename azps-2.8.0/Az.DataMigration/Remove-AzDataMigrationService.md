---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 737f723fddd7b351a0f1e9189590a61d83454976
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721228"
---
# <span data-ttu-id="45d48-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="45d48-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="45d48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45d48-102">SYNOPSIS</span></span>
<span data-ttu-id="45d48-103">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="45d48-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="45d48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45d48-104">SYNTAX</span></span>

### <span data-ttu-id="45d48-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45d48-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45d48-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45d48-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45d48-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45d48-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d48-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45d48-108">DESCRIPTION</span></span>
<span data-ttu-id="45d48-109">Командлет Remove-AzDataMigrationService удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="45d48-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="45d48-110">При указании параметра DeleteRunningTask удаляются все задачи службы миграции баз данных Azure, связанные с удаляемой службой.</span><span class="sxs-lookup"><span data-stu-id="45d48-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="45d48-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45d48-111">EXAMPLES</span></span>

### <span data-ttu-id="45d48-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45d48-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="45d48-113">В приведенном выше примере удаляется экземпляр службы миграции баз данных Azure с именем TestService, который содержится в группе ресурсов Azure с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45d48-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="45d48-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45d48-114">PARAMETERS</span></span>

### <span data-ttu-id="45d48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d48-115">-DefaultProfile</span></span>
<span data-ttu-id="45d48-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45d48-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d48-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="45d48-117">-DeleteRunningTask</span></span>
<span data-ttu-id="45d48-118">Удаление любой выполняемой задачи</span><span class="sxs-lookup"><span data-stu-id="45d48-118">Delete any running task</span></span>

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

### <span data-ttu-id="45d48-119">-Force</span><span class="sxs-lookup"><span data-stu-id="45d48-119">-Force</span></span>
<span data-ttu-id="45d48-120">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="45d48-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="45d48-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45d48-121">-InputObject</span></span>
<span data-ttu-id="45d48-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="45d48-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45d48-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45d48-123">-Name</span></span>
<span data-ttu-id="45d48-124">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="45d48-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d48-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45d48-125">-PassThru</span></span>
<span data-ttu-id="45d48-126">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="45d48-126">Returns an true/false.</span></span>
<span data-ttu-id="45d48-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="45d48-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45d48-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d48-128">-ResourceGroupName</span></span>
<span data-ttu-id="45d48-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45d48-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="45d48-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45d48-130">-ResourceId</span></span>
<span data-ttu-id="45d48-131">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="45d48-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="45d48-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45d48-132">-Confirm</span></span>
<span data-ttu-id="45d48-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45d48-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d48-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d48-134">-WhatIf</span></span>
<span data-ttu-id="45d48-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45d48-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45d48-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45d48-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d48-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d48-137">CommonParameters</span></span>
<span data-ttu-id="45d48-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45d48-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d48-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d48-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d48-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45d48-140">INPUTS</span></span>

### <span data-ttu-id="45d48-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="45d48-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="45d48-142">System. String</span><span class="sxs-lookup"><span data-stu-id="45d48-142">System.String</span></span>

## <span data-ttu-id="45d48-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45d48-143">OUTPUTS</span></span>

### <span data-ttu-id="45d48-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45d48-144">System.Boolean</span></span>

## <span data-ttu-id="45d48-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="45d48-145">NOTES</span></span>

## <span data-ttu-id="45d48-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45d48-146">RELATED LINKS</span></span>
