---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 683ca81587ff7c71f1406eb7a4accef37aac794d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412199"
---
# <span data-ttu-id="f03f6-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="f03f6-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="f03f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f03f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f03f6-103">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="f03f6-103">Creates a new server.</span></span>

## <span data-ttu-id="f03f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f03f6-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f03f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f03f6-105">DESCRIPTION</span></span>
<span data-ttu-id="f03f6-106">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="f03f6-106">Creates a new server.</span></span>

## <span data-ttu-id="f03f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f03f6-107">EXAMPLES</span></span>

### <span data-ttu-id="f03f6-108">Пример 1. Создание нового сервера MySql</span><span class="sxs-lookup"><span data-stu-id="f03f6-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f03f6-109">Эти cmdlets создают новый сервер MySql.</span><span class="sxs-lookup"><span data-stu-id="f03f6-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="f03f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f03f6-110">PARAMETERS</span></span>

### <span data-ttu-id="f03f6-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f03f6-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f03f6-112">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="f03f6-112">The password of the administrator.</span></span>
<span data-ttu-id="f03f6-113">Не менее 8 знаков и не более 128 знаков.</span><span class="sxs-lookup"><span data-stu-id="f03f6-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="f03f6-114">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="f03f6-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="f03f6-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="f03f6-115">-AdministratorUserName</span></span>
<span data-ttu-id="f03f6-116">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="f03f6-116">Administrator username for the server.</span></span>
<span data-ttu-id="f03f6-117">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="f03f6-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="f03f6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f03f6-118">-AsJob</span></span>
<span data-ttu-id="f03f6-119">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="f03f6-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="f03f6-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="f03f6-120">-BackupRetentionDay</span></span>
<span data-ttu-id="f03f6-121">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="f03f6-121">Backup retention days for the server.</span></span>
<span data-ttu-id="f03f6-122">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="f03f6-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="f03f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03f6-123">-DefaultProfile</span></span>
<span data-ttu-id="f03f6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f03f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03f6-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="f03f6-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="f03f6-126">В этой области можно включить гео избыточное резервное копирование или не использовать резервное копирование на сервере.</span><span class="sxs-lookup"><span data-stu-id="f03f6-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="f03f6-127">-Location</span><span class="sxs-lookup"><span data-stu-id="f03f6-127">-Location</span></span>
<span data-ttu-id="f03f6-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f03f6-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f03f6-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f03f6-129">-Name</span></span>
<span data-ttu-id="f03f6-130">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f03f6-130">The name of the server.</span></span>

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

### <span data-ttu-id="f03f6-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f03f6-131">-NoWait</span></span>
<span data-ttu-id="f03f6-132">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f03f6-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="f03f6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03f6-133">-ResourceGroupName</span></span>
<span data-ttu-id="f03f6-134">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="f03f6-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f03f6-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="f03f6-135">-Sku</span></span>
<span data-ttu-id="f03f6-136">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f03f6-136">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="f03f6-137">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="f03f6-137">-SslEnforcement</span></span>
<span data-ttu-id="f03f6-138">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="f03f6-138">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="f03f6-139">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="f03f6-139">-StorageAutogrow</span></span>
<span data-ttu-id="f03f6-140">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="f03f6-140">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="f03f6-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="f03f6-141">-StorageInMb</span></span>
<span data-ttu-id="f03f6-142">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="f03f6-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="f03f6-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f03f6-143">-SubscriptionId</span></span>
<span data-ttu-id="f03f6-144">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="f03f6-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f03f6-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="f03f6-145">-Tag</span></span>
<span data-ttu-id="f03f6-146">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="f03f6-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f03f6-147">-Version</span><span class="sxs-lookup"><span data-stu-id="f03f6-147">-Version</span></span>
<span data-ttu-id="f03f6-148">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="f03f6-148">Server version.</span></span>

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

### <span data-ttu-id="f03f6-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f03f6-149">-Confirm</span></span>
<span data-ttu-id="f03f6-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f03f6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03f6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f03f6-151">-WhatIf</span></span>
<span data-ttu-id="f03f6-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f03f6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f03f6-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f03f6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03f6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03f6-154">CommonParameters</span></span>
<span data-ttu-id="f03f6-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03f6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03f6-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f03f6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03f6-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f03f6-157">INPUTS</span></span>

## <span data-ttu-id="f03f6-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f03f6-158">OUTPUTS</span></span>

### <span data-ttu-id="f03f6-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="f03f6-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f03f6-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f03f6-160">NOTES</span></span>

<span data-ttu-id="f03f6-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f03f6-161">ALIASES</span></span>

## <span data-ttu-id="f03f6-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f03f6-162">RELATED LINKS</span></span>

