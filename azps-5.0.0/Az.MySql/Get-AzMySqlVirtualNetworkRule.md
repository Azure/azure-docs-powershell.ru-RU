---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 91d774931ac7ef4b8f1d41a70953d4a5b3a322cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247690"
---
# <span data-ttu-id="fd1a1-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fd1a1-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="fd1a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fd1a1-103">Возвращает правило виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="fd1a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd1a1-104">SYNTAX</span></span>

### <span data-ttu-id="fd1a1-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd1a1-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fd1a1-106">Получить</span><span class="sxs-lookup"><span data-stu-id="fd1a1-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fd1a1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd1a1-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="fd1a1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-108">DESCRIPTION</span></span>
<span data-ttu-id="fd1a1-109">Возвращает правило виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="fd1a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-110">EXAMPLES</span></span>

### <span data-ttu-id="fd1a1-111">Пример 1: список всех правил виртуальных сетей в указанном сервере MySql</span><span class="sxs-lookup"><span data-stu-id="fd1a1-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="fd1a1-112">Этот командлет перечисление всех правил виртуальных сетей в указанном сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="fd1a1-113">Пример 2: получение правила виртуальной сети по имени</span><span class="sxs-lookup"><span data-stu-id="fd1a1-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="fd1a1-114">Этот командлет получает правило виртуальной сети по имени.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="fd1a1-115">Пример 3: получение правила для виртуальной сети по удостоверению</span><span class="sxs-lookup"><span data-stu-id="fd1a1-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="fd1a1-116">Этот командлет получает правило виртуальной сети по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="fd1a1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-117">PARAMETERS</span></span>

### <span data-ttu-id="fd1a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd1a1-118">-DefaultProfile</span></span>
<span data-ttu-id="fd1a1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd1a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd1a1-120">-InputObject</span></span>
<span data-ttu-id="fd1a1-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd1a1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd1a1-122">-Name</span></span>
<span data-ttu-id="fd1a1-123">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd1a1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd1a1-124">-PassThru</span></span>
<span data-ttu-id="fd1a1-125">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fd1a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd1a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd1a1-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-127">The name of the resource group.</span></span>
<span data-ttu-id="fd1a1-128">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-128">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd1a1-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fd1a1-129">-ServerName</span></span>
<span data-ttu-id="fd1a1-130">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-130">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd1a1-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd1a1-131">-SubscriptionId</span></span>
<span data-ttu-id="fd1a1-132">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd1a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd1a1-133">CommonParameters</span></span>
<span data-ttu-id="fd1a1-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd1a1-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd1a1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd1a1-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd1a1-136">INPUTS</span></span>

### <span data-ttu-id="fd1a1-137">Microsoft. Azure. PowerShell. командлеты. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fd1a1-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="fd1a1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-138">OUTPUTS</span></span>

### <span data-ttu-id="fd1a1-139">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fd1a1-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="fd1a1-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd1a1-140">NOTES</span></span>

<span data-ttu-id="fd1a1-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-141">ALIASES</span></span>

<span data-ttu-id="fd1a1-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd1a1-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd1a1-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd1a1-145">INPUTOBJECT <IMySqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="fd1a1-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd1a1-146">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fd1a1-147">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fd1a1-148">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fd1a1-149">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="fd1a1-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd1a1-150">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fd1a1-151">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fd1a1-152">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="fd1a1-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fd1a1-154">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fd1a1-155">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fd1a1-156">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd1a1-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fd1a1-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-157">RELATED LINKS</span></span>

