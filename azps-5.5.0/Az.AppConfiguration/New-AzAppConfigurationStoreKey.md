---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216369"
---
# <span data-ttu-id="cc3f9-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="cc3f9-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="cc3f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc3f9-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3f9-103">Повторно сгенерирует ключ доступа для указанного магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="cc3f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc3f9-104">SYNTAX</span></span>

### <span data-ttu-id="cc3f9-105">RegenerateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc3f9-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc3f9-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cc3f9-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc3f9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc3f9-107">DESCRIPTION</span></span>
<span data-ttu-id="cc3f9-108">Повторно сгенерирует ключ доступа для указанного магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="cc3f9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc3f9-109">EXAMPLES</span></span>

### <span data-ttu-id="cc3f9-110">Пример 1. Повторное сгенерация ключа магазина конфигурации приложений</span><span class="sxs-lookup"><span data-stu-id="cc3f9-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="cc3f9-111">Эта команда повторно сгенерирует ключ из магазина конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="cc3f9-112">Пример 2. Повторное сгенерация ключа магазина конфигурации приложения по объекту</span><span class="sxs-lookup"><span data-stu-id="cc3f9-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="cc3f9-113">Эта команда повторно сгенерирует ключ из магазина конфигурации приложения по объекту.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="cc3f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc3f9-114">PARAMETERS</span></span>

### <span data-ttu-id="cc3f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3f9-115">-DefaultProfile</span></span>
<span data-ttu-id="cc3f9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc3f9-117">-Id</span><span class="sxs-lookup"><span data-stu-id="cc3f9-117">-Id</span></span>
<span data-ttu-id="cc3f9-118">ИД ключа для повторного сгенерации.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="cc3f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc3f9-119">-InputObject</span></span>
<span data-ttu-id="cc3f9-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc3f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cc3f9-121">-Name</span></span>
<span data-ttu-id="cc3f9-122">Имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc3f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc3f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc3f9-124">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc3f9-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc3f9-125">-SubscriptionId</span></span>
<span data-ttu-id="cc3f9-126">ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc3f9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc3f9-127">-Confirm</span></span>
<span data-ttu-id="cc3f9-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc3f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc3f9-129">-WhatIf</span></span>
<span data-ttu-id="cc3f9-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc3f9-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc3f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3f9-132">CommonParameters</span></span>
<span data-ttu-id="cc3f9-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3f9-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc3f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3f9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc3f9-135">INPUTS</span></span>

### <span data-ttu-id="cc3f9-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="cc3f9-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="cc3f9-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc3f9-137">OUTPUTS</span></span>

### <span data-ttu-id="cc3f9-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="cc3f9-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="cc3f9-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc3f9-139">NOTES</span></span>

<span data-ttu-id="cc3f9-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cc3f9-140">ALIASES</span></span>

<span data-ttu-id="cc3f9-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cc3f9-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc3f9-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc3f9-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc3f9-144">INPUTOBJECT <IAppConfigurationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="cc3f9-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc3f9-145">`[ConfigStoreName <String>]`: имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="cc3f9-146">`[GroupName <String>]`: Имя закрытой группы ресурсов, связываемой с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="cc3f9-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="cc3f9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc3f9-148">`[PrivateEndpointConnectionName <String>]`: имя подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="cc3f9-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="cc3f9-149">`[ResourceGroupName <String>]`: имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="cc3f9-150">`[SubscriptionId <String>]`: ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3f9-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="cc3f9-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc3f9-151">RELATED LINKS</span></span>

