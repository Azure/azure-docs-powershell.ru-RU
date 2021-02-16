---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 37e8896389931f6909d783cbb07a694ed6186fc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241189"
---
# <span data-ttu-id="46743-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="46743-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="46743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46743-102">SYNOPSIS</span></span>
<span data-ttu-id="46743-103">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="46743-103">Creates a new server.</span></span>

## <span data-ttu-id="46743-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46743-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46743-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46743-105">DESCRIPTION</span></span>
<span data-ttu-id="46743-106">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="46743-106">Creates a new server.</span></span>

## <span data-ttu-id="46743-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46743-107">EXAMPLES</span></span>

### <span data-ttu-id="46743-108">Пример 1. Создание нового сервера MySql</span><span class="sxs-lookup"><span data-stu-id="46743-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="46743-109">Эти cmdlets создают новый сервер MySql.</span><span class="sxs-lookup"><span data-stu-id="46743-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="46743-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46743-110">PARAMETERS</span></span>

### <span data-ttu-id="46743-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="46743-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="46743-112">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="46743-112">The password of the administrator.</span></span>
<span data-ttu-id="46743-113">Не менее 8 знаков и не более 128 знаков.</span><span class="sxs-lookup"><span data-stu-id="46743-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="46743-114">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="46743-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="46743-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="46743-115">-AdministratorUserName</span></span>
<span data-ttu-id="46743-116">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="46743-116">Administrator username for the server.</span></span>
<span data-ttu-id="46743-117">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="46743-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="46743-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46743-118">-AsJob</span></span>
<span data-ttu-id="46743-119">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="46743-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="46743-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="46743-120">-BackupRetentionDay</span></span>
<span data-ttu-id="46743-121">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="46743-121">Backup retention days for the server.</span></span>
<span data-ttu-id="46743-122">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="46743-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="46743-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46743-123">-DefaultProfile</span></span>
<span data-ttu-id="46743-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46743-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46743-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="46743-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="46743-126">В этой области можно включить гео избыточное резервное копирование или не использовать резервное копирование на сервере.</span><span class="sxs-lookup"><span data-stu-id="46743-126">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46743-127">-Location</span><span class="sxs-lookup"><span data-stu-id="46743-127">-Location</span></span>
<span data-ttu-id="46743-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="46743-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="46743-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="46743-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="46743-130">Установите минимальную версию TLS для подключений к серверу, если включен SSL.</span><span class="sxs-lookup"><span data-stu-id="46743-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="46743-131">Значение по умолчанию — TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="46743-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46743-132">-Name</span><span class="sxs-lookup"><span data-stu-id="46743-132">-Name</span></span>
<span data-ttu-id="46743-133">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="46743-133">The name of the server.</span></span>

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

### <span data-ttu-id="46743-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="46743-134">-NoWait</span></span>
<span data-ttu-id="46743-135">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="46743-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="46743-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46743-136">-ResourceGroupName</span></span>
<span data-ttu-id="46743-137">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="46743-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="46743-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="46743-138">-Sku</span></span>
<span data-ttu-id="46743-139">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="46743-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="46743-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="46743-140">-SslEnforcement</span></span>
<span data-ttu-id="46743-141">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="46743-141">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46743-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="46743-142">-StorageAutogrow</span></span>
<span data-ttu-id="46743-143">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="46743-143">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46743-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="46743-144">-StorageInMb</span></span>
<span data-ttu-id="46743-145">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="46743-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="46743-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46743-146">-SubscriptionId</span></span>
<span data-ttu-id="46743-147">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="46743-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="46743-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="46743-148">-Tag</span></span>
<span data-ttu-id="46743-149">Метаданные приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="46743-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="46743-150">-Version</span><span class="sxs-lookup"><span data-stu-id="46743-150">-Version</span></span>
<span data-ttu-id="46743-151">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="46743-151">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46743-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46743-152">-Confirm</span></span>
<span data-ttu-id="46743-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="46743-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46743-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46743-154">-WhatIf</span></span>
<span data-ttu-id="46743-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46743-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46743-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46743-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46743-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46743-157">CommonParameters</span></span>
<span data-ttu-id="46743-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46743-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46743-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46743-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46743-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46743-160">INPUTS</span></span>

## <span data-ttu-id="46743-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46743-161">OUTPUTS</span></span>

### <span data-ttu-id="46743-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="46743-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="46743-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46743-163">NOTES</span></span>

<span data-ttu-id="46743-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="46743-164">ALIASES</span></span>

## <span data-ttu-id="46743-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46743-165">RELATED LINKS</span></span>

