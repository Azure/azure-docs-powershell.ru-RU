---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243741"
---
# <span data-ttu-id="80979-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="80979-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="80979-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80979-102">SYNOPSIS</span></span>
<span data-ttu-id="80979-103">Повторно создает клавишу доступа для указанного хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="80979-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="80979-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80979-104">SYNTAX</span></span>

### <span data-ttu-id="80979-105">RegenerateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80979-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80979-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="80979-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80979-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80979-107">DESCRIPTION</span></span>
<span data-ttu-id="80979-108">Повторно создает клавишу доступа для указанного хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="80979-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="80979-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80979-109">EXAMPLES</span></span>

### <span data-ttu-id="80979-110">Пример 1: повторное создание ключа из хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="80979-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="80979-111">Эта команда повторное создание ключа из хранилища конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="80979-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="80979-112">Пример 2: повторное создание ключа из хранилища конфигурации приложения по объекту</span><span class="sxs-lookup"><span data-stu-id="80979-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="80979-113">Эта команда используется для повторного создания ключа хранилища конфигурации приложения по объекту.</span><span class="sxs-lookup"><span data-stu-id="80979-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="80979-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80979-114">PARAMETERS</span></span>

### <span data-ttu-id="80979-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80979-115">-DefaultProfile</span></span>
<span data-ttu-id="80979-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80979-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80979-117">-ID</span><span class="sxs-lookup"><span data-stu-id="80979-117">-Id</span></span>
<span data-ttu-id="80979-118">Идентификатор ключа, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="80979-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="80979-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80979-119">-InputObject</span></span>
<span data-ttu-id="80979-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="80979-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80979-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80979-121">-Name</span></span>
<span data-ttu-id="80979-122">Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="80979-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="80979-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80979-123">-ResourceGroupName</span></span>
<span data-ttu-id="80979-124">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="80979-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="80979-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80979-125">-SubscriptionId</span></span>
<span data-ttu-id="80979-126">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="80979-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="80979-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80979-127">-Confirm</span></span>
<span data-ttu-id="80979-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80979-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80979-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80979-129">-WhatIf</span></span>
<span data-ttu-id="80979-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80979-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80979-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80979-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80979-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80979-132">CommonParameters</span></span>
<span data-ttu-id="80979-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80979-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80979-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80979-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80979-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80979-135">INPUTS</span></span>

### <span data-ttu-id="80979-136">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="80979-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="80979-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80979-137">OUTPUTS</span></span>

### <span data-ttu-id="80979-138">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="80979-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="80979-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="80979-139">NOTES</span></span>

<span data-ttu-id="80979-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="80979-140">ALIASES</span></span>

<span data-ttu-id="80979-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="80979-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80979-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="80979-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80979-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80979-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80979-144">INPUTOBJECT <IAppConfigurationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="80979-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80979-145">`[ConfigStoreName <String>]`: Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="80979-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="80979-146">`[GroupName <String>]`: Имя группы ресурсов частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="80979-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="80979-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="80979-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80979-148">`[PrivateEndpointConnectionName <String>]`: Имя частного подключения конечной точки</span><span class="sxs-lookup"><span data-stu-id="80979-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="80979-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="80979-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="80979-150">`[SubscriptionId <String>]`: Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="80979-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="80979-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80979-151">RELATED LINKS</span></span>
