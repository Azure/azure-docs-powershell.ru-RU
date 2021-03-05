---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: 71aa5886035164dee5b011be8a90b18e33e055e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987678"
---
# <span data-ttu-id="68924-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="68924-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="68924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68924-102">SYNOPSIS</span></span>
<span data-ttu-id="68924-103">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="68924-103">Creates a new server.</span></span>

## <span data-ttu-id="68924-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68924-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68924-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68924-105">DESCRIPTION</span></span>
<span data-ttu-id="68924-106">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="68924-106">Creates a new server.</span></span>

## <span data-ttu-id="68924-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68924-107">EXAMPLES</span></span>

### <span data-ttu-id="68924-108">Пример 1. Создание нового сервера PostgreSql</span><span class="sxs-lookup"><span data-stu-id="68924-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="68924-109">Эти cmdlets создают новый сервер PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="68924-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="68924-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68924-110">PARAMETERS</span></span>

### <span data-ttu-id="68924-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="68924-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="68924-112">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="68924-112">The password of the administrator.</span></span>
<span data-ttu-id="68924-113">Не менее 8 знаков и не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="68924-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="68924-114">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="68924-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="68924-115">-AdministratorUserName</span></span>
<span data-ttu-id="68924-116">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="68924-116">Administrator username for the server.</span></span>
<span data-ttu-id="68924-117">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="68924-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="68924-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68924-118">-AsJob</span></span>
<span data-ttu-id="68924-119">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="68924-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="68924-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="68924-120">-BackupRetentionDay</span></span>
<span data-ttu-id="68924-121">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="68924-121">Backup retention days for the server.</span></span>
<span data-ttu-id="68924-122">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="68924-122">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68924-123">-DefaultProfile</span></span>
<span data-ttu-id="68924-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68924-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68924-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="68924-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="68924-126">В этой области можно включить гео избыточное резервное копирование или не использовать резервное копирование на сервере.</span><span class="sxs-lookup"><span data-stu-id="68924-126">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-127">-Location</span><span class="sxs-lookup"><span data-stu-id="68924-127">-Location</span></span>
<span data-ttu-id="68924-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="68924-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="68924-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="68924-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="68924-130">Установите минимальную версию TLS для подключений к серверу, если включен SSL.</span><span class="sxs-lookup"><span data-stu-id="68924-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="68924-131">Значение по умолчанию — TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="68924-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-132">-Name</span><span class="sxs-lookup"><span data-stu-id="68924-132">-Name</span></span>
<span data-ttu-id="68924-133">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="68924-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68924-134">-NoWait</span></span>
<span data-ttu-id="68924-135">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="68924-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="68924-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68924-136">-ResourceGroupName</span></span>
<span data-ttu-id="68924-137">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="68924-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="68924-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="68924-138">-Sku</span></span>
<span data-ttu-id="68924-139">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="68924-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="68924-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="68924-140">-SslEnforcement</span></span>
<span data-ttu-id="68924-141">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="68924-141">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="68924-142">-StorageAutogrow</span></span>
<span data-ttu-id="68924-143">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="68924-143">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="68924-144">-StorageInMb</span></span>
<span data-ttu-id="68924-145">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="68924-145">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68924-146">-SubscriptionId</span></span>
<span data-ttu-id="68924-147">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="68924-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="68924-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="68924-148">-Tag</span></span>
<span data-ttu-id="68924-149">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="68924-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="68924-150">-Version</span><span class="sxs-lookup"><span data-stu-id="68924-150">-Version</span></span>
<span data-ttu-id="68924-151">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="68924-151">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68924-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68924-152">-Confirm</span></span>
<span data-ttu-id="68924-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="68924-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68924-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68924-154">-WhatIf</span></span>
<span data-ttu-id="68924-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68924-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68924-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="68924-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68924-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68924-157">CommonParameters</span></span>
<span data-ttu-id="68924-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68924-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68924-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68924-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68924-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68924-160">INPUTS</span></span>

## <span data-ttu-id="68924-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68924-161">OUTPUTS</span></span>

### <span data-ttu-id="68924-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="68924-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="68924-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68924-163">NOTES</span></span>

<span data-ttu-id="68924-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="68924-164">ALIASES</span></span>

## <span data-ttu-id="68924-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68924-165">RELATED LINKS</span></span>

