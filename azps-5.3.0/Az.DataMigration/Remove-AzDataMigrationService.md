---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420839"
---
# <span data-ttu-id="660b5-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="660b5-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="660b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="660b5-102">SYNOPSIS</span></span>
<span data-ttu-id="660b5-103">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="660b5-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="660b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="660b5-104">SYNTAX</span></span>

### <span data-ttu-id="660b5-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="660b5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="660b5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="660b5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="660b5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="660b5-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="660b5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="660b5-108">DESCRIPTION</span></span>
<span data-ttu-id="660b5-109">Этот Remove-AzDataMigrationService удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="660b5-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="660b5-110">При этом удаляются все задачи службы миграции баз данных Azure, связанные со удаляемой службой.</span><span class="sxs-lookup"><span data-stu-id="660b5-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="660b5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="660b5-111">EXAMPLES</span></span>

### <span data-ttu-id="660b5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="660b5-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="660b5-113">В примере выше удаляется экземпляр службы миграции баз данных Azure с именем TestService, который содержится в группе ресурсов Azure с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="660b5-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="660b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="660b5-114">PARAMETERS</span></span>

### <span data-ttu-id="660b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660b5-115">-DefaultProfile</span></span>
<span data-ttu-id="660b5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="660b5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="660b5-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="660b5-117">-DeleteRunningTask</span></span>
<span data-ttu-id="660b5-118">Удаление любой запущенной задачи</span><span class="sxs-lookup"><span data-stu-id="660b5-118">Delete any running task</span></span>

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

### <span data-ttu-id="660b5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="660b5-119">-Force</span></span>
<span data-ttu-id="660b5-120">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="660b5-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="660b5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="660b5-121">-InputObject</span></span>
<span data-ttu-id="660b5-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="660b5-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="660b5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="660b5-123">-Name</span></span>
<span data-ttu-id="660b5-124">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="660b5-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="660b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="660b5-125">-PassThru</span></span>
<span data-ttu-id="660b5-126">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="660b5-126">Returns an true/false.</span></span>
<span data-ttu-id="660b5-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="660b5-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="660b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="660b5-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="660b5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="660b5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="660b5-130">-ResourceId</span></span>
<span data-ttu-id="660b5-131">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="660b5-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="660b5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="660b5-132">-Confirm</span></span>
<span data-ttu-id="660b5-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="660b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="660b5-134">-WhatIf</span></span>
<span data-ttu-id="660b5-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660b5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="660b5-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="660b5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="660b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660b5-137">CommonParameters</span></span>
<span data-ttu-id="660b5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660b5-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660b5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660b5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="660b5-140">INPUTS</span></span>

### <span data-ttu-id="660b5-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="660b5-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="660b5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="660b5-142">System.String</span></span>

## <span data-ttu-id="660b5-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="660b5-143">OUTPUTS</span></span>

### <span data-ttu-id="660b5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="660b5-144">System.Boolean</span></span>

## <span data-ttu-id="660b5-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="660b5-145">NOTES</span></span>

## <span data-ttu-id="660b5-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="660b5-146">RELATED LINKS</span></span>
