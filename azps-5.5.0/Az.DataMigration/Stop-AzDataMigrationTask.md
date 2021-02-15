---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232148"
---
# <span data-ttu-id="86122-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="86122-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="86122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86122-102">SYNOPSIS</span></span>
<span data-ttu-id="86122-103">Остановка задачи службы миграции баз данных Azure, которая находится в запущенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="86122-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="86122-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86122-104">SYNTAX</span></span>

### <span data-ttu-id="86122-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86122-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86122-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86122-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86122-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86122-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86122-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86122-108">DESCRIPTION</span></span>
<span data-ttu-id="86122-109">Stop-AzDataMigrationTask запуск миграции базы данных прекращается.</span><span class="sxs-lookup"><span data-stu-id="86122-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="86122-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86122-110">EXAMPLES</span></span>

### <span data-ttu-id="86122-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="86122-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="86122-112">В примере выше остановка задачи службы миграции баз данных Azure с именем myDMSTask, связанной с проектом myDMSProject и экземпляром службы миграции баз данных Azure с именем TestService</span><span class="sxs-lookup"><span data-stu-id="86122-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="86122-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="86122-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="86122-114">В примере выше остановка задачи службы миграции баз данных Azure в качестве входного параметра PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="86122-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="86122-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86122-115">PARAMETERS</span></span>

### <span data-ttu-id="86122-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86122-116">-DefaultProfile</span></span>
<span data-ttu-id="86122-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86122-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86122-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86122-118">-InputObject</span></span>
<span data-ttu-id="86122-119">Объект PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="86122-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="86122-120">-Name</span><span class="sxs-lookup"><span data-stu-id="86122-120">-Name</span></span>
<span data-ttu-id="86122-121">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="86122-121">The name of the task.</span></span>

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

### <span data-ttu-id="86122-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86122-122">-PassThru</span></span>
<span data-ttu-id="86122-123">Возвращает "истина" или "ложь".</span><span class="sxs-lookup"><span data-stu-id="86122-123">Returns an true/false.</span></span>
<span data-ttu-id="86122-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86122-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86122-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="86122-125">-ProjectName</span></span>
<span data-ttu-id="86122-126">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="86122-126">The name of the project.</span></span>

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

### <span data-ttu-id="86122-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86122-127">-ResourceGroupName</span></span>
<span data-ttu-id="86122-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86122-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="86122-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86122-129">-ResourceId</span></span>
<span data-ttu-id="86122-130">ИД ресурса ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="86122-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="86122-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="86122-131">-ServiceName</span></span>
<span data-ttu-id="86122-132">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="86122-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="86122-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86122-133">-Confirm</span></span>
<span data-ttu-id="86122-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="86122-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86122-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86122-135">-WhatIf</span></span>
<span data-ttu-id="86122-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86122-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86122-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86122-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86122-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86122-138">CommonParameters</span></span>
<span data-ttu-id="86122-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86122-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86122-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86122-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86122-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86122-141">INPUTS</span></span>

### <span data-ttu-id="86122-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="86122-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="86122-143">System.String</span><span class="sxs-lookup"><span data-stu-id="86122-143">System.String</span></span>

## <span data-ttu-id="86122-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86122-144">OUTPUTS</span></span>

### <span data-ttu-id="86122-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86122-145">System.Boolean</span></span>

## <span data-ttu-id="86122-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86122-146">NOTES</span></span>

## <span data-ttu-id="86122-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86122-147">RELATED LINKS</span></span>
