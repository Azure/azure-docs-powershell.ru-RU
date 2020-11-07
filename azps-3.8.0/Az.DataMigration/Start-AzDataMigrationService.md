---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911876"
---
# <span data-ttu-id="db813-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="db813-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="db813-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db813-102">SYNOPSIS</span></span>
<span data-ttu-id="db813-103">Запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="db813-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="db813-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db813-104">SYNTAX</span></span>

### <span data-ttu-id="db813-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db813-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db813-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db813-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db813-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db813-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db813-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db813-108">DESCRIPTION</span></span>
<span data-ttu-id="db813-109">Командлет Start-AzDataMigrationService запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="db813-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="db813-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db813-110">EXAMPLES</span></span>

### <span data-ttu-id="db813-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db813-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="db813-112">В приведенном выше примере запускается экземпляр службы миграции базы данных Azure с именем службы тестирования в остановленном состоянии на основе имени службы, переданного в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="db813-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="db813-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="db813-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="db813-114">В приведенном выше примере запускается экземпляр службы миграции баз данных Azure на основе PSDataMigrationService, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="db813-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="db813-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db813-115">PARAMETERS</span></span>

### <span data-ttu-id="db813-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db813-116">-DefaultProfile</span></span>
<span data-ttu-id="db813-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db813-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db813-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db813-118">-InputObject</span></span>
<span data-ttu-id="db813-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="db813-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="db813-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db813-120">-Name</span></span>
<span data-ttu-id="db813-121">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="db813-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="db813-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db813-122">-PassThru</span></span>
<span data-ttu-id="db813-123">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="db813-123">Returns an true/false.</span></span>
<span data-ttu-id="db813-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="db813-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db813-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db813-125">-ResourceGroupName</span></span>
<span data-ttu-id="db813-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db813-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="db813-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db813-127">-ResourceId</span></span>
<span data-ttu-id="db813-128">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="db813-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="db813-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db813-129">-Confirm</span></span>
<span data-ttu-id="db813-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db813-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db813-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db813-131">-WhatIf</span></span>
<span data-ttu-id="db813-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db813-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db813-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db813-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db813-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db813-134">CommonParameters</span></span>
<span data-ttu-id="db813-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db813-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db813-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db813-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db813-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db813-137">INPUTS</span></span>

### <span data-ttu-id="db813-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="db813-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="db813-139">System. String</span><span class="sxs-lookup"><span data-stu-id="db813-139">System.String</span></span>

## <span data-ttu-id="db813-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db813-140">OUTPUTS</span></span>

### <span data-ttu-id="db813-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db813-141">System.Boolean</span></span>

## <span data-ttu-id="db813-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="db813-142">NOTES</span></span>

## <span data-ttu-id="db813-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db813-143">RELATED LINKS</span></span>
