---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566637"
---
# <span data-ttu-id="fe1d5-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fe1d5-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="fe1d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1d5-103">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe1d5-104">SYNTAX</span></span>

### <span data-ttu-id="fe1d5-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe1d5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fe1d5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe1d5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fe1d5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe1d5-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fe1d5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1d5-108">DESCRIPTION</span></span>
<span data-ttu-id="fe1d5-109">Командлет Remove-AzureRmDataMigrationService удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="fe1d5-110">При указании параметра DeleteRunningTask удаляются все задачи службы миграции баз данных Azure, связанные с удаляемой службой.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="fe1d5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe1d5-111">EXAMPLES</span></span>

### <span data-ttu-id="fe1d5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe1d5-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="fe1d5-113">В приведенном выше примере удаляется экземпляр службы миграции баз данных Azure с именем TestService, который содержится в группе ресурсов Azure с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="fe1d5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe1d5-114">PARAMETERS</span></span>

### <span data-ttu-id="fe1d5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe1d5-115">-Confirm</span></span>
<span data-ttu-id="fe1d5-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe1d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1d5-117">-DefaultProfile</span></span>
<span data-ttu-id="fe1d5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe1d5-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="fe1d5-119">-DeleteRunningTask</span></span>
<span data-ttu-id="fe1d5-120">Удаление любой выполняемой задачи</span><span class="sxs-lookup"><span data-stu-id="fe1d5-120">Delete any running task</span></span>

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

### <span data-ttu-id="fe1d5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fe1d5-121">-Force</span></span>
<span data-ttu-id="fe1d5-122">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="fe1d5-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fe1d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe1d5-123">-InputObject</span></span>
<span data-ttu-id="fe1d5-124">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-124">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="fe1d5-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe1d5-125">-Name</span></span>
<span data-ttu-id="fe1d5-126">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-126">The name of the Data Migration Service.</span></span>

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

### <span data-ttu-id="fe1d5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe1d5-127">-PassThru</span></span>
<span data-ttu-id="fe1d5-128">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-128">Returns an true/false.</span></span>
<span data-ttu-id="fe1d5-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe1d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1d5-130">-ResourceGroupName</span></span>
<span data-ttu-id="fe1d5-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe1d5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe1d5-132">-ResourceId</span></span>
<span data-ttu-id="fe1d5-133">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-133">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="fe1d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1d5-134">-WhatIf</span></span>
<span data-ttu-id="fe1d5-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe1d5-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe1d5-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="fe1d5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe1d5-137">INPUTS</span></span>

### <span data-ttu-id="fe1d5-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fe1d5-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="fe1d5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fe1d5-139">System.String</span></span>


## <span data-ttu-id="fe1d5-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1d5-140">OUTPUTS</span></span>

### <span data-ttu-id="fe1d5-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe1d5-141">System.Boolean</span></span>


## <span data-ttu-id="fe1d5-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe1d5-142">NOTES</span></span>

## <span data-ttu-id="fe1d5-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe1d5-143">RELATED LINKS</span></span>


