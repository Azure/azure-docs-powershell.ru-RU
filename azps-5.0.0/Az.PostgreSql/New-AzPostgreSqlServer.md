---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246366"
---
# <span data-ttu-id="88d23-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="88d23-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="88d23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88d23-102">SYNOPSIS</span></span>
<span data-ttu-id="88d23-103">Создание нового сервера.</span><span class="sxs-lookup"><span data-stu-id="88d23-103">Creates a new server.</span></span>

## <span data-ttu-id="88d23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88d23-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88d23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88d23-105">DESCRIPTION</span></span>
<span data-ttu-id="88d23-106">Создание нового сервера.</span><span class="sxs-lookup"><span data-stu-id="88d23-106">Creates a new server.</span></span>

## <span data-ttu-id="88d23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88d23-107">EXAMPLES</span></span>

### <span data-ttu-id="88d23-108">Пример 1: создание нового сервера PostgreSql</span><span class="sxs-lookup"><span data-stu-id="88d23-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="88d23-109">Эти командлеты создают новый сервер PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="88d23-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="88d23-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88d23-110">PARAMETERS</span></span>

### <span data-ttu-id="88d23-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="88d23-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="88d23-112">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="88d23-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="88d23-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="88d23-113">-AdministratorUserName</span></span>
<span data-ttu-id="88d23-114">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="88d23-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="88d23-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88d23-115">-AsJob</span></span>
<span data-ttu-id="88d23-116">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="88d23-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="88d23-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="88d23-117">-BackupRetentionDay</span></span>
<span data-ttu-id="88d23-118">Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="88d23-118">Backup retention days for the server.</span></span>
<span data-ttu-id="88d23-119">Число дней в интервале от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="88d23-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="88d23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d23-120">-DefaultProfile</span></span>
<span data-ttu-id="88d23-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88d23-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88d23-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="88d23-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="88d23-123">Включите геоизбыточное или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="88d23-123">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="88d23-124">-Location</span><span class="sxs-lookup"><span data-stu-id="88d23-124">-Location</span></span>
<span data-ttu-id="88d23-125">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="88d23-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="88d23-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88d23-126">-Name</span></span>
<span data-ttu-id="88d23-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="88d23-127">The name of the server.</span></span>

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

### <span data-ttu-id="88d23-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="88d23-128">-NoWait</span></span>
<span data-ttu-id="88d23-129">Выполните команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="88d23-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="88d23-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88d23-130">-ResourceGroupName</span></span>
<span data-ttu-id="88d23-131">Имя группы ресурсов, содержащей ресурс, это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="88d23-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="88d23-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="88d23-132">-Sku</span></span>
<span data-ttu-id="88d23-133">Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="88d23-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="88d23-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="88d23-134">-SslEnforcement</span></span>
<span data-ttu-id="88d23-135">Включите шифрование SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="88d23-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="88d23-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="88d23-136">-StorageAutogrow</span></span>
<span data-ttu-id="88d23-137">Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="88d23-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="88d23-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="88d23-138">-StorageInMb</span></span>
<span data-ttu-id="88d23-139">Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="88d23-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="88d23-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88d23-140">-SubscriptionId</span></span>
<span data-ttu-id="88d23-141">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="88d23-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="88d23-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="88d23-142">-Tag</span></span>
<span data-ttu-id="88d23-143">Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="88d23-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="88d23-144">-Version</span><span class="sxs-lookup"><span data-stu-id="88d23-144">-Version</span></span>
<span data-ttu-id="88d23-145">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="88d23-145">Server version.</span></span>

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

### <span data-ttu-id="88d23-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88d23-146">-Confirm</span></span>
<span data-ttu-id="88d23-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88d23-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d23-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d23-148">-WhatIf</span></span>
<span data-ttu-id="88d23-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88d23-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d23-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88d23-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d23-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d23-151">CommonParameters</span></span>
<span data-ttu-id="88d23-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88d23-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d23-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88d23-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d23-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88d23-154">INPUTS</span></span>

## <span data-ttu-id="88d23-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88d23-155">OUTPUTS</span></span>

### <span data-ttu-id="88d23-156">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="88d23-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="88d23-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="88d23-157">NOTES</span></span>

<span data-ttu-id="88d23-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="88d23-158">ALIASES</span></span>

## <span data-ttu-id="88d23-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88d23-159">RELATED LINKS</span></span>

