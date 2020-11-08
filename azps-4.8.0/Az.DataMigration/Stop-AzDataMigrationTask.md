---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244571"
---
# <span data-ttu-id="b2f0e-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b2f0e-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="b2f0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f0e-103">Останавливает задачу службы миграции баз данных Azure, которая находится в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="b2f0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2f0e-104">SYNTAX</span></span>

### <span data-ttu-id="b2f0e-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2f0e-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f0e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f0e-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f0e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f0e-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f0e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2f0e-108">DESCRIPTION</span></span>
<span data-ttu-id="b2f0e-109">Stop-AzDataMigrationTask командлет прекращает действие миграции базы данных в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="b2f0e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2f0e-110">EXAMPLES</span></span>

### <span data-ttu-id="b2f0e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2f0e-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="b2f0e-112">Ниже приведен пример задачи службы миграции баз данных Azure с именем myDMSTask, связанной с экземпляром службы миграции баз данных Project myDMSProject и Azure с именем TestService</span><span class="sxs-lookup"><span data-stu-id="b2f0e-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="b2f0e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b2f0e-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="b2f0e-114">В предыдущем примере задача службы миграции баз данных Azure передавалась как входной параметр PSProjectTask объекта</span><span class="sxs-lookup"><span data-stu-id="b2f0e-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="b2f0e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2f0e-115">PARAMETERS</span></span>

### <span data-ttu-id="b2f0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f0e-116">-DefaultProfile</span></span>
<span data-ttu-id="b2f0e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2f0e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f0e-118">-InputObject</span></span>
<span data-ttu-id="b2f0e-119">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="b2f0e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2f0e-120">-Name</span></span>
<span data-ttu-id="b2f0e-121">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-121">The name of the task.</span></span>

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

### <span data-ttu-id="b2f0e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2f0e-122">-PassThru</span></span>
<span data-ttu-id="b2f0e-123">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-123">Returns an true/false.</span></span>
<span data-ttu-id="b2f0e-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2f0e-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="b2f0e-125">-ProjectName</span></span>
<span data-ttu-id="b2f0e-126">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-126">The name of the project.</span></span>

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

### <span data-ttu-id="b2f0e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f0e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2f0e-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="b2f0e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f0e-129">-ResourceId</span></span>
<span data-ttu-id="b2f0e-130">Идентификатор ресурса ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="b2f0e-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b2f0e-131">-ServiceName</span></span>
<span data-ttu-id="b2f0e-132">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="b2f0e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2f0e-133">-Confirm</span></span>
<span data-ttu-id="b2f0e-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f0e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f0e-135">-WhatIf</span></span>
<span data-ttu-id="b2f0e-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f0e-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f0e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f0e-138">CommonParameters</span></span>
<span data-ttu-id="b2f0e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f0e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f0e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f0e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2f0e-141">INPUTS</span></span>

### <span data-ttu-id="b2f0e-142">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="b2f0e-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="b2f0e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b2f0e-143">System.String</span></span>

## <span data-ttu-id="b2f0e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2f0e-144">OUTPUTS</span></span>

### <span data-ttu-id="b2f0e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2f0e-145">System.Boolean</span></span>

## <span data-ttu-id="b2f0e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2f0e-146">NOTES</span></span>

## <span data-ttu-id="b2f0e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2f0e-147">RELATED LINKS</span></span>
