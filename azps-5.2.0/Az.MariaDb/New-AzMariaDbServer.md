---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405188"
---
# <span data-ttu-id="bea12-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="bea12-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="bea12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea12-102">SYNOPSIS</span></span>
<span data-ttu-id="bea12-103">Создается новая система MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bea12-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="bea12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bea12-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bea12-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bea12-105">DESCRIPTION</span></span>
<span data-ttu-id="bea12-106">Создается новая система MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bea12-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="bea12-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bea12-107">EXAMPLES</span></span>

### <span data-ttu-id="bea12-108">Пример 1. Создание новой</span><span class="sxs-lookup"><span data-stu-id="bea12-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="bea12-109">Эта команда создает новую MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bea12-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="bea12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bea12-110">PARAMETERS</span></span>

### <span data-ttu-id="bea12-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="bea12-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="bea12-112">Пароль администратора должен быть SecureString.</span><span class="sxs-lookup"><span data-stu-id="bea12-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="bea12-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="bea12-113">-AdministratorUsername</span></span>
<span data-ttu-id="bea12-114">Имя пользователя администратора.</span><span class="sxs-lookup"><span data-stu-id="bea12-114">Username of administrator.</span></span>

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

### <span data-ttu-id="bea12-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bea12-115">-AsJob</span></span>
<span data-ttu-id="bea12-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="bea12-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bea12-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="bea12-117">-BackupRetentionDay</span></span>
<span data-ttu-id="bea12-118">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="bea12-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="bea12-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea12-119">-DefaultProfile</span></span>
<span data-ttu-id="bea12-120">Region DefaultParameters The credentials, account, tenant и subscription, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bea12-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea12-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="bea12-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="bea12-122">В этой области можно включить гео избыточное резервное копирование или не использовать резервное копирование на сервере.</span><span class="sxs-lookup"><span data-stu-id="bea12-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea12-123">-Location</span><span class="sxs-lookup"><span data-stu-id="bea12-123">-Location</span></span>
<span data-ttu-id="bea12-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="bea12-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="bea12-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bea12-125">-Name</span></span>
<span data-ttu-id="bea12-126">Имя сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bea12-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="bea12-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bea12-127">-NoWait</span></span>
<span data-ttu-id="bea12-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="bea12-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bea12-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea12-129">-ResourceGroupName</span></span>
<span data-ttu-id="bea12-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="bea12-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="bea12-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="bea12-131">-Sku</span></span>
<span data-ttu-id="bea12-132">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bea12-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="bea12-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="bea12-133">-SslEnforcement</span></span>
<span data-ttu-id="bea12-134">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="bea12-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea12-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="bea12-135">-StorageAutogrow</span></span>
<span data-ttu-id="bea12-136">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="bea12-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea12-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="bea12-137">-StorageInMb</span></span>
<span data-ttu-id="bea12-138">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="bea12-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="bea12-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bea12-139">-SubscriptionId</span></span>
<span data-ttu-id="bea12-140">ИД подписки является частью URI для каждого звонка в службу</span><span class="sxs-lookup"><span data-stu-id="bea12-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="bea12-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="bea12-141">-Tag</span></span>
<span data-ttu-id="bea12-142">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="bea12-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="bea12-143">-Version</span><span class="sxs-lookup"><span data-stu-id="bea12-143">-Version</span></span>
<span data-ttu-id="bea12-144">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="bea12-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea12-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bea12-145">-Confirm</span></span>
<span data-ttu-id="bea12-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea12-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea12-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea12-147">-WhatIf</span></span>
<span data-ttu-id="bea12-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea12-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea12-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bea12-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea12-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea12-150">CommonParameters</span></span>
<span data-ttu-id="bea12-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea12-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea12-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bea12-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea12-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bea12-153">INPUTS</span></span>

## <span data-ttu-id="bea12-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bea12-154">OUTPUTS</span></span>

### <span data-ttu-id="bea12-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="bea12-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="bea12-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bea12-156">NOTES</span></span>

<span data-ttu-id="bea12-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bea12-157">ALIASES</span></span>

## <span data-ttu-id="bea12-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bea12-158">RELATED LINKS</span></span>

