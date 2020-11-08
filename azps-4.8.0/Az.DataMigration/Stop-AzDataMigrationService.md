---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236750"
---
# <span data-ttu-id="ff769-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ff769-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="ff769-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff769-102">SYNOPSIS</span></span>
<span data-ttu-id="ff769-103">Останавливает экземпляр службы миграции баз данных Azure, которая находится в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="ff769-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="ff769-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff769-104">SYNTAX</span></span>

### <span data-ttu-id="ff769-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff769-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff769-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff769-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff769-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff769-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff769-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff769-108">DESCRIPTION</span></span>
<span data-ttu-id="ff769-109">Командлет Stop-AzDataMigrationService останавливает экземпляр службы миграции баз данных Azure, которая находится в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="ff769-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="ff769-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff769-110">EXAMPLES</span></span>

### <span data-ttu-id="ff769-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff769-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="ff769-112">В приведенном выше примере останавливается экземпляр службы миграции баз данных Azure с именем TestService на основе имени службы, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="ff769-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="ff769-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ff769-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="ff769-114">В приведенном выше примере останавливается экземпляр службы миграции баз данных Azure на основе объекта PSDataMigrationService, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="ff769-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="ff769-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff769-115">PARAMETERS</span></span>

### <span data-ttu-id="ff769-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff769-116">-DefaultProfile</span></span>
<span data-ttu-id="ff769-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff769-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff769-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff769-118">-InputObject</span></span>
<span data-ttu-id="ff769-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="ff769-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="ff769-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff769-120">-Name</span></span>
<span data-ttu-id="ff769-121">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="ff769-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ff769-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff769-122">-PassThru</span></span>
<span data-ttu-id="ff769-123">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="ff769-123">Returns an true/false.</span></span>
<span data-ttu-id="ff769-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ff769-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ff769-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff769-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff769-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff769-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff769-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff769-127">-ResourceId</span></span>
<span data-ttu-id="ff769-128">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="ff769-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ff769-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff769-129">-Confirm</span></span>
<span data-ttu-id="ff769-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff769-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff769-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff769-131">-WhatIf</span></span>
<span data-ttu-id="ff769-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff769-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff769-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff769-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff769-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff769-134">CommonParameters</span></span>
<span data-ttu-id="ff769-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff769-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff769-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff769-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff769-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff769-137">INPUTS</span></span>

### <span data-ttu-id="ff769-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ff769-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="ff769-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ff769-139">System.String</span></span>

## <span data-ttu-id="ff769-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff769-140">OUTPUTS</span></span>

### <span data-ttu-id="ff769-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff769-141">System.Boolean</span></span>

## <span data-ttu-id="ff769-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff769-142">NOTES</span></span>

## <span data-ttu-id="ff769-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff769-143">RELATED LINKS</span></span>