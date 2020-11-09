---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244479"
---
# <span data-ttu-id="e08ff-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e08ff-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="e08ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e08ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e08ff-103">Создает пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="e08ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e08ff-104">SYNTAX</span></span>

### <span data-ttu-id="e08ff-105">ByIntegrationAccountAndParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e08ff-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="e08ff-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e08ff-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="e08ff-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e08ff-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="e08ff-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="e08ff-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e08ff-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ff-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="e08ff-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08ff-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e08ff-114">DESCRIPTION</span></span>
<span data-ttu-id="e08ff-115">Командлет **Get-AzIntegrationAccountBatchConfiguration** создает новую конфигурацию пакета в учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="e08ff-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e08ff-116">EXAMPLES</span></span>

### <span data-ttu-id="e08ff-117">Пример 1: создание новой конфигурации пакета с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="e08ff-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e08ff-118">Создает новую пакетную конфигурацию с помощью локального файла, расположенного в папке "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="e08ff-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="e08ff-119">Пример 2: создание новой конфигурации пакета с помощью строки JSON</span><span class="sxs-lookup"><span data-stu-id="e08ff-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e08ff-120">Создает новую пакетную конфигурацию с помощью строки JSON, содержащейся в разделе "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="e08ff-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="e08ff-121">Пример 3: создание новой конфигурации пакета с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="e08ff-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e08ff-122">Создает новую конфигурацию пакета, предоставляя все необходимые параметры вручную.</span><span class="sxs-lookup"><span data-stu-id="e08ff-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="e08ff-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e08ff-123">PARAMETERS</span></span>

### <span data-ttu-id="e08ff-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="e08ff-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="e08ff-125">Определение конфигурации пакета для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="e08ff-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="e08ff-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="e08ff-127">Путь к файлу конфигурации пакета учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="e08ff-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="e08ff-128">-BatchGroupName</span></span>
<span data-ttu-id="e08ff-129">Имя группы пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="e08ff-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="e08ff-130">-BatchSize</span></span>
<span data-ttu-id="e08ff-131">Размер пакета пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="e08ff-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08ff-132">-DefaultProfile</span></span>
<span data-ttu-id="e08ff-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e08ff-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e08ff-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="e08ff-134">-MessageCount</span></span>
<span data-ttu-id="e08ff-135">Число сообщений о конфигурации пакетов учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="e08ff-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e08ff-136">-Metadata</span></span>
<span data-ttu-id="e08ff-137">Метаданные пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="e08ff-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e08ff-138">-Name</span></span>
<span data-ttu-id="e08ff-139">Название пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-139">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="e08ff-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e08ff-140">-ParentName</span></span>
<span data-ttu-id="e08ff-141">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-141">The integration account name.</span></span>

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

### <span data-ttu-id="e08ff-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e08ff-142">-ParentObject</span></span>
<span data-ttu-id="e08ff-143">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-143">An integration account object.</span></span>

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

### <span data-ttu-id="e08ff-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e08ff-144">-ParentResourceId</span></span>
<span data-ttu-id="e08ff-145">Код ресурса конфигурации для пакетной службы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="e08ff-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e08ff-146">-ResourceGroupName</span></span>
<span data-ttu-id="e08ff-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e08ff-147">The resource group name.</span></span>

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

### <span data-ttu-id="e08ff-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="e08ff-148">-ScheduleFrequency</span></span>
<span data-ttu-id="e08ff-149">Периодичность расписания для пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="e08ff-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="e08ff-150">-ScheduleInterval</span></span>
<span data-ttu-id="e08ff-151">Интервал расписания для пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="e08ff-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="e08ff-152">-ScheduleStartTime</span></span>
<span data-ttu-id="e08ff-153">Время начала расписания пакетной конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="e08ff-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="e08ff-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="e08ff-155">Часовой пояс расписания пакетной настройки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e08ff-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="e08ff-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e08ff-156">-Confirm</span></span>
<span data-ttu-id="e08ff-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e08ff-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08ff-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08ff-158">-WhatIf</span></span>
<span data-ttu-id="e08ff-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e08ff-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e08ff-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e08ff-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08ff-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08ff-161">CommonParameters</span></span>
<span data-ttu-id="e08ff-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e08ff-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08ff-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e08ff-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08ff-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e08ff-164">INPUTS</span></span>

### <span data-ttu-id="e08ff-165">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e08ff-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="e08ff-166">System. String</span><span class="sxs-lookup"><span data-stu-id="e08ff-166">System.String</span></span>

## <span data-ttu-id="e08ff-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e08ff-167">OUTPUTS</span></span>

### <span data-ttu-id="e08ff-168">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e08ff-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="e08ff-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="e08ff-169">NOTES</span></span>

## <span data-ttu-id="e08ff-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e08ff-170">RELATED LINKS</span></span>