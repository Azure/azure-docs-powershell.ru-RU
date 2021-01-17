---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392591"
---
# <span data-ttu-id="84e9b-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="84e9b-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="84e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="84e9b-103">Создает экземпляр поставщика для указанной подписки, группы ресурсов, имени sapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="84e9b-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="84e9b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84e9b-104">SYNTAX</span></span>

### <span data-ttu-id="84e9b-105">ByString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84e9b-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="84e9b-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="84e9b-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="84e9b-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="84e9b-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84e9b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84e9b-108">DESCRIPTION</span></span>
<span data-ttu-id="84e9b-109">Создает экземпляр поставщика для указанной подписки, группы ресурсов, имени sapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="84e9b-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="84e9b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84e9b-110">EXAMPLES</span></span>

### <span data-ttu-id="84e9b-111">Пример 1. Создание экземпляра монитора SAP по строке для HANA</span><span class="sxs-lookup"><span data-stu-id="84e9b-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="84e9b-112">Эта команда создает экземпляр монитора SAP по строке для HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="84e9b-113">Пример 2. Создание экземпляра монитора SAP с ключным хранилищем для HANA</span><span class="sxs-lookup"><span data-stu-id="84e9b-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="84e9b-114">Эта команда создает экземпляр монитора SAP в хранилище ключей для HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="84e9b-115">Пример 3. Создание экземпляра монитора SAP по словарю для PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="84e9b-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="84e9b-116">Эта команда создает экземпляр монитора SAP в словаре для PrometheusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="84e9b-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="84e9b-117">Пример 4. Создание экземпляра монитора SAP по словарю для PrometheusOS</span><span class="sxs-lookup"><span data-stu-id="84e9b-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="84e9b-118">Эта команда создает экземпляр монитора SAP по словарю для PrometheusOS.</span><span class="sxs-lookup"><span data-stu-id="84e9b-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="84e9b-119">Пример 5. Создание экземпляра монитора SAP в словаре для MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="84e9b-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="84e9b-120">Эта команда создает экземпляр монитора SAP для словаря MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="84e9b-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="84e9b-121">Пример 6. Создание экземпляра монитора SAP в словаре для SapHana</span><span class="sxs-lookup"><span data-stu-id="84e9b-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="84e9b-122">Эта команда создает экземпляр монитора SAP для словаря SapHana.</span><span class="sxs-lookup"><span data-stu-id="84e9b-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="84e9b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84e9b-123">PARAMETERS</span></span>

### <span data-ttu-id="84e9b-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84e9b-124">-AsJob</span></span>
<span data-ttu-id="84e9b-125">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="84e9b-125">Run the command as a job</span></span>

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

### <span data-ttu-id="84e9b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e9b-126">-DefaultProfile</span></span>
<span data-ttu-id="84e9b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84e9b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="84e9b-128">-HanaDatabaseName</span></span>
<span data-ttu-id="84e9b-129">Имя экземпляра базы данных SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="84e9b-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="84e9b-131">Пароль базы данных экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="84e9b-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="84e9b-133">ИД ресурса хранилища ключа, который содержит учетные данные HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="84e9b-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="84e9b-135">Секретный идентификатор секретного сейфа, который содержит учетные данные HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="84e9b-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="84e9b-137">Порт SQL базы данных экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="84e9b-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="84e9b-139">Имя пользователя базы данных экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="84e9b-140">-HanaHostname</span></span>
<span data-ttu-id="84e9b-141">Имя экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="84e9b-142">-InstanceProperty</span></span>
<span data-ttu-id="84e9b-143">Свойство экземпляра HANA.</span><span class="sxs-lookup"><span data-stu-id="84e9b-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-144">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="84e9b-144">-Metadata</span></span>
<span data-ttu-id="84e9b-145">Строка JSON, содержащая метаданные экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="84e9b-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="84e9b-146">-Name</span><span class="sxs-lookup"><span data-stu-id="84e9b-146">-Name</span></span>
<span data-ttu-id="84e9b-147">Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="84e9b-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84e9b-148">-NoWait</span></span>
<span data-ttu-id="84e9b-149">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="84e9b-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84e9b-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="84e9b-150">-ProviderType</span></span>
<span data-ttu-id="84e9b-151">Тип экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="84e9b-151">The type of provider instance.</span></span>
<span data-ttu-id="84e9b-152">Поддерживаемые значения: "СапХана".</span><span class="sxs-lookup"><span data-stu-id="84e9b-152">Supported values are: "SapHana".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e9b-153">-ResourceGroupName</span></span>
<span data-ttu-id="84e9b-154">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84e9b-154">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="84e9b-155">-SapMonitorName</span></span>
<span data-ttu-id="84e9b-156">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="84e9b-156">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84e9b-157">-SubscriptionId</span></span>
<span data-ttu-id="84e9b-158">Идентификация подписки, однозначно определяемая подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84e9b-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84e9b-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="84e9b-159">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e9b-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84e9b-160">-Confirm</span></span>
<span data-ttu-id="84e9b-161">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e9b-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e9b-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e9b-162">-WhatIf</span></span>
<span data-ttu-id="84e9b-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e9b-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84e9b-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="84e9b-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84e9b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e9b-165">CommonParameters</span></span>
<span data-ttu-id="84e9b-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e9b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e9b-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84e9b-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e9b-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84e9b-168">INPUTS</span></span>

## <span data-ttu-id="84e9b-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84e9b-169">OUTPUTS</span></span>

### <span data-ttu-id="84e9b-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="84e9b-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="84e9b-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84e9b-171">NOTES</span></span>

<span data-ttu-id="84e9b-172">ALIASES</span><span class="sxs-lookup"><span data-stu-id="84e9b-172">ALIASES</span></span>

## <span data-ttu-id="84e9b-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84e9b-173">RELATED LINKS</span></span>

