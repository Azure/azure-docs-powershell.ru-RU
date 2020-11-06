---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569864"
---
# <span data-ttu-id="e2f8d-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e2f8d-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="e2f8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f8d-103">Запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2f8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2f8d-104">SYNTAX</span></span>

### <span data-ttu-id="e2f8d-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2f8d-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f8d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2f8d-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f8d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2f8d-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2f8d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f8d-108">DESCRIPTION</span></span>
<span data-ttu-id="e2f8d-109">Командлет Start-AzureRmDataMigrationService запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="e2f8d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2f8d-110">EXAMPLES</span></span>

### <span data-ttu-id="e2f8d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2f8d-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="e2f8d-112">В приведенном выше примере запускается экземпляр службы миграции базы данных Azure с именем службы тестирования в остановленном состоянии на основе имени службы, переданного в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="e2f8d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2f8d-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="e2f8d-114">В приведенном выше примере запускается экземпляр службы миграции баз данных Azure на основе PSDataMigrationService, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="e2f8d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2f8d-115">PARAMETERS</span></span>

### <span data-ttu-id="e2f8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f8d-116">-DefaultProfile</span></span>
<span data-ttu-id="e2f8d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2f8d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f8d-118">-InputObject</span></span>
<span data-ttu-id="e2f8d-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="e2f8d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2f8d-120">-Name</span></span>
<span data-ttu-id="e2f8d-121">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e2f8d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2f8d-122">-PassThru</span></span>
<span data-ttu-id="e2f8d-123">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-123">Returns an true/false.</span></span>
<span data-ttu-id="e2f8d-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2f8d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f8d-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2f8d-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2f8d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f8d-127">-ResourceId</span></span>
<span data-ttu-id="e2f8d-128">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e2f8d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f8d-129">-Confirm</span></span>
<span data-ttu-id="e2f8d-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f8d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f8d-131">-WhatIf</span></span>
<span data-ttu-id="e2f8d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f8d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f8d-134">CommonParameters</span></span>
<span data-ttu-id="e2f8d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2f8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f8d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f8d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f8d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2f8d-137">INPUTS</span></span>

### <span data-ttu-id="e2f8d-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e2f8d-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="e2f8d-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2f8d-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e2f8d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e2f8d-140">System.String</span></span>

## <span data-ttu-id="e2f8d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f8d-141">OUTPUTS</span></span>

### <span data-ttu-id="e2f8d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2f8d-142">System.Boolean</span></span>

## <span data-ttu-id="e2f8d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2f8d-143">NOTES</span></span>

## <span data-ttu-id="e2f8d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2f8d-144">RELATED LINKS</span></span>
