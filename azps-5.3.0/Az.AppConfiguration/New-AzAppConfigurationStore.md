---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423055"
---
# <span data-ttu-id="9e815-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="9e815-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="9e815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e815-102">SYNOPSIS</span></span>
<span data-ttu-id="9e815-103">Создает хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="9e815-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="9e815-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e815-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9e815-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e815-105">DESCRIPTION</span></span>
<span data-ttu-id="9e815-106">Создает хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="9e815-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="9e815-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e815-107">EXAMPLES</span></span>

### <span data-ttu-id="9e815-108">Пример 1. Создание магазина конфигурации приложений</span><span class="sxs-lookup"><span data-stu-id="9e815-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9e815-109">Эта команда создает магазин конфигурации приложений.</span><span class="sxs-lookup"><span data-stu-id="9e815-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="9e815-110">Пример 2. Создание конфигурации приложения с идентификатором IdentityType "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="9e815-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9e815-111">Эта команда создает конфигурацию приложения и назначает ей управляемое удостоверение, назначенное пользователем.</span><span class="sxs-lookup"><span data-stu-id="9e815-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="9e815-112">Ниже приводится пример для того, чтобы включить `Update-AzAppConfigurationStore` CMK (утомительный управляемый ключ).</span><span class="sxs-lookup"><span data-stu-id="9e815-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="9e815-113">Пример 3. Создание конфигурации приложения с типом IdentityType "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="9e815-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9e815-114">Эта команда создает конфигурацию приложения и позволяет управлять удостоверением, связанным с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="9e815-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="9e815-115">Ниже приводится пример для того, чтобы включить `Update-AzAppConfigurationStore` CMK (утомительный управляемый ключ).</span><span class="sxs-lookup"><span data-stu-id="9e815-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="9e815-116">Пример 4. Создание конфигурации приложения с типом IdentityType "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="9e815-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9e815-117">Вы можете включить управляемые удостоверения, которым назначены системы, и одновременно предоставить удостоверения, которые назначены пользователям.</span><span class="sxs-lookup"><span data-stu-id="9e815-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="9e815-118">Ниже приводится пример для того, чтобы включить `Update-AzAppConfigurationStore` CMK (утомительный управляемый ключ).</span><span class="sxs-lookup"><span data-stu-id="9e815-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="9e815-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e815-119">PARAMETERS</span></span>

### <span data-ttu-id="9e815-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e815-120">-AsJob</span></span>
<span data-ttu-id="9e815-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9e815-121">Run the command as a job</span></span>

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

### <span data-ttu-id="9e815-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e815-122">-DefaultProfile</span></span>
<span data-ttu-id="9e815-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e815-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e815-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9e815-124">-IdentityType</span></span>
<span data-ttu-id="9e815-125">Тип используемых управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9e815-125">The type of managed identity used.</span></span>
<span data-ttu-id="9e815-126">Тип SystemAssignedAndUserAssigned включает неявно созданное удостоверение и набор удостоверений, которые назначены пользователю.</span><span class="sxs-lookup"><span data-stu-id="9e815-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="9e815-127">Тип "Нет" удалит все удостоверения.</span><span class="sxs-lookup"><span data-stu-id="9e815-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e815-128">-Location</span><span class="sxs-lookup"><span data-stu-id="9e815-128">-Location</span></span>
<span data-ttu-id="9e815-129">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e815-129">The location of the resource.</span></span>
<span data-ttu-id="9e815-130">Это невозможно изменить после создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e815-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="9e815-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9e815-131">-Name</span></span>
<span data-ttu-id="9e815-132">Имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9e815-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="9e815-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9e815-133">-NoWait</span></span>
<span data-ttu-id="9e815-134">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9e815-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9e815-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e815-135">-ResourceGroupName</span></span>
<span data-ttu-id="9e815-136">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e815-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="9e815-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e815-137">-Sku</span></span>
<span data-ttu-id="9e815-138">Имя SKU магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9e815-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="9e815-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e815-139">-SubscriptionId</span></span>
<span data-ttu-id="9e815-140">ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e815-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="9e815-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e815-141">-Tag</span></span>
<span data-ttu-id="9e815-142">Теги ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e815-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="9e815-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9e815-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="9e815-144">Список удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="9e815-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="9e815-145">В качестве ключей словарей для пользовательских удостоверений будут ARM идентификаторы ресурсов в форме :'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="9e815-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e815-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e815-146">-Confirm</span></span>
<span data-ttu-id="9e815-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e815-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e815-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e815-148">-WhatIf</span></span>
<span data-ttu-id="9e815-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e815-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e815-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9e815-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e815-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e815-151">CommonParameters</span></span>
<span data-ttu-id="9e815-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e815-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e815-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e815-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e815-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e815-154">INPUTS</span></span>

## <span data-ttu-id="9e815-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e815-155">OUTPUTS</span></span>

### <span data-ttu-id="9e815-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="9e815-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="9e815-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e815-157">NOTES</span></span>

<span data-ttu-id="9e815-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9e815-158">ALIASES</span></span>

## <span data-ttu-id="9e815-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e815-159">RELATED LINKS</span></span>



[<span data-ttu-id="9e815-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9e815-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

