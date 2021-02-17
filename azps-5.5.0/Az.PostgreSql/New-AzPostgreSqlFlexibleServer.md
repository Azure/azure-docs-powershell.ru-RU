---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c658780407454f780ccbd00cb824dd1032f3463d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227220"
---
# <span data-ttu-id="2c686-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="2c686-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="2c686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c686-102">SYNOPSIS</span></span>
<span data-ttu-id="2c686-103">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="2c686-103">Creates a new server.</span></span>

## <span data-ttu-id="2c686-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c686-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2c686-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c686-105">DESCRIPTION</span></span>
<span data-ttu-id="2c686-106">Создается новый сервер.</span><span class="sxs-lookup"><span data-stu-id="2c686-106">Creates a new server.</span></span>

## <span data-ttu-id="2c686-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c686-107">EXAMPLES</span></span>

### <span data-ttu-id="2c686-108">Пример 1. Создание нового гибкого сервера PostgreSql с аргументами</span><span class="sxs-lookup"><span data-stu-id="2c686-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="2c686-109">Пример 2. Создание нового гибкого сервера PostgreSql с настройкой по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c686-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="2c686-110">Этот cmdlet создает гибкий сервер PostgreSql со значениями параметров по умолчанию и создает сервер в новой виртуальной сети и делегирует серверу подсеть.</span><span class="sxs-lookup"><span data-stu-id="2c686-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="2c686-111">По умолчанию местоположение имеет значение West US 2, SKU — Standard_D2s_v3, SKU — GeneralPurpose, а размер хранилища — 128GiB.</span><span class="sxs-lookup"><span data-stu-id="2c686-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="2c686-112">Если вы хотите найти автоматически созданный пароль для сервера, ConvertFrom-SecureString преобразуйте свойство SecuredPassword в обычный текст.</span><span class="sxs-lookup"><span data-stu-id="2c686-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="2c686-113">(Например, $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="2c686-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="2c686-114">Пример 3. Создание нового гибкого сервера PostgreSql с виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="2c686-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="2c686-115">Этот cmdlet создает гибкий сервер PostgreSql с ИД vnet или именем vnet, предоставленным пользователем.</span><span class="sxs-lookup"><span data-stu-id="2c686-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="2c686-116">Если виртуальная сеть не существует, ее создает cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c686-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="2c686-117">Пример 4. Создание нового гибкого сервера PostgreSql с именем виртуальной сети и подсети</span><span class="sxs-lookup"><span data-stu-id="2c686-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="2c686-118">Этот cmdlet создает гибкий сервер PostgreSql с именем vnet, именем подсети, префиксом vnet и префиксом подсети.</span><span class="sxs-lookup"><span data-stu-id="2c686-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="2c686-119">Если виртуальная сеть и подсеть не существуют, будет создаться ее с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="2c686-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="2c686-120">Пример 7. Создание нового гибкого сервера PostgreSql с общедоступным доступом ко всем IP-данным</span><span class="sxs-lookup"><span data-stu-id="2c686-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="2c686-121">Этот cmdlet создает гибкий сервер PostgreSql, открытый для всех IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2c686-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="2c686-122">Пример 8. Создание нового гибкого сервера PostgreSql с брандмауэром</span><span class="sxs-lookup"><span data-stu-id="2c686-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="2c686-123">Этот cmdlet создает гибкий сервер PostgreSql, открытый по указанным IP-адресам.</span><span class="sxs-lookup"><span data-stu-id="2c686-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="2c686-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c686-124">PARAMETERS</span></span>

### <span data-ttu-id="2c686-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="2c686-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="2c686-126">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="2c686-126">The password of the administrator.</span></span>
<span data-ttu-id="2c686-127">Не менее 8 знаков и не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="2c686-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="2c686-128">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="2c686-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="2c686-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="2c686-129">-AdministratorUserName</span></span>
<span data-ttu-id="2c686-130">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="2c686-130">Administrator username for the server.</span></span>
<span data-ttu-id="2c686-131">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="2c686-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="2c686-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c686-132">-AsJob</span></span>
<span data-ttu-id="2c686-133">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="2c686-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="2c686-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="2c686-134">-BackupRetentionDay</span></span>
<span data-ttu-id="2c686-135">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="2c686-135">Backup retention days for the server.</span></span>
<span data-ttu-id="2c686-136">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="2c686-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="2c686-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c686-137">-DefaultProfile</span></span>
<span data-ttu-id="2c686-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c686-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c686-139">-Location</span><span class="sxs-lookup"><span data-stu-id="2c686-139">-Location</span></span>
<span data-ttu-id="2c686-140">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c686-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="2c686-141">-Name</span><span class="sxs-lookup"><span data-stu-id="2c686-141">-Name</span></span>
<span data-ttu-id="2c686-142">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2c686-142">The name of the server.</span></span>

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

### <span data-ttu-id="2c686-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2c686-143">-NoWait</span></span>
<span data-ttu-id="2c686-144">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="2c686-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="2c686-145">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="2c686-145">-PublicAccess</span></span>
<span data-ttu-id="2c686-146">Определяет общедоступный доступ.</span><span class="sxs-lookup"><span data-stu-id="2c686-146">Determines the public access.</span></span>
<span data-ttu-id="2c686-147">Введите один или несколько IP-адресов, которые будут включены в список разрешенных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2c686-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="2c686-148">Диапазоны IP-адресов должны быть разделены тире и не содержать пробелов.</span><span class="sxs-lookup"><span data-stu-id="2c686-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="2c686-149">При указании 0.0.0.0 доступ к серверу обеспечивается для всех ресурсов, развернутых в Azure.</span><span class="sxs-lookup"><span data-stu-id="2c686-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="2c686-150">Если не указать IP-адрес, сервер будет перенаправиться в режим общего доступа, но правило брандмауэра не будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="2c686-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="2c686-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c686-151">-ResourceGroupName</span></span>
<span data-ttu-id="2c686-152">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="2c686-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2c686-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="2c686-153">-Sku</span></span>
<span data-ttu-id="2c686-154">Как правило, это название SKU уровня +family + cores, например Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="2c686-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="2c686-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2c686-155">-SkuTier</span></span>
<span data-ttu-id="2c686-156">Вычислять уровень сервера.</span><span class="sxs-lookup"><span data-stu-id="2c686-156">Compute tier of the server.</span></span>
<span data-ttu-id="2c686-157">Принятые значения: Скайп, ОбщееТип, Оптимизированная память.</span><span class="sxs-lookup"><span data-stu-id="2c686-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="2c686-158">По умолчанию: срыв.</span><span class="sxs-lookup"><span data-stu-id="2c686-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="2c686-159">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="2c686-159">-StorageInMb</span></span>
<span data-ttu-id="2c686-160">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="2c686-160">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="2c686-161">-Subnet</span><span class="sxs-lookup"><span data-stu-id="2c686-161">-Subnet</span></span>
<span data-ttu-id="2c686-162">Имя или ИД существующей подсети или имя новой подсети, которая требуется создать.</span><span class="sxs-lookup"><span data-stu-id="2c686-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="2c686-163">Обратите внимание, что подсеть будет делегирована службе Microsoft.DBforPostgreSQL/flexibleServers.</span><span class="sxs-lookup"><span data-stu-id="2c686-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="2c686-164">После делегирования эту подсеть нельзя использовать для других типов ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2c686-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="2c686-165">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="2c686-165">-SubnetPrefix</span></span>
<span data-ttu-id="2c686-166">Префикс IP-адреса подсети, который используется при создании новой сети в формате CIDR.</span><span class="sxs-lookup"><span data-stu-id="2c686-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="2c686-167">Значение по умолчанию — 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="2c686-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="2c686-168">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c686-168">-SubscriptionId</span></span>
<span data-ttu-id="2c686-169">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="2c686-169">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="2c686-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c686-170">-Tag</span></span>
<span data-ttu-id="2c686-171">Метаданные приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="2c686-171">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="2c686-172">-Версия</span><span class="sxs-lookup"><span data-stu-id="2c686-172">-Version</span></span>
<span data-ttu-id="2c686-173">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="2c686-173">Server version.</span></span>

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

### <span data-ttu-id="2c686-174">-Vnet</span><span class="sxs-lookup"><span data-stu-id="2c686-174">-Vnet</span></span>
<span data-ttu-id="2c686-175">Имя или ИД существующей виртуальной сети или имя новой создаемой сети.</span><span class="sxs-lookup"><span data-stu-id="2c686-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="2c686-176">Имя должно быть вме же от 2 до 64 символов.</span><span class="sxs-lookup"><span data-stu-id="2c686-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="2c686-177">Имя должно начинаться с буквы или числа, заканчивается буквой, числом или подчеркиваменем и может содержать только буквы, цифры, подчеркиваия, цыпцы или дефис.</span><span class="sxs-lookup"><span data-stu-id="2c686-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="2c686-178">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="2c686-178">-VnetPrefix</span></span>
<span data-ttu-id="2c686-179">Префикс IP-адреса, который используется при создании новой сети vnet в формате CIDR.</span><span class="sxs-lookup"><span data-stu-id="2c686-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="2c686-180">Значение по умолчанию — 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="2c686-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="2c686-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c686-181">-Confirm</span></span>
<span data-ttu-id="2c686-182">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2c686-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c686-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c686-183">-WhatIf</span></span>
<span data-ttu-id="2c686-184">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c686-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c686-185">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2c686-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c686-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c686-186">CommonParameters</span></span>
<span data-ttu-id="2c686-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c686-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c686-188">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c686-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c686-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c686-189">INPUTS</span></span>

## <span data-ttu-id="2c686-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c686-190">OUTPUTS</span></span>

### <span data-ttu-id="2c686-191">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="2c686-191">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="2c686-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c686-192">NOTES</span></span>

<span data-ttu-id="2c686-193">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2c686-193">ALIASES</span></span>

## <span data-ttu-id="2c686-194">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c686-194">RELATED LINKS</span></span>

