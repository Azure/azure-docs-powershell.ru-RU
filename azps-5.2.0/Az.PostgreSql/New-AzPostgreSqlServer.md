---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391932"
---
# <span data-ttu-id="56fc5-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="56fc5-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="56fc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="56fc5-103">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="56fc5-103">Creates a new server.</span></span>

## <span data-ttu-id="56fc5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56fc5-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56fc5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="56fc5-106">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="56fc5-106">Creates a new server.</span></span>

## <span data-ttu-id="56fc5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="56fc5-108">Пример 1. Создание нового сервера PostgreSql</span><span class="sxs-lookup"><span data-stu-id="56fc5-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="56fc5-109">Эти cmdlets создают новый сервер PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="56fc5-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="56fc5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56fc5-110">PARAMETERS</span></span>

### <span data-ttu-id="56fc5-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="56fc5-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="56fc5-112">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="56fc5-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="56fc5-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="56fc5-113">-AdministratorUserName</span></span>
<span data-ttu-id="56fc5-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="56fc5-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="56fc5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56fc5-115">-AsJob</span></span>
<span data-ttu-id="56fc5-116">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="56fc5-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="56fc5-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="56fc5-117">-BackupRetentionDay</span></span>
<span data-ttu-id="56fc5-118">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="56fc5-118">Backup retention days for the server.</span></span>
<span data-ttu-id="56fc5-119">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="56fc5-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="56fc5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fc5-120">-DefaultProfile</span></span>
<span data-ttu-id="56fc5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56fc5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56fc5-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="56fc5-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="56fc5-123">В этой области можно включить гео избыточное резервное копирование или не использовать резервное копирование на сервере.</span><span class="sxs-lookup"><span data-stu-id="56fc5-123">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="56fc5-124">-Location</span><span class="sxs-lookup"><span data-stu-id="56fc5-124">-Location</span></span>
<span data-ttu-id="56fc5-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="56fc5-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="56fc5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="56fc5-126">-Name</span></span>
<span data-ttu-id="56fc5-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="56fc5-127">The name of the server.</span></span>

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

### <span data-ttu-id="56fc5-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="56fc5-128">-NoWait</span></span>
<span data-ttu-id="56fc5-129">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="56fc5-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="56fc5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56fc5-130">-ResourceGroupName</span></span>
<span data-ttu-id="56fc5-131">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="56fc5-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="56fc5-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="56fc5-132">-Sku</span></span>
<span data-ttu-id="56fc5-133">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="56fc5-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="56fc5-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="56fc5-134">-SslEnforcement</span></span>
<span data-ttu-id="56fc5-135">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="56fc5-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="56fc5-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="56fc5-136">-StorageAutogrow</span></span>
<span data-ttu-id="56fc5-137">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="56fc5-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="56fc5-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="56fc5-138">-StorageInMb</span></span>
<span data-ttu-id="56fc5-139">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="56fc5-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="56fc5-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56fc5-140">-SubscriptionId</span></span>
<span data-ttu-id="56fc5-141">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="56fc5-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="56fc5-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="56fc5-142">-Tag</span></span>
<span data-ttu-id="56fc5-143">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="56fc5-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="56fc5-144">-Версия</span><span class="sxs-lookup"><span data-stu-id="56fc5-144">-Version</span></span>
<span data-ttu-id="56fc5-145">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="56fc5-145">Server version.</span></span>

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

### <span data-ttu-id="56fc5-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56fc5-146">-Confirm</span></span>
<span data-ttu-id="56fc5-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56fc5-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56fc5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56fc5-148">-WhatIf</span></span>
<span data-ttu-id="56fc5-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56fc5-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56fc5-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56fc5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56fc5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fc5-151">CommonParameters</span></span>
<span data-ttu-id="56fc5-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fc5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fc5-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56fc5-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fc5-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56fc5-154">INPUTS</span></span>

## <span data-ttu-id="56fc5-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56fc5-155">OUTPUTS</span></span>

### <span data-ttu-id="56fc5-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="56fc5-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="56fc5-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56fc5-157">NOTES</span></span>

<span data-ttu-id="56fc5-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="56fc5-158">ALIASES</span></span>

## <span data-ttu-id="56fc5-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56fc5-159">RELATED LINKS</span></span>

