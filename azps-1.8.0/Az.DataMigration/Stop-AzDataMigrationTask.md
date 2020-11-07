---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 11ef118483d22451c908fcf7beefb7faae038622
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731012"
---
# <span data-ttu-id="a79ac-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a79ac-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="a79ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a79ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a79ac-103">Останавливает задачу службы миграции баз данных Azure, которая находится в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="a79ac-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="a79ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a79ac-104">SYNTAX</span></span>

### <span data-ttu-id="a79ac-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a79ac-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79ac-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a79ac-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79ac-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a79ac-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79ac-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a79ac-108">DESCRIPTION</span></span>
<span data-ttu-id="a79ac-109">Stop-AzDataMigrationTask командлет прекращает действие миграции базы данных в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="a79ac-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="a79ac-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a79ac-110">EXAMPLES</span></span>

### <span data-ttu-id="a79ac-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a79ac-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="a79ac-112">Ниже приведен пример задачи службы миграции баз данных Azure с именем myDMSTask, связанной с экземпляром службы миграции баз данных Project myDMSProject и Azure с именем TestService</span><span class="sxs-lookup"><span data-stu-id="a79ac-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="a79ac-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a79ac-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="a79ac-114">В предыдущем примере задача службы миграции баз данных Azure передавалась как входной параметр PSProjectTask объекта</span><span class="sxs-lookup"><span data-stu-id="a79ac-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="a79ac-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a79ac-115">PARAMETERS</span></span>

### <span data-ttu-id="a79ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79ac-116">-DefaultProfile</span></span>
<span data-ttu-id="a79ac-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a79ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a79ac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a79ac-118">-InputObject</span></span>
<span data-ttu-id="a79ac-119">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="a79ac-119">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a79ac-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a79ac-120">-Name</span></span>
<span data-ttu-id="a79ac-121">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="a79ac-121">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79ac-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a79ac-122">-PassThru</span></span>
<span data-ttu-id="a79ac-123">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="a79ac-123">Returns an true/false.</span></span>
<span data-ttu-id="a79ac-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a79ac-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a79ac-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="a79ac-125">-ProjectName</span></span>
<span data-ttu-id="a79ac-126">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="a79ac-126">The name of the project.</span></span>

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

### <span data-ttu-id="a79ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="a79ac-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a79ac-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="a79ac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a79ac-129">-ResourceId</span></span>
<span data-ttu-id="a79ac-130">Идентификатор ресурса ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="a79ac-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="a79ac-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a79ac-131">-ServiceName</span></span>
<span data-ttu-id="a79ac-132">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="a79ac-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="a79ac-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a79ac-133">-Confirm</span></span>
<span data-ttu-id="a79ac-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a79ac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a79ac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79ac-135">-WhatIf</span></span>
<span data-ttu-id="a79ac-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a79ac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a79ac-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a79ac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a79ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79ac-138">CommonParameters</span></span>
<span data-ttu-id="a79ac-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a79ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79ac-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a79ac-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79ac-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a79ac-141">INPUTS</span></span>

### <span data-ttu-id="a79ac-142">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="a79ac-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="a79ac-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a79ac-143">System.String</span></span>

## <span data-ttu-id="a79ac-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a79ac-144">OUTPUTS</span></span>

### <span data-ttu-id="a79ac-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a79ac-145">System.Boolean</span></span>

## <span data-ttu-id="a79ac-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="a79ac-146">NOTES</span></span>

## <span data-ttu-id="a79ac-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a79ac-147">RELATED LINKS</span></span>
