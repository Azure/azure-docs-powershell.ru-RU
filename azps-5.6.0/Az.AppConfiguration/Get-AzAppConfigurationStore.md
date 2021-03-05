---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: e7f7c1f7493123793a32163b4e8f37bec8706e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998248"
---
# <span data-ttu-id="7332e-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="7332e-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="7332e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7332e-102">SYNOPSIS</span></span>
<span data-ttu-id="7332e-103">Получить или с помощью списка хранилищ конфигурации приложений.</span><span class="sxs-lookup"><span data-stu-id="7332e-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="7332e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7332e-104">SYNTAX</span></span>

### <span data-ttu-id="7332e-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7332e-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7332e-106">Получить</span><span class="sxs-lookup"><span data-stu-id="7332e-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7332e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7332e-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7332e-108">List1</span><span class="sxs-lookup"><span data-stu-id="7332e-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7332e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7332e-109">DESCRIPTION</span></span>
<span data-ttu-id="7332e-110">Получить или с помощью списка хранилищ конфигурации приложений.</span><span class="sxs-lookup"><span data-stu-id="7332e-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="7332e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7332e-111">EXAMPLES</span></span>

### <span data-ttu-id="7332e-112">Пример 1. Список всех хранилищ конфигурации приложений в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="7332e-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7332e-113">Эта команда содержит список всех хранилищ конфигурации приложений, которые находятся в подписке.</span><span class="sxs-lookup"><span data-stu-id="7332e-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="7332e-114">Пример 2. Список всех хранилищ конфигурации приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="7332e-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7332e-115">Эта команда содержит список всех хранилищ конфигурации приложений, которые находятся в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7332e-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="7332e-116">Пример 3. Получить хранилище конфигурации приложения по имени</span><span class="sxs-lookup"><span data-stu-id="7332e-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7332e-117">Эта команда получает хранилище конфигурации приложения по имени.</span><span class="sxs-lookup"><span data-stu-id="7332e-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="7332e-118">Пример 4. Получить хранилище конфигурации приложений по конвейеру</span><span class="sxs-lookup"><span data-stu-id="7332e-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7332e-119">Эта команда получает хранилище конфигурации приложения по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="7332e-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="7332e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7332e-120">PARAMETERS</span></span>

### <span data-ttu-id="7332e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7332e-121">-DefaultProfile</span></span>
<span data-ttu-id="7332e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7332e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7332e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7332e-123">-InputObject</span></span>
<span data-ttu-id="7332e-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="7332e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7332e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7332e-125">-Name</span></span>
<span data-ttu-id="7332e-126">Имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7332e-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7332e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7332e-127">-ResourceGroupName</span></span>
<span data-ttu-id="7332e-128">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="7332e-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7332e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7332e-129">-SubscriptionId</span></span>
<span data-ttu-id="7332e-130">ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7332e-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7332e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7332e-131">CommonParameters</span></span>
<span data-ttu-id="7332e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7332e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7332e-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7332e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7332e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7332e-134">INPUTS</span></span>

### <span data-ttu-id="7332e-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="7332e-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="7332e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7332e-136">OUTPUTS</span></span>

### <span data-ttu-id="7332e-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="7332e-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="7332e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7332e-138">NOTES</span></span>

<span data-ttu-id="7332e-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7332e-139">ALIASES</span></span>

<span data-ttu-id="7332e-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7332e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7332e-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="7332e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7332e-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7332e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7332e-143">INPUTOBJECT <IAppConfigurationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="7332e-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7332e-144">`[ConfigStoreName <String>]`: имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7332e-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="7332e-145">`[GroupName <String>]`: Имя закрытой группы ресурсов, связываемой с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="7332e-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="7332e-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="7332e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7332e-147">`[PrivateEndpointConnectionName <String>]`: имя подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="7332e-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="7332e-148">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="7332e-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="7332e-149">`[SubscriptionId <String>]`: ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7332e-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="7332e-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7332e-150">RELATED LINKS</span></span>

