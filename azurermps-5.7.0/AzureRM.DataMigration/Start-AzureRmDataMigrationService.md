---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557364"
---
# <span data-ttu-id="1bb57-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1bb57-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="1bb57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bb57-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb57-103">Запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1bb57-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bb57-104">SYNTAX</span></span>

### <span data-ttu-id="1bb57-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1bb57-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1bb57-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bb57-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1bb57-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bb57-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1bb57-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bb57-108">DESCRIPTION</span></span>
<span data-ttu-id="1bb57-109">Командлет Start-AzureRmDataMigrationService запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1bb57-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="1bb57-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bb57-110">EXAMPLES</span></span>

### <span data-ttu-id="1bb57-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1bb57-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="1bb57-112">В приведенном выше примере запускается экземпляр службы миграции базы данных Azure с именем службы тестирования в остановленном состоянии на основе имени службы, переданного в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="1bb57-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="1bb57-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1bb57-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="1bb57-114">В приведенном выше примере запускается экземпляр службы миграции баз данных Azure на основе PSDataMigrationService, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="1bb57-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="1bb57-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bb57-115">PARAMETERS</span></span>

### <span data-ttu-id="1bb57-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bb57-116">-Confirm</span></span>
<span data-ttu-id="1bb57-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1bb57-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb57-118">-DefaultProfile</span></span>
<span data-ttu-id="1bb57-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb57-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb57-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bb57-120">-InputObject</span></span>
<span data-ttu-id="1bb57-121">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="1bb57-121">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb57-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1bb57-122">-Name</span></span>
<span data-ttu-id="1bb57-123">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="1bb57-123">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb57-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bb57-124">-PassThru</span></span>
<span data-ttu-id="1bb57-125">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="1bb57-125">Returns an true/false.</span></span>
<span data-ttu-id="1bb57-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1bb57-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb57-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bb57-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1bb57-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb57-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb57-129">-ResourceId</span></span>
<span data-ttu-id="1bb57-130">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="1bb57-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb57-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb57-131">-WhatIf</span></span>
<span data-ttu-id="1bb57-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1bb57-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb57-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1bb57-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1bb57-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bb57-134">INPUTS</span></span>

### <span data-ttu-id="1bb57-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1bb57-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="1bb57-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb57-136">System.String</span></span>


## <span data-ttu-id="1bb57-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bb57-137">OUTPUTS</span></span>

### <span data-ttu-id="1bb57-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bb57-138">System.Boolean</span></span>


## <span data-ttu-id="1bb57-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bb57-139">NOTES</span></span>

## <span data-ttu-id="1bb57-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bb57-140">RELATED LINKS</span></span>


