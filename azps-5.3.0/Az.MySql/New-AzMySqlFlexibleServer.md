---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518190"
---
# <span data-ttu-id="be883-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="be883-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="be883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be883-102">SYNOPSIS</span></span>
<span data-ttu-id="be883-103">Создание нового гибкого сервера MySQL</span><span class="sxs-lookup"><span data-stu-id="be883-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="be883-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be883-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be883-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be883-105">DESCRIPTION</span></span>
<span data-ttu-id="be883-106">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="be883-106">Creates a new server.</span></span>

## <span data-ttu-id="be883-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be883-107">EXAMPLES</span></span>

### <span data-ttu-id="be883-108">Пример 1. Создание нового гибкого сервера MySql</span><span class="sxs-lookup"><span data-stu-id="be883-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="be883-109">Пример 2. Создание нового гибкого сервера MySql с настройкой по умолчанию</span><span class="sxs-lookup"><span data-stu-id="be883-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="be883-110">Создайте сервер MySql со значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be883-110">Create MySql server with default values.</span></span>
<span data-ttu-id="be883-111">По умолчанию расположение имеет значение West US 2, SKU — Standard_B1ms, SKU — срыв, а размер хранилища — 10GiB.</span><span class="sxs-lookup"><span data-stu-id="be883-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="be883-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be883-112">PARAMETERS</span></span>

### <span data-ttu-id="be883-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="be883-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="be883-114">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="be883-114">The password of the administrator.</span></span>
<span data-ttu-id="be883-115">Не менее 8 знаков и не более 128 знаков.</span><span class="sxs-lookup"><span data-stu-id="be883-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="be883-116">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="be883-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="be883-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="be883-117">-AdministratorUserName</span></span>
<span data-ttu-id="be883-118">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="be883-118">Administrator username for the server.</span></span>
<span data-ttu-id="be883-119">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="be883-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="be883-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be883-120">-AsJob</span></span>
<span data-ttu-id="be883-121">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="be883-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="be883-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="be883-122">-BackupRetentionDay</span></span>
<span data-ttu-id="be883-123">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="be883-123">Backup retention days for the server.</span></span>
<span data-ttu-id="be883-124">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="be883-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="be883-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be883-125">-DefaultProfile</span></span>
<span data-ttu-id="be883-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be883-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be883-127">-Location</span><span class="sxs-lookup"><span data-stu-id="be883-127">-Location</span></span>
<span data-ttu-id="be883-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="be883-128">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be883-129">-Name</span><span class="sxs-lookup"><span data-stu-id="be883-129">-Name</span></span>
<span data-ttu-id="be883-130">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="be883-130">The name of the server.</span></span>

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

### <span data-ttu-id="be883-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be883-131">-NoWait</span></span>
<span data-ttu-id="be883-132">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="be883-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="be883-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be883-133">-ResourceGroupName</span></span>
<span data-ttu-id="be883-134">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="be883-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="be883-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="be883-135">-Sku</span></span>
<span data-ttu-id="be883-136">Как правило, это название SKU уровня +family + cores, например Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="be883-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be883-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="be883-137">-SkuTier</span></span>
<span data-ttu-id="be883-138">Вычислять уровень сервера.</span><span class="sxs-lookup"><span data-stu-id="be883-138">Compute tier of the server.</span></span>
<span data-ttu-id="be883-139">Принятые значения: Скайп, ОбщееТип, Оптимизированная память.</span><span class="sxs-lookup"><span data-stu-id="be883-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="be883-140">По умолчанию: срыв.</span><span class="sxs-lookup"><span data-stu-id="be883-140">Default: Burstable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be883-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="be883-141">-StorageInMb</span></span>
<span data-ttu-id="be883-142">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="be883-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="be883-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be883-143">-SubscriptionId</span></span>
<span data-ttu-id="be883-144">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="be883-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="be883-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="be883-145">-Tag</span></span>
<span data-ttu-id="be883-146">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="be883-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="be883-147">-Version</span><span class="sxs-lookup"><span data-stu-id="be883-147">-Version</span></span>
<span data-ttu-id="be883-148">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="be883-148">Server version.</span></span>

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

### <span data-ttu-id="be883-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be883-149">-Confirm</span></span>
<span data-ttu-id="be883-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="be883-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be883-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be883-151">-WhatIf</span></span>
<span data-ttu-id="be883-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be883-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be883-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="be883-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be883-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be883-154">CommonParameters</span></span>
<span data-ttu-id="be883-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be883-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be883-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be883-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be883-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be883-157">INPUTS</span></span>

## <span data-ttu-id="be883-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be883-158">OUTPUTS</span></span>

### <span data-ttu-id="be883-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="be883-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="be883-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be883-160">NOTES</span></span>

<span data-ttu-id="be883-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="be883-161">ALIASES</span></span>

## <span data-ttu-id="be883-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be883-162">RELATED LINKS</span></span>

