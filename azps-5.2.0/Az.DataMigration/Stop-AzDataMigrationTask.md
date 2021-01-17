---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390871"
---
# <span data-ttu-id="d3266-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d3266-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="d3266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3266-102">SYNOPSIS</span></span>
<span data-ttu-id="d3266-103">Остановка задачи службы миграции баз данных Azure, которая находится в запущенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="d3266-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="d3266-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3266-104">SYNTAX</span></span>

### <span data-ttu-id="d3266-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3266-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3266-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3266-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3266-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3266-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3266-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3266-108">DESCRIPTION</span></span>
<span data-ttu-id="d3266-109">Stop-AzDataMigrationTask запуск миграции базы данных прекращается.</span><span class="sxs-lookup"><span data-stu-id="d3266-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="d3266-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3266-110">EXAMPLES</span></span>

### <span data-ttu-id="d3266-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3266-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="d3266-112">В примере выше остановка задачи службы миграции баз данных Azure с именем myDMSTask, связанной с проектом myDMSProject и экземпляром службы миграции баз данных Azure с именем TestService</span><span class="sxs-lookup"><span data-stu-id="d3266-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="d3266-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d3266-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="d3266-114">В примере выше остановка задачи службы миграции баз данных Azure в качестве входного параметра PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="d3266-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="d3266-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3266-115">PARAMETERS</span></span>

### <span data-ttu-id="d3266-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3266-116">-DefaultProfile</span></span>
<span data-ttu-id="d3266-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3266-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3266-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3266-118">-InputObject</span></span>
<span data-ttu-id="d3266-119">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="d3266-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="d3266-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d3266-120">-Name</span></span>
<span data-ttu-id="d3266-121">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="d3266-121">The name of the task.</span></span>

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

### <span data-ttu-id="d3266-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3266-122">-PassThru</span></span>
<span data-ttu-id="d3266-123">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="d3266-123">Returns an true/false.</span></span>
<span data-ttu-id="d3266-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d3266-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3266-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d3266-125">-ProjectName</span></span>
<span data-ttu-id="d3266-126">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="d3266-126">The name of the project.</span></span>

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

### <span data-ttu-id="d3266-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3266-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3266-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3266-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="d3266-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3266-129">-ResourceId</span></span>
<span data-ttu-id="d3266-130">ИД ресурса ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="d3266-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="d3266-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d3266-131">-ServiceName</span></span>
<span data-ttu-id="d3266-132">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="d3266-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="d3266-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3266-133">-Confirm</span></span>
<span data-ttu-id="d3266-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3266-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3266-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3266-135">-WhatIf</span></span>
<span data-ttu-id="d3266-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3266-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3266-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3266-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3266-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3266-138">CommonParameters</span></span>
<span data-ttu-id="d3266-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3266-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3266-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3266-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3266-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3266-141">INPUTS</span></span>

### <span data-ttu-id="d3266-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="d3266-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="d3266-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d3266-143">System.String</span></span>

## <span data-ttu-id="d3266-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3266-144">OUTPUTS</span></span>

### <span data-ttu-id="d3266-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3266-145">System.Boolean</span></span>

## <span data-ttu-id="d3266-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3266-146">NOTES</span></span>

## <span data-ttu-id="d3266-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3266-147">RELATED LINKS</span></span>
