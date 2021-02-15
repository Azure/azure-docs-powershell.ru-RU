---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232161"
---
# <span data-ttu-id="5892f-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5892f-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="5892f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5892f-102">SYNOPSIS</span></span>
<span data-ttu-id="5892f-103">Запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5892f-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="5892f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5892f-104">SYNTAX</span></span>

### <span data-ttu-id="5892f-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5892f-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5892f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5892f-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5892f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5892f-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5892f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5892f-108">DESCRIPTION</span></span>
<span data-ttu-id="5892f-109">С Start-AzDataMigrationService запускается экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5892f-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="5892f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5892f-110">EXAMPLES</span></span>

### <span data-ttu-id="5892f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5892f-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="5892f-112">В примере выше экземпляр службы миграции баз данных Azure с именем Test Service запускается в остановленном состоянии на основе имени службы, переданного в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="5892f-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="5892f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5892f-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="5892f-114">В примере выше запускается экземпляр службы миграции баз данных Azure на основе PSDataMigrationService, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="5892f-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="5892f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5892f-115">PARAMETERS</span></span>

### <span data-ttu-id="5892f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5892f-116">-DefaultProfile</span></span>
<span data-ttu-id="5892f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5892f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5892f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5892f-118">-InputObject</span></span>
<span data-ttu-id="5892f-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5892f-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="5892f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5892f-120">-Name</span></span>
<span data-ttu-id="5892f-121">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="5892f-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="5892f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5892f-122">-PassThru</span></span>
<span data-ttu-id="5892f-123">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="5892f-123">Returns an true/false.</span></span>
<span data-ttu-id="5892f-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5892f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5892f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5892f-125">-ResourceGroupName</span></span>
<span data-ttu-id="5892f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5892f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="5892f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5892f-127">-ResourceId</span></span>
<span data-ttu-id="5892f-128">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="5892f-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="5892f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5892f-129">-Confirm</span></span>
<span data-ttu-id="5892f-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5892f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5892f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5892f-131">-WhatIf</span></span>
<span data-ttu-id="5892f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5892f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5892f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5892f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5892f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5892f-134">CommonParameters</span></span>
<span data-ttu-id="5892f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5892f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5892f-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5892f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5892f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5892f-137">INPUTS</span></span>

### <span data-ttu-id="5892f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5892f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="5892f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5892f-139">System.String</span></span>

## <span data-ttu-id="5892f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5892f-140">OUTPUTS</span></span>

### <span data-ttu-id="5892f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5892f-141">System.Boolean</span></span>

## <span data-ttu-id="5892f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5892f-142">NOTES</span></span>

## <span data-ttu-id="5892f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5892f-143">RELATED LINKS</span></span>
