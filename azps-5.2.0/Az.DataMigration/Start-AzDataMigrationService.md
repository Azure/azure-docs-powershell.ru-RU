---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328975"
---
# <span data-ttu-id="e6a76-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e6a76-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="e6a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a76-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a76-103">Запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e6a76-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="e6a76-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6a76-104">SYNTAX</span></span>

### <span data-ttu-id="e6a76-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6a76-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a76-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6a76-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a76-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6a76-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a76-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6a76-108">DESCRIPTION</span></span>
<span data-ttu-id="e6a76-109">С Start-AzDataMigrationService запускается экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e6a76-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="e6a76-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6a76-110">EXAMPLES</span></span>

### <span data-ttu-id="e6a76-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6a76-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="e6a76-112">В примере выше экземпляр службы миграции баз данных Azure с именем Test Service запускается в остановленном состоянии на основе имени службы, переданного в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="e6a76-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="e6a76-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e6a76-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="e6a76-114">В примере выше запускается экземпляр службы миграции баз данных Azure на основе PSDataMigrationService, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="e6a76-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="e6a76-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6a76-115">PARAMETERS</span></span>

### <span data-ttu-id="e6a76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a76-116">-DefaultProfile</span></span>
<span data-ttu-id="e6a76-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a76-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a76-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6a76-118">-InputObject</span></span>
<span data-ttu-id="e6a76-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e6a76-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="e6a76-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e6a76-120">-Name</span></span>
<span data-ttu-id="e6a76-121">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="e6a76-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e6a76-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6a76-122">-PassThru</span></span>
<span data-ttu-id="e6a76-123">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="e6a76-123">Returns an true/false.</span></span>
<span data-ttu-id="e6a76-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e6a76-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6a76-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a76-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6a76-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6a76-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6a76-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6a76-127">-ResourceId</span></span>
<span data-ttu-id="e6a76-128">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="e6a76-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e6a76-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6a76-129">-Confirm</span></span>
<span data-ttu-id="e6a76-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a76-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a76-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a76-131">-WhatIf</span></span>
<span data-ttu-id="e6a76-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a76-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6a76-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e6a76-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a76-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a76-134">CommonParameters</span></span>
<span data-ttu-id="e6a76-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a76-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a76-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a76-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a76-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6a76-137">INPUTS</span></span>

### <span data-ttu-id="e6a76-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e6a76-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="e6a76-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e6a76-139">System.String</span></span>

## <span data-ttu-id="e6a76-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6a76-140">OUTPUTS</span></span>

### <span data-ttu-id="e6a76-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6a76-141">System.Boolean</span></span>

## <span data-ttu-id="e6a76-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6a76-142">NOTES</span></span>

## <span data-ttu-id="e6a76-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6a76-143">RELATED LINKS</span></span>
