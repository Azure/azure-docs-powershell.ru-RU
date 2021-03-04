---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 33bc407c5585017bfe98591649a0c30e46adfea4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955939"
---
# <span data-ttu-id="dabde-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="dabde-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="dabde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dabde-102">SYNOPSIS</span></span>
<span data-ttu-id="dabde-103">Остановка задачи службы миграции баз данных Azure, которая запущена.</span><span class="sxs-lookup"><span data-stu-id="dabde-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="dabde-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dabde-104">SYNTAX</span></span>

### <span data-ttu-id="dabde-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dabde-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dabde-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dabde-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dabde-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dabde-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dabde-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dabde-108">DESCRIPTION</span></span>
<span data-ttu-id="dabde-109">Stop-AzDataMigrationTask запуск миграции базы данных прекращается.</span><span class="sxs-lookup"><span data-stu-id="dabde-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="dabde-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dabde-110">EXAMPLES</span></span>

### <span data-ttu-id="dabde-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dabde-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="dabde-112">В примере выше остановка задачи службы миграции баз данных Azure с именем myDMSTask, связанной с проектом myDMSProject и экземпляром службы миграции баз данных Azure с именем TestService</span><span class="sxs-lookup"><span data-stu-id="dabde-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="dabde-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dabde-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="dabde-114">В примере выше остановка задачи службы миграции баз данных Azure в качестве входного параметра PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="dabde-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="dabde-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dabde-115">PARAMETERS</span></span>

### <span data-ttu-id="dabde-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabde-116">-DefaultProfile</span></span>
<span data-ttu-id="dabde-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dabde-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dabde-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dabde-118">-InputObject</span></span>
<span data-ttu-id="dabde-119">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="dabde-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="dabde-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dabde-120">-Name</span></span>
<span data-ttu-id="dabde-121">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="dabde-121">The name of the task.</span></span>

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

### <span data-ttu-id="dabde-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dabde-122">-PassThru</span></span>
<span data-ttu-id="dabde-123">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="dabde-123">Returns an true/false.</span></span>
<span data-ttu-id="dabde-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dabde-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dabde-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="dabde-125">-ProjectName</span></span>
<span data-ttu-id="dabde-126">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="dabde-126">The name of the project.</span></span>

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

### <span data-ttu-id="dabde-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabde-127">-ResourceGroupName</span></span>
<span data-ttu-id="dabde-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dabde-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="dabde-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dabde-129">-ResourceId</span></span>
<span data-ttu-id="dabde-130">ИД ресурса ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="dabde-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="dabde-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dabde-131">-ServiceName</span></span>
<span data-ttu-id="dabde-132">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="dabde-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="dabde-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dabde-133">-Confirm</span></span>
<span data-ttu-id="dabde-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dabde-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dabde-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dabde-135">-WhatIf</span></span>
<span data-ttu-id="dabde-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dabde-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dabde-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dabde-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dabde-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabde-138">CommonParameters</span></span>
<span data-ttu-id="dabde-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabde-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabde-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabde-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabde-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dabde-141">INPUTS</span></span>

### <span data-ttu-id="dabde-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="dabde-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="dabde-143">System.String</span><span class="sxs-lookup"><span data-stu-id="dabde-143">System.String</span></span>

## <span data-ttu-id="dabde-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dabde-144">OUTPUTS</span></span>

### <span data-ttu-id="dabde-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dabde-145">System.Boolean</span></span>

## <span data-ttu-id="dabde-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dabde-146">NOTES</span></span>

## <span data-ttu-id="dabde-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dabde-147">RELATED LINKS</span></span>
