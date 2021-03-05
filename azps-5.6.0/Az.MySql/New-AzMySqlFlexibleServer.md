---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 4d4581d78b2e1f90ce334fda77107058f2294f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995459"
---
# <span data-ttu-id="808a3-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="808a3-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="808a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="808a3-102">SYNOPSIS</span></span>
<span data-ttu-id="808a3-103">Создает новый гибкий сервер MySQL.</span><span class="sxs-lookup"><span data-stu-id="808a3-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="808a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="808a3-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="808a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="808a3-105">DESCRIPTION</span></span>
<span data-ttu-id="808a3-106">Создает новый гибкий сервер MySQL.</span><span class="sxs-lookup"><span data-stu-id="808a3-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="808a3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="808a3-107">EXAMPLES</span></span>

### <span data-ttu-id="808a3-108">Пример 1. Создание нового гибкого сервера MySql с аргументами</span><span class="sxs-lookup"><span data-stu-id="808a3-108">Example 1: Create a new MySql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### <span data-ttu-id="808a3-109">Пример 2. Создание нового гибкого сервера MySql с настройкой по умолчанию</span><span class="sxs-lookup"><span data-stu-id="808a3-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="808a3-110">Этот cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span><span class="sxs-lookup"><span data-stu-id="808a3-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="808a3-111">По умолчанию расположение имеет значение West US 2, SKU — Standard_B1ms, SKU — срыв, а размер хранилища — 10GiB.</span><span class="sxs-lookup"><span data-stu-id="808a3-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="808a3-112">Если вы хотите найти автоматически созданный пароль для сервера, ConvertFrom-SecureString преобразуйте свойство SecuredPassword в обычный текст.</span><span class="sxs-lookup"><span data-stu-id="808a3-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="808a3-113">(Например, $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="808a3-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="808a3-114">Пример 3. Создание нового гибкого сервера MySql с виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="808a3-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="808a3-115">Этот cmdlet создает гибкий сервер MySql с ИД vnet или именем vnet, предоставленным пользователем.</span><span class="sxs-lookup"><span data-stu-id="808a3-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="808a3-116">Если виртуальная сеть не существует, ее создает cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808a3-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="808a3-117">Пример 4. Создание нового гибкого сервера MySql с именем виртуальной сети и подсети</span><span class="sxs-lookup"><span data-stu-id="808a3-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="808a3-118">Этот cmdlet создает гибкий сервер MySql с именем vnet, именем подсети, префиксом vnet и префиксом подсети.</span><span class="sxs-lookup"><span data-stu-id="808a3-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="808a3-119">Если виртуальная сеть и подсеть не существуют, будет создаться cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808a3-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="808a3-120">Пример 7. Создание нового гибкого сервера MySql с общедоступным доступом ко всем IP-данным</span><span class="sxs-lookup"><span data-stu-id="808a3-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="808a3-121">Этот cmdlet создает гибкий сервер MySql, открытый для всех IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="808a3-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="808a3-122">Пример 8. Создание нового гибкого сервера MySql с брандмауэром</span><span class="sxs-lookup"><span data-stu-id="808a3-122">Example 8: Create a new MySql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="808a3-123">Этот cmdlet создает гибкий сервер MySql, открытый для указанных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="808a3-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="808a3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="808a3-124">PARAMETERS</span></span>

### <span data-ttu-id="808a3-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="808a3-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="808a3-126">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="808a3-126">The password of the administrator.</span></span>
<span data-ttu-id="808a3-127">Не менее 8 знаков и не более 128 знаков.</span><span class="sxs-lookup"><span data-stu-id="808a3-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="808a3-128">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="808a3-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808a3-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="808a3-129">-AdministratorUserName</span></span>
<span data-ttu-id="808a3-130">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="808a3-130">Administrator username for the server.</span></span>
<span data-ttu-id="808a3-131">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="808a3-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="808a3-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="808a3-132">-AsJob</span></span>
<span data-ttu-id="808a3-133">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="808a3-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="808a3-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="808a3-134">-BackupRetentionDay</span></span>
<span data-ttu-id="808a3-135">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="808a3-135">Backup retention days for the server.</span></span>
<span data-ttu-id="808a3-136">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="808a3-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="808a3-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808a3-137">-DefaultProfile</span></span>
<span data-ttu-id="808a3-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="808a3-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808a3-139">-HighAvailability</span><span class="sxs-lookup"><span data-stu-id="808a3-139">-HighAvailability</span></span>
<span data-ttu-id="808a3-140">Включить или отключить функцию высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="808a3-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="808a3-141">Значение по умолчанию отключено.</span><span class="sxs-lookup"><span data-stu-id="808a3-141">Default value is Disabled.</span></span>
<span data-ttu-id="808a3-142">По умолчанию: отключено.</span><span class="sxs-lookup"><span data-stu-id="808a3-142">Default: Disabled.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808a3-143">-Location</span><span class="sxs-lookup"><span data-stu-id="808a3-143">-Location</span></span>
<span data-ttu-id="808a3-144">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="808a3-144">The location the resource resides in.</span></span>

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

### <span data-ttu-id="808a3-145">-Name</span><span class="sxs-lookup"><span data-stu-id="808a3-145">-Name</span></span>
<span data-ttu-id="808a3-146">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="808a3-146">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808a3-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="808a3-147">-NoWait</span></span>
<span data-ttu-id="808a3-148">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="808a3-148">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="808a3-149">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="808a3-149">-PublicAccess</span></span>
<span data-ttu-id="808a3-150">Определяет общедоступный доступ.</span><span class="sxs-lookup"><span data-stu-id="808a3-150">Determines the public access.</span></span>
<span data-ttu-id="808a3-151">Введите один или несколько IP-адресов, которые будут включены в список разрешенных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="808a3-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="808a3-152">Диапазоны IP-адресов должны быть разделены тире и не содержать пробелов.</span><span class="sxs-lookup"><span data-stu-id="808a3-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="808a3-153">При указании 0.0.0.0 доступ к серверу обеспечивается для всех ресурсов, развернутых в Azure.</span><span class="sxs-lookup"><span data-stu-id="808a3-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="808a3-154">Если не указать IP-адрес, сервер будет перенаправиться в режим общего доступа, но правило брандмауэра не будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="808a3-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="808a3-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808a3-155">-ResourceGroupName</span></span>
<span data-ttu-id="808a3-156">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="808a3-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="808a3-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="808a3-157">-Sku</span></span>
<span data-ttu-id="808a3-158">Как правило, это название SKU уровня +family + cores, например Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="808a3-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="808a3-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="808a3-159">-SkuTier</span></span>
<span data-ttu-id="808a3-160">Вычислять уровень сервера.</span><span class="sxs-lookup"><span data-stu-id="808a3-160">Compute tier of the server.</span></span>
<span data-ttu-id="808a3-161">Принятые значения: Скайп, ОбщееТип, Оптимизированная память.</span><span class="sxs-lookup"><span data-stu-id="808a3-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="808a3-162">По умолчанию: срыв.</span><span class="sxs-lookup"><span data-stu-id="808a3-162">Default: Burstable.</span></span>

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

### <span data-ttu-id="808a3-163">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="808a3-163">-StorageInMb</span></span>
<span data-ttu-id="808a3-164">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="808a3-164">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="808a3-165">-Subnet</span><span class="sxs-lookup"><span data-stu-id="808a3-165">-Subnet</span></span>
<span data-ttu-id="808a3-166">Имя или ИД существующей подсети или имя новой подсети, которая требуется создать.</span><span class="sxs-lookup"><span data-stu-id="808a3-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="808a3-167">Обратите внимание, что подсеть будет делегирована microsoft.DBforMySQL/flexibleServers.</span><span class="sxs-lookup"><span data-stu-id="808a3-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="808a3-168">После делегирования эту подсеть нельзя использовать для других типов ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="808a3-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="808a3-169">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="808a3-169">-SubnetPrefix</span></span>
<span data-ttu-id="808a3-170">Префикс IP-адреса подсети, который используется при создании новой сети в формате CIDR.</span><span class="sxs-lookup"><span data-stu-id="808a3-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="808a3-171">Значение по умолчанию — 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="808a3-171">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="808a3-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="808a3-172">-SubscriptionId</span></span>
<span data-ttu-id="808a3-173">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="808a3-173">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="808a3-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="808a3-174">-Tag</span></span>
<span data-ttu-id="808a3-175">Метаданные приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="808a3-175">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="808a3-176">-Version</span><span class="sxs-lookup"><span data-stu-id="808a3-176">-Version</span></span>
<span data-ttu-id="808a3-177">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="808a3-177">Server version.</span></span>

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

### <span data-ttu-id="808a3-178">-Vnet</span><span class="sxs-lookup"><span data-stu-id="808a3-178">-Vnet</span></span>
<span data-ttu-id="808a3-179">Имя или ИД существующей виртуальной сети или имя новой создаемой сети.</span><span class="sxs-lookup"><span data-stu-id="808a3-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="808a3-180">Имя должно быть вме же от 2 до 64 символов.</span><span class="sxs-lookup"><span data-stu-id="808a3-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="808a3-181">Имя должно начинаться с буквы или числа, заканчивается буквой, числом или подчеркиваменем и может содержать только буквы, цифры, подчеркиваия, цыпцы или дефис.</span><span class="sxs-lookup"><span data-stu-id="808a3-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="808a3-182">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="808a3-182">-VnetPrefix</span></span>
<span data-ttu-id="808a3-183">Префикс IP-адреса, который используется при создании новой сети vnet в формате CIDR.</span><span class="sxs-lookup"><span data-stu-id="808a3-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="808a3-184">Значение по умолчанию — 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="808a3-184">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="808a3-185">-Zone</span><span class="sxs-lookup"><span data-stu-id="808a3-185">-Zone</span></span>
<span data-ttu-id="808a3-186">Зона доступности, в которую нужно подчистить ресурс.</span><span class="sxs-lookup"><span data-stu-id="808a3-186">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="808a3-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="808a3-187">-Confirm</span></span>
<span data-ttu-id="808a3-188">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="808a3-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="808a3-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="808a3-189">-WhatIf</span></span>
<span data-ttu-id="808a3-190">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808a3-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="808a3-191">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="808a3-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="808a3-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808a3-192">CommonParameters</span></span>
<span data-ttu-id="808a3-193">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808a3-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808a3-194">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="808a3-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808a3-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="808a3-195">INPUTS</span></span>

## <span data-ttu-id="808a3-196">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="808a3-196">OUTPUTS</span></span>

### <span data-ttu-id="808a3-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="808a3-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="808a3-198">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="808a3-198">NOTES</span></span>

<span data-ttu-id="808a3-199">ALIASES</span><span class="sxs-lookup"><span data-stu-id="808a3-199">ALIASES</span></span>

## <span data-ttu-id="808a3-200">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="808a3-200">RELATED LINKS</span></span>

