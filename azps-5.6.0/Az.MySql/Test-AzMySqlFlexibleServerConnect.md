---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/test-azmysqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
ms.openlocfilehash: 5616eb79575154e2cbd5128f10eabc1913c9d506
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968840"
---
# <span data-ttu-id="b386c-101">Test-AzMySqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="b386c-101">Test-AzMySqlFlexibleServerConnect</span></span>

## <span data-ttu-id="b386c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b386c-102">SYNOPSIS</span></span>
<span data-ttu-id="b386c-103">Проверка подключения к серверу базы данных</span><span class="sxs-lookup"><span data-stu-id="b386c-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="b386c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b386c-104">SYNTAX</span></span>

### <span data-ttu-id="b386c-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b386c-105">Test (Default)</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b386c-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="b386c-106">TestAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b386c-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b386c-107">TestViaIdentity</span></span>
```
Test-AzMySqlFlexibleServerConnect -AdministratorLoginPassword <SecureString> -InputObject <IMySqlIdentity>
 [-DatabaseName <String>] [-AdministratorUserName <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b386c-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="b386c-108">TestViaIdentityAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IMySqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b386c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b386c-109">DESCRIPTION</span></span>
<span data-ttu-id="b386c-110">Проверка подключения к серверу базы данных</span><span class="sxs-lookup"><span data-stu-id="b386c-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="b386c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b386c-111">EXAMPLES</span></span>

### <span data-ttu-id="b386c-112">Пример 1. Проверка подключения по имени</span><span class="sxs-lookup"><span data-stu-id="b386c-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="b386c-113">Проверка подключения по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="b386c-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="b386c-114">Пример 2. Проверка подключения по удостоверению</span><span class="sxs-lookup"><span data-stu-id="b386c-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="b386c-115">Проверка подключения по удостоверению</span><span class="sxs-lookup"><span data-stu-id="b386c-115">Test connection by the identity</span></span>

### <span data-ttu-id="b386c-116">Пример 3. Проверка запроса по имени</span><span class="sxs-lookup"><span data-stu-id="b386c-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="b386c-117">Проверка запроса по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="b386c-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="b386c-118">Пример 4. Проверка подключения по удостоверению</span><span class="sxs-lookup"><span data-stu-id="b386c-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="b386c-119">Проверка запроса по удостоверению</span><span class="sxs-lookup"><span data-stu-id="b386c-119">Test a query by the identity</span></span>

## <span data-ttu-id="b386c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b386c-120">PARAMETERS</span></span>

### <span data-ttu-id="b386c-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b386c-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b386c-122">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="b386c-122">The password of the administrator.</span></span>
<span data-ttu-id="b386c-123">Не менее 8 знаков и не более 128 знаков.</span><span class="sxs-lookup"><span data-stu-id="b386c-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b386c-124">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="b386c-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="b386c-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b386c-125">-AdministratorUserName</span></span>
<span data-ttu-id="b386c-126">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="b386c-126">Administrator username for the server.</span></span>
<span data-ttu-id="b386c-127">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="b386c-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b386c-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b386c-128">-DatabaseName</span></span>
<span data-ttu-id="b386c-129">Имя базы данных, к которой нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="b386c-129">The database name to connect.</span></span>

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

### <span data-ttu-id="b386c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b386c-130">-DefaultProfile</span></span>
<span data-ttu-id="b386c-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b386c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b386c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b386c-132">-InputObject</span></span>
<span data-ttu-id="b386c-133">Сервер для подключения.</span><span class="sxs-lookup"><span data-stu-id="b386c-133">The server to connect.</span></span>
<span data-ttu-id="b386c-134">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="b386c-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b386c-135">-Name</span><span class="sxs-lookup"><span data-stu-id="b386c-135">-Name</span></span>
<span data-ttu-id="b386c-136">Имя сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="b386c-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386c-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="b386c-137">-QueryText</span></span>
<span data-ttu-id="b386c-138">Проверяемая база данных запроса</span><span class="sxs-lookup"><span data-stu-id="b386c-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b386c-139">-ResourceGroupName</span></span>
<span data-ttu-id="b386c-140">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b386c-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b386c-141">CommonParameters</span></span>
<span data-ttu-id="b386c-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b386c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b386c-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b386c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b386c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b386c-144">INPUTS</span></span>

### <span data-ttu-id="b386c-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b386c-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b386c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b386c-146">OUTPUTS</span></span>

### <span data-ttu-id="b386c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b386c-147">System.String</span></span>

## <span data-ttu-id="b386c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b386c-148">NOTES</span></span>

<span data-ttu-id="b386c-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b386c-149">ALIASES</span></span>

<span data-ttu-id="b386c-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b386c-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b386c-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b386c-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b386c-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b386c-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b386c-153">INPUTOBJECT: <IMySqlIdentity> сервер для подключения.</span><span class="sxs-lookup"><span data-stu-id="b386c-153">INPUTOBJECT <IMySqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="b386c-154">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="b386c-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b386c-155">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b386c-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b386c-156">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="b386c-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b386c-157">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b386c-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b386c-158">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="b386c-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b386c-159">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="b386c-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b386c-160">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b386c-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b386c-161">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b386c-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="b386c-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="b386c-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b386c-163">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b386c-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b386c-164">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b386c-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b386c-165">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="b386c-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b386c-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b386c-166">RELATED LINKS</span></span>

