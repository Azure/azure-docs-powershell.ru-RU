---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077985"
---
# <span data-ttu-id="f0c98-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="f0c98-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="f0c98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0c98-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c98-103">Получение или перечисление хранилищ конфигураций приложений.</span><span class="sxs-lookup"><span data-stu-id="f0c98-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="f0c98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0c98-104">SYNTAX</span></span>

### <span data-ttu-id="f0c98-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0c98-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0c98-106">Получить</span><span class="sxs-lookup"><span data-stu-id="f0c98-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0c98-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0c98-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0c98-108">List1</span><span class="sxs-lookup"><span data-stu-id="f0c98-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f0c98-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0c98-109">DESCRIPTION</span></span>
<span data-ttu-id="f0c98-110">Получение или перечисление хранилищ конфигураций приложений.</span><span class="sxs-lookup"><span data-stu-id="f0c98-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="f0c98-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0c98-111">EXAMPLES</span></span>

### <span data-ttu-id="f0c98-112">Пример 1: список всех хранилищ конфигураций приложений в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="f0c98-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="f0c98-113">Эта команда перечисляет все хранилища конфигурации приложений в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="f0c98-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="f0c98-114">Пример 2: список всех хранилищ конфигурации приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0c98-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="f0c98-115">Эта команда перечисляет все хранилища конфигурации приложений в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0c98-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="f0c98-116">Пример 3: Получение хранилища конфигурации приложения по имени</span><span class="sxs-lookup"><span data-stu-id="f0c98-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="f0c98-117">Эта команда получает хранилище конфигурации приложения по имени.</span><span class="sxs-lookup"><span data-stu-id="f0c98-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="f0c98-118">Пример 4: Получение хранилища конфигурации приложений по каналу продаж</span><span class="sxs-lookup"><span data-stu-id="f0c98-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="f0c98-119">Эта команда возвращает хранилище конфигурации приложения по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="f0c98-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="f0c98-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0c98-120">PARAMETERS</span></span>

### <span data-ttu-id="f0c98-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c98-121">-DefaultProfile</span></span>
<span data-ttu-id="f0c98-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c98-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c98-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0c98-123">-InputObject</span></span>
<span data-ttu-id="f0c98-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="f0c98-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0c98-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0c98-125">-Name</span></span>
<span data-ttu-id="f0c98-126">Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="f0c98-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="f0c98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c98-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0c98-128">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="f0c98-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="f0c98-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0c98-129">-SubscriptionId</span></span>
<span data-ttu-id="f0c98-130">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c98-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="f0c98-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c98-131">CommonParameters</span></span>
<span data-ttu-id="f0c98-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0c98-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c98-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0c98-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c98-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0c98-134">INPUTS</span></span>

### <span data-ttu-id="f0c98-135">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="f0c98-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="f0c98-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0c98-136">OUTPUTS</span></span>

### <span data-ttu-id="f0c98-137">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="f0c98-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="f0c98-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0c98-138">NOTES</span></span>

<span data-ttu-id="f0c98-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="f0c98-139">ALIASES</span></span>

<span data-ttu-id="f0c98-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f0c98-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0c98-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f0c98-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0c98-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f0c98-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0c98-143">INPUTOBJECT <IAppConfigurationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="f0c98-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0c98-144">`[ConfigStoreName <String>]`: Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="f0c98-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="f0c98-145">`[GroupName <String>]`: Имя группы ресурсов частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="f0c98-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="f0c98-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="f0c98-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0c98-147">`[PrivateEndpointConnectionName <String>]`: Имя частного подключения конечной точки</span><span class="sxs-lookup"><span data-stu-id="f0c98-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="f0c98-148">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="f0c98-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="f0c98-149">`[SubscriptionId <String>]`: Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c98-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="f0c98-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0c98-150">RELATED LINKS</span></span>
