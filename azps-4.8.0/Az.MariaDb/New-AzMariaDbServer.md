---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078190"
---
# <span data-ttu-id="74b80-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="74b80-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="74b80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74b80-102">SYNOPSIS</span></span>
<span data-ttu-id="74b80-103">Создание нового MariaDB.</span><span class="sxs-lookup"><span data-stu-id="74b80-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="74b80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74b80-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74b80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74b80-105">DESCRIPTION</span></span>
<span data-ttu-id="74b80-106">Создание нового MariaDB.</span><span class="sxs-lookup"><span data-stu-id="74b80-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="74b80-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74b80-107">EXAMPLES</span></span>

### <span data-ttu-id="74b80-108">Пример 1: создание нового MariaDB</span><span class="sxs-lookup"><span data-stu-id="74b80-108">Example 1: Create a new MariaDB</span></span>
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

<span data-ttu-id="74b80-109">Эта команда создает новый MariaDB.</span><span class="sxs-lookup"><span data-stu-id="74b80-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="74b80-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74b80-110">PARAMETERS</span></span>

### <span data-ttu-id="74b80-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="74b80-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="74b80-112">Пароль администратора должен быть SecureString.</span><span class="sxs-lookup"><span data-stu-id="74b80-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="74b80-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="74b80-113">-AdministratorUsername</span></span>
<span data-ttu-id="74b80-114">Имя пользователя администратора.</span><span class="sxs-lookup"><span data-stu-id="74b80-114">Username of administrator.</span></span>

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

### <span data-ttu-id="74b80-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74b80-115">-AsJob</span></span>
<span data-ttu-id="74b80-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="74b80-116">Run the command as a job</span></span>

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

### <span data-ttu-id="74b80-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="74b80-117">-BackupRetentionDay</span></span>
<span data-ttu-id="74b80-118">Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="74b80-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="74b80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b80-119">-DefaultProfile</span></span>
<span data-ttu-id="74b80-120">Region DefaultParameters учетные данные, учетную запись, клиента и подписку, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74b80-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b80-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="74b80-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="74b80-122">Включите геоизбыточное или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="74b80-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="74b80-123">-Location</span><span class="sxs-lookup"><span data-stu-id="74b80-123">-Location</span></span>
<span data-ttu-id="74b80-124">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="74b80-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="74b80-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74b80-125">-Name</span></span>
<span data-ttu-id="74b80-126">Имя сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="74b80-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="74b80-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="74b80-127">-NoWait</span></span>
<span data-ttu-id="74b80-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="74b80-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74b80-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b80-129">-ResourceGroupName</span></span>
<span data-ttu-id="74b80-130">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="74b80-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="74b80-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="74b80-131">-Sku</span></span>
<span data-ttu-id="74b80-132">Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="74b80-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="74b80-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="74b80-133">-SslEnforcement</span></span>
<span data-ttu-id="74b80-134">Включите шифрование SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="74b80-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="74b80-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="74b80-135">-StorageAutogrow</span></span>
<span data-ttu-id="74b80-136">Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="74b80-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="74b80-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="74b80-137">-StorageInMb</span></span>
<span data-ttu-id="74b80-138">Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="74b80-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="74b80-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74b80-139">-SubscriptionId</span></span>
<span data-ttu-id="74b80-140">Идентификатор подписки — это часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="74b80-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="74b80-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="74b80-141">-Tag</span></span>
<span data-ttu-id="74b80-142">Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="74b80-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="74b80-143">-Version</span><span class="sxs-lookup"><span data-stu-id="74b80-143">-Version</span></span>
<span data-ttu-id="74b80-144">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="74b80-144">Server version.</span></span>

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

### <span data-ttu-id="74b80-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74b80-145">-Confirm</span></span>
<span data-ttu-id="74b80-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74b80-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b80-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b80-147">-WhatIf</span></span>
<span data-ttu-id="74b80-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74b80-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b80-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74b80-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b80-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b80-150">CommonParameters</span></span>
<span data-ttu-id="74b80-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74b80-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b80-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74b80-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b80-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74b80-153">INPUTS</span></span>

## <span data-ttu-id="74b80-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74b80-154">OUTPUTS</span></span>

### <span data-ttu-id="74b80-155">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="74b80-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="74b80-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="74b80-156">NOTES</span></span>

<span data-ttu-id="74b80-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="74b80-157">ALIASES</span></span>

## <span data-ttu-id="74b80-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74b80-158">RELATED LINKS</span></span>

