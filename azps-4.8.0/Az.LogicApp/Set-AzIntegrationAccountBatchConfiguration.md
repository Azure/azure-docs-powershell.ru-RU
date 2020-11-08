---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236147"
---
# <span data-ttu-id="fe09b-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe09b-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="fe09b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe09b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe09b-103">Изменение конфигурации пакета учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="fe09b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe09b-104">SYNTAX</span></span>

### <span data-ttu-id="fe09b-105">ByIntegrationAccountAndParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe09b-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="fe09b-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="fe09b-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="fe09b-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="fe09b-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="fe09b-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="fe09b-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="fe09b-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe09b-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="fe09b-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe09b-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe09b-114">DESCRIPTION</span></span>
<span data-ttu-id="fe09b-115">Командлет **Set-AzIntegrationAccountBatchConfiguration** изменяет конфигурацию пакета учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="fe09b-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe09b-116">EXAMPLES</span></span>

### <span data-ttu-id="fe09b-117">Пример 1: изменение конфигурации пакета с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="fe09b-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fe09b-118">Изменение пакетной конфигурации с именем "sampleBatchConfig" с помощью локального файла, расположенного в пути к файлу, который хранится в разделе "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="fe09b-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="fe09b-119">Пример 2: изменение конфигурации пакета с помощью строки JSON</span><span class="sxs-lookup"><span data-stu-id="fe09b-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fe09b-120">Изменение пакетной конфигурации с именем "sampleBatchConfig" с помощью строки JSON, содержащейся в "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="fe09b-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="fe09b-121">Пример 3: изменение конфигурации пакета с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="fe09b-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fe09b-122">Измените пакетную конфигурацию с именем "sampleBatchConfig", указав все необходимые параметры вручную.</span><span class="sxs-lookup"><span data-stu-id="fe09b-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="fe09b-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe09b-123">PARAMETERS</span></span>

### <span data-ttu-id="fe09b-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="fe09b-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="fe09b-125">Определение конфигурации пакета для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="fe09b-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="fe09b-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="fe09b-127">Путь к файлу конфигурации пакета учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="fe09b-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="fe09b-128">-BatchGroupName</span></span>
<span data-ttu-id="fe09b-129">Имя группы пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="fe09b-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="fe09b-130">-BatchSize</span></span>
<span data-ttu-id="fe09b-131">Размер пакета пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="fe09b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe09b-132">-DefaultProfile</span></span>
<span data-ttu-id="fe09b-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe09b-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe09b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe09b-134">-InputObject</span></span>
<span data-ttu-id="fe09b-135">Настройка пакетной учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="fe09b-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="fe09b-136">-MessageCount</span></span>
<span data-ttu-id="fe09b-137">Число сообщений о конфигурации пакетов учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="fe09b-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fe09b-138">-Metadata</span></span>
<span data-ttu-id="fe09b-139">Метаданные пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="fe09b-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe09b-140">-Name</span></span>
<span data-ttu-id="fe09b-141">Название пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="fe09b-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="fe09b-142">-ParentName</span></span>
<span data-ttu-id="fe09b-143">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-143">The integration account name.</span></span>

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

### <span data-ttu-id="fe09b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe09b-144">-ResourceGroupName</span></span>
<span data-ttu-id="fe09b-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe09b-145">The resource group name.</span></span>

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

### <span data-ttu-id="fe09b-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe09b-146">-ResourceId</span></span>
<span data-ttu-id="fe09b-147">Код ресурса конфигурации для пакетной службы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="fe09b-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="fe09b-148">-ScheduleFrequency</span></span>
<span data-ttu-id="fe09b-149">Периодичность расписания для пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="fe09b-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="fe09b-150">-ScheduleInterval</span></span>
<span data-ttu-id="fe09b-151">Интервал расписания для пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="fe09b-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="fe09b-152">-ScheduleStartTime</span></span>
<span data-ttu-id="fe09b-153">Время начала расписания пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="fe09b-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="fe09b-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="fe09b-155">Часовой пояс расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fe09b-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="fe09b-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe09b-156">-Confirm</span></span>
<span data-ttu-id="fe09b-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe09b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe09b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe09b-158">-WhatIf</span></span>
<span data-ttu-id="fe09b-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe09b-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe09b-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe09b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe09b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe09b-161">CommonParameters</span></span>
<span data-ttu-id="fe09b-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe09b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe09b-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe09b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe09b-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe09b-164">INPUTS</span></span>

### <span data-ttu-id="fe09b-165">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe09b-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="fe09b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="fe09b-166">System.String</span></span>

## <span data-ttu-id="fe09b-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe09b-167">OUTPUTS</span></span>

### <span data-ttu-id="fe09b-168">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe09b-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="fe09b-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe09b-169">NOTES</span></span>

## <span data-ttu-id="fe09b-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe09b-170">RELATED LINKS</span></span>
