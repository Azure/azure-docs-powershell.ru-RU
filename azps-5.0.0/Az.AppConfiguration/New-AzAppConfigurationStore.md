---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246449"
---
# <span data-ttu-id="cbdb0-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="cbdb0-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="cbdb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbdb0-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdb0-103">Создает хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="cbdb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbdb0-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cbdb0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbdb0-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdb0-106">Создает хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="cbdb0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbdb0-107">EXAMPLES</span></span>

### <span data-ttu-id="cbdb0-108">Пример 1: создание хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="cbdb0-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="cbdb0-109">Эта команда создает хранилище конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="cbdb0-110">Пример 2: создание конфигурации приложения с IdentityType, установленным на "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="cbdb0-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="cbdb0-111">Эта команда создает конфигурацию приложения и присваивает ей назначенный пользователю управляемый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="cbdb0-112">`Update-AzAppConfigurationStore`Ниже описаны действия, которые необходимо выполнить, чтобы включить CMK (управляемый ключ cusomer).</span><span class="sxs-lookup"><span data-stu-id="cbdb0-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="cbdb0-113">Пример 3: создание конфигурации приложения с IdentityType, установленным на "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="cbdb0-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="cbdb0-114">Эта команда создает конфигурацию приложения и включает управляемое системой удостоверение, связанное с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="cbdb0-115">`Update-AzAppConfigurationStore`Ниже описаны действия, которые необходимо выполнить, чтобы включить CMK (управляемый ключ cusomer).</span><span class="sxs-lookup"><span data-stu-id="cbdb0-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="cbdb0-116">Пример 4: создание конфигурации приложения с IdentityType, установленным на "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="cbdb0-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="cbdb0-117">Вы можете включить управляемую системой идентификационную идентификацию и одновременно предоставить пользователям Идентификационные удостоверения.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="cbdb0-118">`Update-AzAppConfigurationStore`Ниже описаны действия, которые необходимо выполнить, чтобы включить CMK (управляемый ключ cusomer).</span><span class="sxs-lookup"><span data-stu-id="cbdb0-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="cbdb0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbdb0-119">PARAMETERS</span></span>

### <span data-ttu-id="cbdb0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbdb0-120">-AsJob</span></span>
<span data-ttu-id="cbdb0-121">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="cbdb0-121">Run the command as a job</span></span>

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

### <span data-ttu-id="cbdb0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdb0-122">-DefaultProfile</span></span>
<span data-ttu-id="cbdb0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdb0-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cbdb0-124">-IdentityType</span></span>
<span data-ttu-id="cbdb0-125">Тип используемого управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-125">The type of managed identity used.</span></span>
<span data-ttu-id="cbdb0-126">Тип "SystemAssignedAndUserAssigned" включает в себя как неявно созданную идентификацию, так и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="cbdb0-127">Тип "нет" приведет к удалению всех удостоверений.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="cbdb0-128">-Location</span><span class="sxs-lookup"><span data-stu-id="cbdb0-128">-Location</span></span>
<span data-ttu-id="cbdb0-129">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-129">The location of the resource.</span></span>
<span data-ttu-id="cbdb0-130">После создания ресурса изменить его нельзя.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="cbdb0-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbdb0-131">-Name</span></span>
<span data-ttu-id="cbdb0-132">Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="cbdb0-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="cbdb0-133">-NoWait</span></span>
<span data-ttu-id="cbdb0-134">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="cbdb0-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cbdb0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdb0-135">-ResourceGroupName</span></span>
<span data-ttu-id="cbdb0-136">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="cbdb0-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="cbdb0-137">-Sku</span></span>
<span data-ttu-id="cbdb0-138">Имя SKU хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="cbdb0-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbdb0-139">-SubscriptionId</span></span>
<span data-ttu-id="cbdb0-140">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="cbdb0-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="cbdb0-141">-Tag</span></span>
<span data-ttu-id="cbdb0-142">Теги ресурса.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="cbdb0-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cbdb0-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="cbdb0-144">Список назначенных пользователю удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="cbdb0-145">Назначенные пользователем ключи словаря идентификаторов будут представлять собой идентификаторы ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="cbdb0-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="cbdb0-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbdb0-146">-Confirm</span></span>
<span data-ttu-id="cbdb0-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdb0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdb0-148">-WhatIf</span></span>
<span data-ttu-id="cbdb0-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbdb0-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdb0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdb0-151">CommonParameters</span></span>
<span data-ttu-id="cbdb0-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbdb0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdb0-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbdb0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdb0-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbdb0-154">INPUTS</span></span>

## <span data-ttu-id="cbdb0-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbdb0-155">OUTPUTS</span></span>

### <span data-ttu-id="cbdb0-156">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="cbdb0-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="cbdb0-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbdb0-157">NOTES</span></span>

<span data-ttu-id="cbdb0-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cbdb0-158">ALIASES</span></span>

## <span data-ttu-id="cbdb0-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbdb0-159">RELATED LINKS</span></span>



[<span data-ttu-id="cbdb0-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cbdb0-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)
