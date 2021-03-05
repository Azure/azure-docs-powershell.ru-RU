---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: b1495f4b7473225697567ca3e9d87e98107ce001
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972755"
---
# <span data-ttu-id="ff209-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff209-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="ff209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff209-102">SYNOPSIS</span></span>
<span data-ttu-id="ff209-103">Изменяет пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="ff209-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff209-104">SYNTAX</span></span>

### <span data-ttu-id="ff209-105">ByIntegrationAccountAndParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff209-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="ff209-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ff209-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="ff209-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ff209-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="ff209-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="ff209-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ff209-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff209-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="ff209-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff209-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff209-114">DESCRIPTION</span></span>
<span data-ttu-id="ff209-115">**Cmdlet Set-AzIntegrationAccountBatchConfiguration** изменяет пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="ff209-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff209-116">EXAMPLES</span></span>

### <span data-ttu-id="ff209-117">Пример 1. Изменение пакетной конфигурации с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="ff209-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="ff209-118">Измените пакетную конфигурацию sampleBatchConfig, используя локальный файл, расположенный в пути к файлу, который содержится в $batchConfigurationFilePath.</span><span class="sxs-lookup"><span data-stu-id="ff209-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="ff209-119">Пример 2. Изменение пакетной конфигурации с помощью строки JSON</span><span class="sxs-lookup"><span data-stu-id="ff209-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="ff209-120">Измените пакетную конфигурацию sampleBatchConfig, используя строку JSON, содержаную в $batchConfigurationContent.</span><span class="sxs-lookup"><span data-stu-id="ff209-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="ff209-121">Пример 3. Изменение пакетной конфигурации с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="ff209-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="ff209-122">Измените пакетную конфигурацию sampleBatchConfig, вручную заявив все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="ff209-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="ff209-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff209-123">PARAMETERS</span></span>

### <span data-ttu-id="ff209-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="ff209-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="ff209-125">Определение конфигурации пакета для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="ff209-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="ff209-127">Путь к файлу пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="ff209-128">-BatchGroupName</span></span>
<span data-ttu-id="ff209-129">Имя группы конфигурации пакета настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="ff209-130">-BatchSize</span></span>
<span data-ttu-id="ff209-131">Размер пакета конфигурации для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff209-132">-DefaultProfile</span></span>
<span data-ttu-id="ff209-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff209-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff209-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff209-134">-InputObject</span></span>
<span data-ttu-id="ff209-135">Пакетная конфигурация учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="ff209-136">-MessageCount</span></span>
<span data-ttu-id="ff209-137">Количество сообщений о пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-138">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="ff209-138">-Metadata</span></span>
<span data-ttu-id="ff209-139">Метаданные пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-140">-Name</span><span class="sxs-lookup"><span data-stu-id="ff209-140">-Name</span></span>
<span data-ttu-id="ff209-141">Имя пакета конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="ff209-142">-ParentName</span></span>
<span data-ttu-id="ff209-143">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff209-144">-ResourceGroupName</span></span>
<span data-ttu-id="ff209-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff209-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff209-146">-ResourceId</span></span>
<span data-ttu-id="ff209-147">ИД пакета конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="ff209-148">-ScheduleFrequency</span></span>
<span data-ttu-id="ff209-149">Частота расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="ff209-150">-ScheduleInterval</span></span>
<span data-ttu-id="ff209-151">Интервал расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="ff209-152">-ScheduleStartTime</span></span>
<span data-ttu-id="ff209-153">Время начала настройки пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="ff209-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="ff209-155">Часовой пояс расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ff209-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff209-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff209-156">-Confirm</span></span>
<span data-ttu-id="ff209-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff209-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff209-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff209-158">-WhatIf</span></span>
<span data-ttu-id="ff209-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff209-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff209-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ff209-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff209-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff209-161">CommonParameters</span></span>
<span data-ttu-id="ff209-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff209-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff209-163">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff209-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff209-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff209-164">INPUTS</span></span>

### <span data-ttu-id="ff209-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff209-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="ff209-166">System.String</span><span class="sxs-lookup"><span data-stu-id="ff209-166">System.String</span></span>

## <span data-ttu-id="ff209-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff209-167">OUTPUTS</span></span>

### <span data-ttu-id="ff209-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff209-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="ff209-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff209-169">NOTES</span></span>

## <span data-ttu-id="ff209-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff209-170">RELATED LINKS</span></span>
