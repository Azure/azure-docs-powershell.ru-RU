---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214913"
---
# <span data-ttu-id="3fd45-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3fd45-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="3fd45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fd45-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd45-103">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd45-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="3fd45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3fd45-104">SYNTAX</span></span>

### <span data-ttu-id="3fd45-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3fd45-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd45-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd45-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd45-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd45-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd45-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fd45-108">DESCRIPTION</span></span>
<span data-ttu-id="3fd45-109">Этот Remove-AzDataMigrationService удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd45-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="3fd45-110">При этом удаляются все задачи службы миграции баз данных Azure, связанные со удаляемой службой.</span><span class="sxs-lookup"><span data-stu-id="3fd45-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="3fd45-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3fd45-111">EXAMPLES</span></span>

### <span data-ttu-id="3fd45-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3fd45-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="3fd45-113">В примере выше удаляется экземпляр службы миграции баз данных Azure с именем TestService, который содержится в группе ресурсов Azure с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3fd45-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="3fd45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fd45-114">PARAMETERS</span></span>

### <span data-ttu-id="3fd45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd45-115">-DefaultProfile</span></span>
<span data-ttu-id="3fd45-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fd45-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="3fd45-117">-DeleteRunningTask</span></span>
<span data-ttu-id="3fd45-118">Удаление любой запущенной задачи</span><span class="sxs-lookup"><span data-stu-id="3fd45-118">Delete any running task</span></span>

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

### <span data-ttu-id="3fd45-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3fd45-119">-Force</span></span>
<span data-ttu-id="3fd45-120">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="3fd45-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3fd45-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fd45-121">-InputObject</span></span>
<span data-ttu-id="3fd45-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="3fd45-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="3fd45-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3fd45-123">-Name</span></span>
<span data-ttu-id="3fd45-124">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="3fd45-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="3fd45-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fd45-125">-PassThru</span></span>
<span data-ttu-id="3fd45-126">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="3fd45-126">Returns an true/false.</span></span>
<span data-ttu-id="3fd45-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3fd45-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fd45-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd45-128">-ResourceGroupName</span></span>
<span data-ttu-id="3fd45-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3fd45-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3fd45-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd45-130">-ResourceId</span></span>
<span data-ttu-id="3fd45-131">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="3fd45-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="3fd45-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fd45-132">-Confirm</span></span>
<span data-ttu-id="3fd45-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3fd45-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fd45-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd45-134">-WhatIf</span></span>
<span data-ttu-id="3fd45-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd45-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd45-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3fd45-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fd45-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd45-137">CommonParameters</span></span>
<span data-ttu-id="3fd45-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd45-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd45-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd45-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd45-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fd45-140">INPUTS</span></span>

### <span data-ttu-id="3fd45-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3fd45-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="3fd45-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3fd45-142">System.String</span></span>

## <span data-ttu-id="3fd45-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3fd45-143">OUTPUTS</span></span>

### <span data-ttu-id="3fd45-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fd45-144">System.Boolean</span></span>

## <span data-ttu-id="3fd45-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3fd45-145">NOTES</span></span>

## <span data-ttu-id="3fd45-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fd45-146">RELATED LINKS</span></span>
