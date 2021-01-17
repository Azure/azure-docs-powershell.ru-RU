---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420807"
---
# <span data-ttu-id="fb0ab-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fb0ab-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="fb0ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb0ab-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0ab-103">Остановка экземпляра службы миграции баз данных Azure, которая находится в запущенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="fb0ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb0ab-104">SYNTAX</span></span>

### <span data-ttu-id="fb0ab-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb0ab-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb0ab-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb0ab-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb0ab-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb0ab-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb0ab-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb0ab-108">DESCRIPTION</span></span>
<span data-ttu-id="fb0ab-109">Этот Stop-AzDataMigrationService останавливает экземпляр службы миграции баз данных Azure, запущенный в состоянии.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="fb0ab-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb0ab-110">EXAMPLES</span></span>

### <span data-ttu-id="fb0ab-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb0ab-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="fb0ab-112">В примере выше остановка экземпляра службы миграции баз данных Azure TestService на основе имени службы, переданного в качестве входного параметра</span><span class="sxs-lookup"><span data-stu-id="fb0ab-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="fb0ab-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fb0ab-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="fb0ab-114">В примере выше экземпляр службы миграции баз данных Azure останавливается на основе объекта PSDataMigrationService, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="fb0ab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb0ab-115">PARAMETERS</span></span>

### <span data-ttu-id="fb0ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0ab-116">-DefaultProfile</span></span>
<span data-ttu-id="fb0ab-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb0ab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb0ab-118">-InputObject</span></span>
<span data-ttu-id="fb0ab-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="fb0ab-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fb0ab-120">-Name</span></span>
<span data-ttu-id="fb0ab-121">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="fb0ab-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb0ab-122">-PassThru</span></span>
<span data-ttu-id="fb0ab-123">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="fb0ab-123">Returns an true/false.</span></span>
<span data-ttu-id="fb0ab-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb0ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb0ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="fb0ab-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb0ab-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0ab-127">-ResourceId</span></span>
<span data-ttu-id="fb0ab-128">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="fb0ab-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb0ab-129">-Confirm</span></span>
<span data-ttu-id="fb0ab-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb0ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb0ab-131">-WhatIf</span></span>
<span data-ttu-id="fb0ab-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb0ab-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb0ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0ab-134">CommonParameters</span></span>
<span data-ttu-id="fb0ab-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb0ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0ab-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb0ab-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0ab-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb0ab-137">INPUTS</span></span>

### <span data-ttu-id="fb0ab-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fb0ab-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="fb0ab-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fb0ab-139">System.String</span></span>

## <span data-ttu-id="fb0ab-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb0ab-140">OUTPUTS</span></span>

### <span data-ttu-id="fb0ab-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb0ab-141">System.Boolean</span></span>

## <span data-ttu-id="fb0ab-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb0ab-142">NOTES</span></span>

## <span data-ttu-id="fb0ab-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb0ab-143">RELATED LINKS</span></span>
