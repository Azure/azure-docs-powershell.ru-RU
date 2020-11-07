---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 8784b69ae5cba2034e02b4f395b479c39d1236f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720522"
---
# <span data-ttu-id="d2ebf-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2ebf-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="d2ebf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ebf-103">Создает пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="d2ebf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2ebf-104">SYNTAX</span></span>

### <span data-ttu-id="d2ebf-105">ByIntegrationAccountAndParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2ebf-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="d2ebf-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="d2ebf-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="d2ebf-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="d2ebf-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="d2ebf-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="d2ebf-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="d2ebf-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ebf-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="d2ebf-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ebf-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ebf-114">DESCRIPTION</span></span>
<span data-ttu-id="d2ebf-115">Командлет **Get-AzIntegrationAccountBatchConfiguration** создает новую конфигурацию пакета в учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="d2ebf-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2ebf-116">EXAMPLES</span></span>

### <span data-ttu-id="d2ebf-117">Пример 1: создание новой конфигурации пакета с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="d2ebf-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="d2ebf-118">Создает новую пакетную конфигурацию с помощью локального файла, расположенного в папке "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="d2ebf-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="d2ebf-119">Пример 2: создание новой конфигурации пакета с помощью строки JSON</span><span class="sxs-lookup"><span data-stu-id="d2ebf-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="d2ebf-120">Создает новую пакетную конфигурацию с помощью строки JSON, содержащейся в разделе "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="d2ebf-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="d2ebf-121">Пример 3: создание новой конфигурации пакета с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="d2ebf-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="d2ebf-122">Создает новую конфигурацию пакета, предоставляя все необходимые параметры вручную.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="d2ebf-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2ebf-123">PARAMETERS</span></span>

### <span data-ttu-id="d2ebf-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="d2ebf-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="d2ebf-125">Определение конфигурации пакета для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="d2ebf-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="d2ebf-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="d2ebf-127">Путь к файлу конфигурации пакета учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="d2ebf-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ebf-128">-BatchGroupName</span></span>
<span data-ttu-id="d2ebf-129">Имя группы пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="d2ebf-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="d2ebf-130">-BatchSize</span></span>
<span data-ttu-id="d2ebf-131">Размер пакета пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="d2ebf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ebf-132">-DefaultProfile</span></span>
<span data-ttu-id="d2ebf-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ebf-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="d2ebf-134">-MessageCount</span></span>
<span data-ttu-id="d2ebf-135">Число сообщений о конфигурации пакетов учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="d2ebf-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d2ebf-136">-Metadata</span></span>
<span data-ttu-id="d2ebf-137">Метаданные пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="d2ebf-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2ebf-138">-Name</span></span>
<span data-ttu-id="d2ebf-139">Название пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ebf-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d2ebf-140">-ParentName</span></span>
<span data-ttu-id="d2ebf-141">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-141">The integration account name.</span></span>

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

### <span data-ttu-id="d2ebf-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d2ebf-142">-ParentObject</span></span>
<span data-ttu-id="d2ebf-143">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ebf-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d2ebf-144">-ParentResourceId</span></span>
<span data-ttu-id="d2ebf-145">Код ресурса конфигурации для пакетной службы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="d2ebf-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ebf-146">-ResourceGroupName</span></span>
<span data-ttu-id="d2ebf-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-147">The resource group name.</span></span>

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

### <span data-ttu-id="d2ebf-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="d2ebf-148">-ScheduleFrequency</span></span>
<span data-ttu-id="d2ebf-149">Периодичность расписания для пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="d2ebf-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="d2ebf-150">-ScheduleInterval</span></span>
<span data-ttu-id="d2ebf-151">Интервал расписания для пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="d2ebf-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="d2ebf-152">-ScheduleStartTime</span></span>
<span data-ttu-id="d2ebf-153">Время начала расписания пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="d2ebf-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="d2ebf-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="d2ebf-155">Часовой пояс расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="d2ebf-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ebf-156">-Confirm</span></span>
<span data-ttu-id="d2ebf-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ebf-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ebf-158">-WhatIf</span></span>
<span data-ttu-id="d2ebf-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2ebf-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ebf-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ebf-161">CommonParameters</span></span>
<span data-ttu-id="d2ebf-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2ebf-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ebf-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ebf-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ebf-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2ebf-164">INPUTS</span></span>

### <span data-ttu-id="d2ebf-165">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d2ebf-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d2ebf-166">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ebf-166">System.String</span></span>

## <span data-ttu-id="d2ebf-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ebf-167">OUTPUTS</span></span>

### <span data-ttu-id="d2ebf-168">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2ebf-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="d2ebf-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2ebf-169">NOTES</span></span>

## <span data-ttu-id="d2ebf-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2ebf-170">RELATED LINKS</span></span>
