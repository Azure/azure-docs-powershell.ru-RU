---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568176"
---
# <span data-ttu-id="6af03-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6af03-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="6af03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6af03-102">SYNOPSIS</span></span>
<span data-ttu-id="6af03-103">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="6af03-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6af03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6af03-104">SYNTAX</span></span>

### <span data-ttu-id="6af03-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6af03-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6af03-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6af03-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6af03-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6af03-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6af03-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6af03-108">DESCRIPTION</span></span>
<span data-ttu-id="6af03-109">Командлет Remove-AzureRmDataMigrationService удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="6af03-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="6af03-110">При указании параметра DeleteRunningTask удаляются все задачи службы миграции баз данных Azure, связанные с удаляемой службой.</span><span class="sxs-lookup"><span data-stu-id="6af03-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="6af03-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6af03-111">EXAMPLES</span></span>

### <span data-ttu-id="6af03-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6af03-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="6af03-113">В приведенном выше примере удаляется экземпляр службы миграции баз данных Azure с именем TestService, который содержится в группе ресурсов Azure с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6af03-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="6af03-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6af03-114">PARAMETERS</span></span>

### <span data-ttu-id="6af03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af03-115">-DefaultProfile</span></span>
<span data-ttu-id="6af03-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6af03-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6af03-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="6af03-117">-DeleteRunningTask</span></span>
<span data-ttu-id="6af03-118">Удаление любой выполняемой задачи</span><span class="sxs-lookup"><span data-stu-id="6af03-118">Delete any running task</span></span>

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

### <span data-ttu-id="6af03-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6af03-119">-Force</span></span>
<span data-ttu-id="6af03-120">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="6af03-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6af03-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6af03-121">-InputObject</span></span>
<span data-ttu-id="6af03-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="6af03-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="6af03-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6af03-123">-Name</span></span>
<span data-ttu-id="6af03-124">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="6af03-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="6af03-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6af03-125">-PassThru</span></span>
<span data-ttu-id="6af03-126">Возвращает значение истина/ложь.</span><span class="sxs-lookup"><span data-stu-id="6af03-126">Returns an true/false.</span></span>
<span data-ttu-id="6af03-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6af03-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6af03-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af03-128">-ResourceGroupName</span></span>
<span data-ttu-id="6af03-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6af03-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="6af03-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6af03-130">-ResourceId</span></span>
<span data-ttu-id="6af03-131">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="6af03-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="6af03-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6af03-132">-Confirm</span></span>
<span data-ttu-id="6af03-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6af03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6af03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af03-134">-WhatIf</span></span>
<span data-ttu-id="6af03-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6af03-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6af03-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6af03-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6af03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af03-137">CommonParameters</span></span>
<span data-ttu-id="6af03-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6af03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af03-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af03-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af03-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6af03-140">INPUTS</span></span>

### <span data-ttu-id="6af03-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6af03-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="6af03-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6af03-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6af03-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6af03-143">System.String</span></span>

## <span data-ttu-id="6af03-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6af03-144">OUTPUTS</span></span>

### <span data-ttu-id="6af03-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6af03-145">System.Boolean</span></span>

## <span data-ttu-id="6af03-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6af03-146">NOTES</span></span>

## <span data-ttu-id="6af03-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6af03-147">RELATED LINKS</span></span>
