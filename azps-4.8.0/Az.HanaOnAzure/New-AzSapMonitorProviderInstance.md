---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079055"
---
# <span data-ttu-id="57d3a-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="57d3a-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="57d3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="57d3a-103">Создает экземпляр поставщика для указанной подписки, группы ресурсов, имени SapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="57d3a-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="57d3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57d3a-104">SYNTAX</span></span>

### <span data-ttu-id="57d3a-105">ByString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57d3a-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="57d3a-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="57d3a-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57d3a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57d3a-107">DESCRIPTION</span></span>
<span data-ttu-id="57d3a-108">Создает экземпляр поставщика для указанной подписки, группы ресурсов, имени SapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="57d3a-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="57d3a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57d3a-109">EXAMPLES</span></span>

### <span data-ttu-id="57d3a-110">Пример 1: создание экземпляра монитора SAP с помощью строки для HANA</span><span class="sxs-lookup"><span data-stu-id="57d3a-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="57d3a-111">Эта команда создает экземпляр мониторинга SAP с помощью строки для HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="57d3a-112">Пример 2: создание экземпляра монитора SAP по ключу хранилища для HANA</span><span class="sxs-lookup"><span data-stu-id="57d3a-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="57d3a-113">Эта команда создает экземпляр монитора SAP с помощью хранилища ключей для HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="57d3a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57d3a-114">PARAMETERS</span></span>

### <span data-ttu-id="57d3a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57d3a-115">-AsJob</span></span>
<span data-ttu-id="57d3a-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="57d3a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="57d3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d3a-117">-DefaultProfile</span></span>
<span data-ttu-id="57d3a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57d3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57d3a-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="57d3a-119">-HanaDatabaseName</span></span>
<span data-ttu-id="57d3a-120">Имя базы данных экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d3a-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="57d3a-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="57d3a-122">Пароль базы данных экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="57d3a-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="57d3a-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="57d3a-124">Идентификатор ресурса для хранилища ключей, содержащего учетные данные HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="57d3a-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="57d3a-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="57d3a-126">Секретный идентификатор в секретный ключ хранилища ключей, содержащий учетные данные HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="57d3a-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="57d3a-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="57d3a-128">Порт SQL базы данных экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d3a-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="57d3a-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="57d3a-130">Имя пользователя базы данных экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d3a-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="57d3a-131">-HanaHostname</span></span>
<span data-ttu-id="57d3a-132">Имя хоста экземпляра SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="57d3a-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="57d3a-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="57d3a-133">-Metadata</span></span>
<span data-ttu-id="57d3a-134">Строка JSON, содержащая метаданные экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="57d3a-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="57d3a-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57d3a-135">-Name</span></span>
<span data-ttu-id="57d3a-136">Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="57d3a-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="57d3a-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="57d3a-137">-NoWait</span></span>
<span data-ttu-id="57d3a-138">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="57d3a-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57d3a-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="57d3a-139">-ProviderType</span></span>
<span data-ttu-id="57d3a-140">Тип экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="57d3a-140">The type of provider instance.</span></span>
<span data-ttu-id="57d3a-141">Поддерживаются следующие значения: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="57d3a-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="57d3a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d3a-142">-ResourceGroupName</span></span>
<span data-ttu-id="57d3a-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57d3a-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="57d3a-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="57d3a-144">-SapMonitorName</span></span>
<span data-ttu-id="57d3a-145">Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="57d3a-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="57d3a-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57d3a-146">-SubscriptionId</span></span>
<span data-ttu-id="57d3a-147">Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57d3a-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57d3a-148">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="57d3a-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57d3a-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57d3a-149">-Confirm</span></span>
<span data-ttu-id="57d3a-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57d3a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57d3a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d3a-151">-WhatIf</span></span>
<span data-ttu-id="57d3a-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57d3a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d3a-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57d3a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57d3a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d3a-154">CommonParameters</span></span>
<span data-ttu-id="57d3a-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57d3a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d3a-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57d3a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d3a-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57d3a-157">INPUTS</span></span>

## <span data-ttu-id="57d3a-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57d3a-158">OUTPUTS</span></span>

### <span data-ttu-id="57d3a-159">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="57d3a-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="57d3a-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="57d3a-160">NOTES</span></span>

<span data-ttu-id="57d3a-161">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="57d3a-161">ALIASES</span></span>

## <span data-ttu-id="57d3a-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57d3a-162">RELATED LINKS</span></span>

