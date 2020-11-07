---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732863"
---
# <span data-ttu-id="9fce7-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9fce7-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="9fce7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fce7-102">SYNOPSIS</span></span>
<span data-ttu-id="9fce7-103">Останавливает задачу службы миграции баз данных Azure, которая находится в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="9fce7-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fce7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fce7-104">SYNTAX</span></span>

### <span data-ttu-id="9fce7-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fce7-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9fce7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fce7-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9fce7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fce7-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9fce7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fce7-108">DESCRIPTION</span></span>
<span data-ttu-id="9fce7-109">Stop-AzureRmDataMigrationTask командлет прекращает действие миграции базы данных в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="9fce7-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="9fce7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fce7-110">EXAMPLES</span></span>

### <span data-ttu-id="9fce7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9fce7-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="9fce7-112">Ниже приведен пример задачи службы миграции баз данных Azure с именем myDMSTask, связанной с экземпляром службы миграции баз данных Project myDMSProject и Azure с именем TestService</span><span class="sxs-lookup"><span data-stu-id="9fce7-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="9fce7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9fce7-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="9fce7-114">В предыдущем примере задача службы миграции баз данных Azure передавалась как входной параметр PSProjectTask объекта</span><span class="sxs-lookup"><span data-stu-id="9fce7-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="9fce7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fce7-115">PARAMETERS</span></span>

### <span data-ttu-id="9fce7-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fce7-116">-Confirm</span></span>
<span data-ttu-id="9fce7-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9fce7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fce7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fce7-118">-DefaultProfile</span></span>
<span data-ttu-id="9fce7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fce7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fce7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fce7-120">-InputObject</span></span>
<span data-ttu-id="9fce7-121">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="9fce7-121">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fce7-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9fce7-122">-Name</span></span>
<span data-ttu-id="9fce7-123">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="9fce7-123">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fce7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fce7-124">-PassThru</span></span>
<span data-ttu-id="9fce7-125">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="9fce7-125">Returns an true/false.</span></span>
<span data-ttu-id="9fce7-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9fce7-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9fce7-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="9fce7-127">-ProjectName</span></span>
<span data-ttu-id="9fce7-128">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="9fce7-128">The name of the project.</span></span>

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

### <span data-ttu-id="9fce7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fce7-129">-ResourceGroupName</span></span>
<span data-ttu-id="9fce7-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fce7-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="9fce7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fce7-131">-ResourceId</span></span>
<span data-ttu-id="9fce7-132">Идентификатор ресурса ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="9fce7-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="9fce7-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9fce7-133">-ServiceName</span></span>
<span data-ttu-id="9fce7-134">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="9fce7-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="9fce7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fce7-135">-WhatIf</span></span>
<span data-ttu-id="9fce7-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9fce7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fce7-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9fce7-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9fce7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fce7-138">INPUTS</span></span>

### <span data-ttu-id="9fce7-139">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="9fce7-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="9fce7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9fce7-140">System.String</span></span>


## <span data-ttu-id="9fce7-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fce7-141">OUTPUTS</span></span>

### <span data-ttu-id="9fce7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9fce7-142">System.Boolean</span></span>


## <span data-ttu-id="9fce7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fce7-143">NOTES</span></span>

## <span data-ttu-id="9fce7-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fce7-144">RELATED LINKS</span></span>

