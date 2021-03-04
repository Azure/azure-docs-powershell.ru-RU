---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1e49f5937196a402e051d28665614befbf6eb04c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953560"
---
# <span data-ttu-id="fb41f-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="fb41f-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="fb41f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb41f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb41f-103">Проверка подключения к серверу базы данных</span><span class="sxs-lookup"><span data-stu-id="fb41f-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="fb41f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb41f-104">SYNTAX</span></span>

### <span data-ttu-id="fb41f-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb41f-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fb41f-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="fb41f-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fb41f-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb41f-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fb41f-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="fb41f-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fb41f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb41f-109">DESCRIPTION</span></span>
<span data-ttu-id="fb41f-110">Проверка подключения к серверу базы данных</span><span class="sxs-lookup"><span data-stu-id="fb41f-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="fb41f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb41f-111">EXAMPLES</span></span>

### <span data-ttu-id="fb41f-112">Пример 1. Проверка подключения по имени</span><span class="sxs-lookup"><span data-stu-id="fb41f-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="fb41f-113">Проверка подключения по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="fb41f-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="fb41f-114">Пример 2. Проверка подключения по удостоверению</span><span class="sxs-lookup"><span data-stu-id="fb41f-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="fb41f-115">Проверка подключения по удостоверению</span><span class="sxs-lookup"><span data-stu-id="fb41f-115">Test connection by the identity</span></span>

### <span data-ttu-id="fb41f-116">Пример 3. Проверка запроса по имени</span><span class="sxs-lookup"><span data-stu-id="fb41f-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="fb41f-117">Проверка запроса по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="fb41f-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="fb41f-118">Пример 4. Проверка подключения по удостоверению</span><span class="sxs-lookup"><span data-stu-id="fb41f-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="fb41f-119">Проверка запроса по удостоверению</span><span class="sxs-lookup"><span data-stu-id="fb41f-119">Test a query by the identity</span></span>

## <span data-ttu-id="fb41f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb41f-120">PARAMETERS</span></span>

### <span data-ttu-id="fb41f-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="fb41f-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="fb41f-122">Пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="fb41f-122">The password of the administrator.</span></span>
<span data-ttu-id="fb41f-123">Не менее 8 знаков и не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="fb41f-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="fb41f-124">Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="fb41f-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="fb41f-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="fb41f-125">-AdministratorUserName</span></span>
<span data-ttu-id="fb41f-126">Имя пользователя администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="fb41f-126">Administrator username for the server.</span></span>
<span data-ttu-id="fb41f-127">После этого изменить его будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="fb41f-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="fb41f-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb41f-128">-DatabaseName</span></span>
<span data-ttu-id="fb41f-129">Имя базы данных, к которой нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="fb41f-129">The database name to connect.</span></span>

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

### <span data-ttu-id="fb41f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb41f-130">-DefaultProfile</span></span>
<span data-ttu-id="fb41f-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb41f-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb41f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb41f-132">-InputObject</span></span>
<span data-ttu-id="fb41f-133">Сервер для подключения.</span><span class="sxs-lookup"><span data-stu-id="fb41f-133">The server to connect.</span></span>
<span data-ttu-id="fb41f-134">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="fb41f-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb41f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="fb41f-135">-Name</span></span>
<span data-ttu-id="fb41f-136">Имя сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="fb41f-136">The name of the server to connect.</span></span>

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

### <span data-ttu-id="fb41f-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="fb41f-137">-QueryText</span></span>
<span data-ttu-id="fb41f-138">Проверяемая база данных запроса</span><span class="sxs-lookup"><span data-stu-id="fb41f-138">The query for the database to test</span></span>

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

### <span data-ttu-id="fb41f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb41f-139">-ResourceGroupName</span></span>
<span data-ttu-id="fb41f-140">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fb41f-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fb41f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb41f-141">CommonParameters</span></span>
<span data-ttu-id="fb41f-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb41f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb41f-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb41f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb41f-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb41f-144">INPUTS</span></span>

### <span data-ttu-id="fb41f-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fb41f-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fb41f-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb41f-146">OUTPUTS</span></span>

### <span data-ttu-id="fb41f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="fb41f-147">System.String</span></span>

## <span data-ttu-id="fb41f-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb41f-148">NOTES</span></span>

<span data-ttu-id="fb41f-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fb41f-149">ALIASES</span></span>

<span data-ttu-id="fb41f-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fb41f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb41f-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fb41f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb41f-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb41f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb41f-153">INPUTOBJECT: <IPostgreSqlIdentity> сервер для подключения.</span><span class="sxs-lookup"><span data-stu-id="fb41f-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="fb41f-154">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="fb41f-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fb41f-155">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb41f-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fb41f-156">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="fb41f-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fb41f-157">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="fb41f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb41f-158">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="fb41f-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fb41f-159">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb41f-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fb41f-160">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="fb41f-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="fb41f-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="fb41f-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fb41f-162">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fb41f-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fb41f-163">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fb41f-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fb41f-164">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="fb41f-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fb41f-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb41f-165">RELATED LINKS</span></span>

