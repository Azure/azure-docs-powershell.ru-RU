---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409804"
---
# <span data-ttu-id="bb681-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb681-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="bb681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb681-102">SYNOPSIS</span></span>
<span data-ttu-id="bb681-103">Изменяет пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="bb681-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb681-104">SYNTAX</span></span>

### <span data-ttu-id="bb681-105">ByIntegrationAccountAndParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb681-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="bb681-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="bb681-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="bb681-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="bb681-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="bb681-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="bb681-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="bb681-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb681-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="bb681-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb681-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb681-114">DESCRIPTION</span></span>
<span data-ttu-id="bb681-115">**Cmdlet Set-AzIntegrationAccountBatchConfiguration** изменяет пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="bb681-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb681-116">EXAMPLES</span></span>

### <span data-ttu-id="bb681-117">Пример 1. Изменение пакетной конфигурации с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="bb681-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="bb681-118">Измените пакетную конфигурацию sampleBatchConfig, используя локальный файл, расположенный в пути к файлу, который содержится в $batchConfigurationFilePath.</span><span class="sxs-lookup"><span data-stu-id="bb681-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="bb681-119">Пример 2. Изменение пакетной конфигурации с помощью строки JSON</span><span class="sxs-lookup"><span data-stu-id="bb681-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="bb681-120">Измените конфигурацию пакета sampleBatchConfig, используя строку JSON, содержаную в $batchConfigurationContent.</span><span class="sxs-lookup"><span data-stu-id="bb681-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="bb681-121">Пример 3. Изменение пакетной конфигурации с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="bb681-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="bb681-122">Измените пакетную конфигурацию sampleBatchConfig, вручную заявив все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="bb681-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="bb681-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb681-123">PARAMETERS</span></span>

### <span data-ttu-id="bb681-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="bb681-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="bb681-125">Определение пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="bb681-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="bb681-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="bb681-127">Путь к файлу пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="bb681-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="bb681-128">-BatchGroupName</span></span>
<span data-ttu-id="bb681-129">Имя группы конфигурации пакета настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="bb681-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="bb681-130">-BatchSize</span></span>
<span data-ttu-id="bb681-131">Размер пакета конфигурации для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="bb681-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb681-132">-DefaultProfile</span></span>
<span data-ttu-id="bb681-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb681-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb681-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb681-134">-InputObject</span></span>
<span data-ttu-id="bb681-135">Пакетная конфигурация учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="bb681-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="bb681-136">-MessageCount</span></span>
<span data-ttu-id="bb681-137">Количество сообщений о пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="bb681-138">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="bb681-138">-Metadata</span></span>
<span data-ttu-id="bb681-139">Метаданные пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="bb681-140">-Name</span><span class="sxs-lookup"><span data-stu-id="bb681-140">-Name</span></span>
<span data-ttu-id="bb681-141">Имя пакета конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="bb681-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="bb681-142">-ParentName</span></span>
<span data-ttu-id="bb681-143">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-143">The integration account name.</span></span>

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

### <span data-ttu-id="bb681-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb681-144">-ResourceGroupName</span></span>
<span data-ttu-id="bb681-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb681-145">The resource group name.</span></span>

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

### <span data-ttu-id="bb681-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb681-146">-ResourceId</span></span>
<span data-ttu-id="bb681-147">ИД пакета конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="bb681-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="bb681-148">-ScheduleFrequency</span></span>
<span data-ttu-id="bb681-149">Частота расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="bb681-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="bb681-150">-ScheduleInterval</span></span>
<span data-ttu-id="bb681-151">Интервал расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="bb681-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="bb681-152">-ScheduleStartTime</span></span>
<span data-ttu-id="bb681-153">Время начала настройки пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="bb681-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="bb681-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="bb681-155">Часовой пояс расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb681-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="bb681-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb681-156">-Confirm</span></span>
<span data-ttu-id="bb681-157">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bb681-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb681-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb681-158">-WhatIf</span></span>
<span data-ttu-id="bb681-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb681-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb681-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bb681-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb681-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb681-161">CommonParameters</span></span>
<span data-ttu-id="bb681-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb681-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb681-163">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb681-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb681-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb681-164">INPUTS</span></span>

### <span data-ttu-id="bb681-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb681-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="bb681-166">System.String</span><span class="sxs-lookup"><span data-stu-id="bb681-166">System.String</span></span>

## <span data-ttu-id="bb681-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb681-167">OUTPUTS</span></span>

### <span data-ttu-id="bb681-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb681-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="bb681-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb681-169">NOTES</span></span>

## <span data-ttu-id="bb681-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb681-170">RELATED LINKS</span></span>
