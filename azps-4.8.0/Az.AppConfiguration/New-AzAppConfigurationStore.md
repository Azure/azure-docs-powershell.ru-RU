---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243735"
---
# <span data-ttu-id="3b86a-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="3b86a-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="3b86a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b86a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b86a-103">Создает хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="3b86a-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="3b86a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b86a-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3b86a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b86a-105">DESCRIPTION</span></span>
<span data-ttu-id="3b86a-106">Создает хранилище конфигураций с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="3b86a-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="3b86a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b86a-107">EXAMPLES</span></span>

### <span data-ttu-id="3b86a-108">Пример 1: создание хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="3b86a-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3b86a-109">Эта команда создает хранилище конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="3b86a-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="3b86a-110">Пример 2: создание конфигурации приложения с IdentityType, установленным на "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="3b86a-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3b86a-111">Эта команда создает конфигурацию приложения и присваивает ей назначенный пользователю управляемый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3b86a-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="3b86a-112">`Update-AzAppConfigurationStore`Ниже описаны действия, которые необходимо выполнить, чтобы включить CMK (управляемый ключ cusomer).</span><span class="sxs-lookup"><span data-stu-id="3b86a-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="3b86a-113">Пример 3: создание конфигурации приложения с IdentityType, установленным на "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="3b86a-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3b86a-114">Эта команда создает конфигурацию приложения и включает управляемое системой удостоверение, связанное с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="3b86a-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="3b86a-115">`Update-AzAppConfigurationStore`Ниже описаны действия, которые необходимо выполнить, чтобы включить CMK (управляемый ключ cusomer).</span><span class="sxs-lookup"><span data-stu-id="3b86a-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="3b86a-116">Пример 4: создание конфигурации приложения с IdentityType, установленным на "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="3b86a-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3b86a-117">Вы можете включить управляемую системой идентификационную идентификацию и одновременно предоставить пользователям Идентификационные удостоверения.</span><span class="sxs-lookup"><span data-stu-id="3b86a-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="3b86a-118">`Update-AzAppConfigurationStore`Ниже описаны действия, которые необходимо выполнить, чтобы включить CMK (управляемый ключ cusomer).</span><span class="sxs-lookup"><span data-stu-id="3b86a-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="3b86a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b86a-119">PARAMETERS</span></span>

### <span data-ttu-id="3b86a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b86a-120">-AsJob</span></span>
<span data-ttu-id="3b86a-121">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3b86a-121">Run the command as a job</span></span>

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

### <span data-ttu-id="3b86a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b86a-122">-DefaultProfile</span></span>
<span data-ttu-id="3b86a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b86a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b86a-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3b86a-124">-IdentityType</span></span>
<span data-ttu-id="3b86a-125">Тип используемого управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="3b86a-125">The type of managed identity used.</span></span>
<span data-ttu-id="3b86a-126">Тип "SystemAssignedAndUserAssigned" включает в себя как неявно созданную идентификацию, так и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="3b86a-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="3b86a-127">Тип "нет" приведет к удалению всех удостоверений.</span><span class="sxs-lookup"><span data-stu-id="3b86a-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="3b86a-128">-Location</span><span class="sxs-lookup"><span data-stu-id="3b86a-128">-Location</span></span>
<span data-ttu-id="3b86a-129">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b86a-129">The location of the resource.</span></span>
<span data-ttu-id="3b86a-130">После создания ресурса изменить его нельзя.</span><span class="sxs-lookup"><span data-stu-id="3b86a-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="3b86a-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b86a-131">-Name</span></span>
<span data-ttu-id="3b86a-132">Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="3b86a-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="3b86a-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="3b86a-133">-NoWait</span></span>
<span data-ttu-id="3b86a-134">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3b86a-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b86a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b86a-135">-ResourceGroupName</span></span>
<span data-ttu-id="3b86a-136">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="3b86a-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="3b86a-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="3b86a-137">-Sku</span></span>
<span data-ttu-id="3b86a-138">Имя SKU хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="3b86a-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="3b86a-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b86a-139">-SubscriptionId</span></span>
<span data-ttu-id="3b86a-140">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b86a-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="3b86a-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="3b86a-141">-Tag</span></span>
<span data-ttu-id="3b86a-142">Теги ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b86a-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="3b86a-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3b86a-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="3b86a-144">Список назначенных пользователю удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="3b86a-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="3b86a-145">Назначенные пользователем ключи словаря идентификаторов будут представлять собой идентификаторы ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="3b86a-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="3b86a-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b86a-146">-Confirm</span></span>
<span data-ttu-id="3b86a-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b86a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b86a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b86a-148">-WhatIf</span></span>
<span data-ttu-id="3b86a-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b86a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b86a-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b86a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b86a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b86a-151">CommonParameters</span></span>
<span data-ttu-id="3b86a-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b86a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b86a-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b86a-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b86a-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b86a-154">INPUTS</span></span>

## <span data-ttu-id="3b86a-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b86a-155">OUTPUTS</span></span>

### <span data-ttu-id="3b86a-156">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="3b86a-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="3b86a-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b86a-157">NOTES</span></span>

<span data-ttu-id="3b86a-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3b86a-158">ALIASES</span></span>

## <span data-ttu-id="3b86a-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b86a-159">RELATED LINKS</span></span>



[<span data-ttu-id="3b86a-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3b86a-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

