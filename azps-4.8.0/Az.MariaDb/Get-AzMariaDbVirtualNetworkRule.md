---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236279"
---
# <span data-ttu-id="1883b-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1883b-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="1883b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1883b-102">SYNOPSIS</span></span>
<span data-ttu-id="1883b-103">Возвращает правило виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1883b-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="1883b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1883b-104">SYNTAX</span></span>

### <span data-ttu-id="1883b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1883b-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1883b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="1883b-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1883b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1883b-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="1883b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1883b-108">DESCRIPTION</span></span>
<span data-ttu-id="1883b-109">Возвращает правило виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1883b-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="1883b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1883b-110">EXAMPLES</span></span>

### <span data-ttu-id="1883b-111">Пример 1: список всех виртуальных сетевых правил в MariaDB</span><span class="sxs-lookup"><span data-stu-id="1883b-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="1883b-112">В этой команде перечислены все правила для всех виртуальных сетей в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="1883b-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="1883b-113">Пример 2: получение правила виртуальной сети для MariaDB</span><span class="sxs-lookup"><span data-stu-id="1883b-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="1883b-114">Эта команда получает правило виртуальной сети в разделе MariaDB.</span><span class="sxs-lookup"><span data-stu-id="1883b-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="1883b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1883b-115">PARAMETERS</span></span>

### <span data-ttu-id="1883b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1883b-116">-DefaultProfile</span></span>
<span data-ttu-id="1883b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1883b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1883b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1883b-118">-InputObject</span></span>
<span data-ttu-id="1883b-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1883b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1883b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1883b-120">-Name</span></span>
<span data-ttu-id="1883b-121">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1883b-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1883b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1883b-122">-PassThru</span></span>
<span data-ttu-id="1883b-123">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1883b-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1883b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1883b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1883b-125">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="1883b-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1883b-126">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="1883b-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1883b-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1883b-127">-ServerName</span></span>
<span data-ttu-id="1883b-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1883b-128">The name of the server.</span></span>

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

### <span data-ttu-id="1883b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1883b-129">-SubscriptionId</span></span>
<span data-ttu-id="1883b-130">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="1883b-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="1883b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1883b-131">CommonParameters</span></span>
<span data-ttu-id="1883b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1883b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1883b-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1883b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1883b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1883b-134">INPUTS</span></span>

### <span data-ttu-id="1883b-135">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="1883b-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="1883b-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1883b-136">OUTPUTS</span></span>

### <span data-ttu-id="1883b-137">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1883b-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="1883b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1883b-138">NOTES</span></span>

<span data-ttu-id="1883b-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1883b-139">ALIASES</span></span>

<span data-ttu-id="1883b-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1883b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1883b-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1883b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1883b-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1883b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1883b-143">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1883b-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1883b-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="1883b-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1883b-145">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="1883b-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1883b-146">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="1883b-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1883b-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1883b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1883b-148">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="1883b-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1883b-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="1883b-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1883b-150">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="1883b-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1883b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="1883b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1883b-152">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1883b-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1883b-153">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="1883b-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="1883b-154">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1883b-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1883b-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1883b-155">RELATED LINKS</span></span>

