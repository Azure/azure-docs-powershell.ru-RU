---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242821"
---
# <span data-ttu-id="81a42-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="81a42-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="81a42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81a42-102">SYNOPSIS</span></span>
<span data-ttu-id="81a42-103">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="81a42-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="81a42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81a42-104">SYNTAX</span></span>

### <span data-ttu-id="81a42-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81a42-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81a42-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a42-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81a42-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a42-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81a42-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81a42-108">DESCRIPTION</span></span>
<span data-ttu-id="81a42-109">Командлет Remove-AzDataMigrationService удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="81a42-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="81a42-110">При указании параметра DeleteRunningTask удаляются все задачи службы миграции баз данных Azure, связанные с удаляемой службой.</span><span class="sxs-lookup"><span data-stu-id="81a42-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="81a42-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81a42-111">EXAMPLES</span></span>

### <span data-ttu-id="81a42-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="81a42-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="81a42-113">В приведенном выше примере удаляется экземпляр службы миграции баз данных Azure с именем TestService, который содержится в группе ресурсов Azure с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="81a42-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="81a42-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81a42-114">PARAMETERS</span></span>

### <span data-ttu-id="81a42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a42-115">-DefaultProfile</span></span>
<span data-ttu-id="81a42-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81a42-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a42-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="81a42-117">-DeleteRunningTask</span></span>
<span data-ttu-id="81a42-118">Удаление любой выполняемой задачи</span><span class="sxs-lookup"><span data-stu-id="81a42-118">Delete any running task</span></span>

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

### <span data-ttu-id="81a42-119">-Force</span><span class="sxs-lookup"><span data-stu-id="81a42-119">-Force</span></span>
<span data-ttu-id="81a42-120">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="81a42-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="81a42-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81a42-121">-InputObject</span></span>
<span data-ttu-id="81a42-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="81a42-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="81a42-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81a42-123">-Name</span></span>
<span data-ttu-id="81a42-124">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="81a42-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="81a42-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81a42-125">-PassThru</span></span>
<span data-ttu-id="81a42-126">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="81a42-126">Returns an true/false.</span></span>
<span data-ttu-id="81a42-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="81a42-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="81a42-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a42-128">-ResourceGroupName</span></span>
<span data-ttu-id="81a42-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81a42-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="81a42-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81a42-130">-ResourceId</span></span>
<span data-ttu-id="81a42-131">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="81a42-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="81a42-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81a42-132">-Confirm</span></span>
<span data-ttu-id="81a42-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81a42-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a42-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a42-134">-WhatIf</span></span>
<span data-ttu-id="81a42-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81a42-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81a42-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81a42-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a42-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a42-137">CommonParameters</span></span>
<span data-ttu-id="81a42-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81a42-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a42-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a42-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a42-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81a42-140">INPUTS</span></span>

### <span data-ttu-id="81a42-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="81a42-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="81a42-142">System. String</span><span class="sxs-lookup"><span data-stu-id="81a42-142">System.String</span></span>

## <span data-ttu-id="81a42-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81a42-143">OUTPUTS</span></span>

### <span data-ttu-id="81a42-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81a42-144">System.Boolean</span></span>

## <span data-ttu-id="81a42-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="81a42-145">NOTES</span></span>

## <span data-ttu-id="81a42-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81a42-146">RELATED LINKS</span></span>