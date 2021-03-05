---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 7ea6f485026faa183f66d5bb2e70eb57c4a9fb97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006744"
---
# <span data-ttu-id="d8263-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d8263-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="d8263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8263-102">SYNOPSIS</span></span>
<span data-ttu-id="d8263-103">Обновляет приложение с функцией.</span><span class="sxs-lookup"><span data-stu-id="d8263-103">Updates a function app.</span></span>

## <span data-ttu-id="d8263-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8263-104">SYNTAX</span></span>

### <span data-ttu-id="d8263-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8263-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8263-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="d8263-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d8263-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8263-107">DESCRIPTION</span></span>
<span data-ttu-id="d8263-108">Обновляет приложение с функцией.</span><span class="sxs-lookup"><span data-stu-id="d8263-108">Updates a function app.</span></span>

## <span data-ttu-id="d8263-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8263-109">EXAMPLES</span></span>

### <span data-ttu-id="d8263-110">Пример 1. Обновление плана размещения приложений с функцией.</span><span class="sxs-lookup"><span data-stu-id="d8263-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="d8263-111">Эта команда обновляет план размещения приложений с функцией.</span><span class="sxs-lookup"><span data-stu-id="d8263-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="d8263-112">Пример 2. Настройка управляемого удостоверения SystemAssigned для приложения функций.</span><span class="sxs-lookup"><span data-stu-id="d8263-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="d8263-113">Эта команда задает управляемое удостоверение SystemAssigned для приложения функций.</span><span class="sxs-lookup"><span data-stu-id="d8263-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="d8263-114">Пример 3. Обновление функции приложения Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d8263-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="d8263-115">Эта команда обновляет функцию application Insights приложения.</span><span class="sxs-lookup"><span data-stu-id="d8263-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="d8263-116">Пример 3. Удаление управляемых удостоверений из приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="d8263-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="d8263-117">Эта команда удаляет управляемое удостоверение из приложения function.</span><span class="sxs-lookup"><span data-stu-id="d8263-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="d8263-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8263-118">PARAMETERS</span></span>

### <span data-ttu-id="d8263-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="d8263-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="d8263-120">Ключ инструментов для анализа приложений, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="d8263-120">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8263-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="d8263-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="d8263-122">Имя существующего проекта App Insights, который нужно добавить в приложение функций.</span><span class="sxs-lookup"><span data-stu-id="d8263-122">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8263-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8263-123">-AsJob</span></span>
<span data-ttu-id="d8263-124">Выполняется в качестве фонового задания.</span><span class="sxs-lookup"><span data-stu-id="d8263-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="d8263-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8263-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="d8263-126">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="d8263-126">-IdentityID</span></span>
<span data-ttu-id="d8263-127">Определяет список удостоверений пользователей, связанных с приложением функции.</span><span class="sxs-lookup"><span data-stu-id="d8263-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="d8263-128">Ссылки на удостоверения пользователей будут ARM ресурса в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="d8263-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="d8263-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d8263-129">-IdentityType</span></span>
<span data-ttu-id="d8263-130">Определяет тип удостоверения, используемого для приложения функции.</span><span class="sxs-lookup"><span data-stu-id="d8263-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="d8263-131">Тип "Нет" удаляет все удостоверения из приложения функции.</span><span class="sxs-lookup"><span data-stu-id="d8263-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="d8263-132">Допустимыми значениями для этого параметра являются: - SystemAssigned - UserAssigned - None</span><span class="sxs-lookup"><span data-stu-id="d8263-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8263-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8263-133">-InputObject</span></span>
<span data-ttu-id="d8263-134">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="d8263-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8263-135">-Name</span><span class="sxs-lookup"><span data-stu-id="d8263-135">-Name</span></span>
<span data-ttu-id="d8263-136">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="d8263-136">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8263-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8263-137">-NoWait</span></span>
<span data-ttu-id="d8263-138">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="d8263-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="d8263-139">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="d8263-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d8263-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d8263-140">-PlanName</span></span>
<span data-ttu-id="d8263-141">Название плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d8263-141">The name of the service plan.</span></span>

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

### <span data-ttu-id="d8263-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8263-142">-ResourceGroupName</span></span>
<span data-ttu-id="d8263-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8263-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8263-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8263-144">-SubscriptionId</span></span>
<span data-ttu-id="d8263-145">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d8263-145">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8263-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8263-146">-Tag</span></span>
<span data-ttu-id="d8263-147">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8263-147">Resource tags.</span></span>

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

### <span data-ttu-id="d8263-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8263-148">-Confirm</span></span>
<span data-ttu-id="d8263-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d8263-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8263-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8263-150">-WhatIf</span></span>
<span data-ttu-id="d8263-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8263-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8263-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d8263-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8263-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8263-153">CommonParameters</span></span>
<span data-ttu-id="d8263-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8263-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8263-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8263-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8263-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8263-156">INPUTS</span></span>

### <span data-ttu-id="d8263-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="d8263-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="d8263-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8263-158">OUTPUTS</span></span>

### <span data-ttu-id="d8263-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="d8263-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="d8263-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8263-160">NOTES</span></span>

<span data-ttu-id="d8263-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d8263-161">ALIASES</span></span>

<span data-ttu-id="d8263-162">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d8263-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8263-163">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d8263-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8263-164">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8263-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8263-165"><ISite>INPUTOBJECT:</span><span class="sxs-lookup"><span data-stu-id="d8263-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="d8263-166">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8263-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="d8263-167">`CloningInfoSourceWebAppId <String>`: ARM ресурса в приложении-источнике.</span><span class="sxs-lookup"><span data-stu-id="d8263-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="d8263-168">ИД ресурса приложения имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} для производственных слотов и /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} для других слотов.</span><span class="sxs-lookup"><span data-stu-id="d8263-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="d8263-169">`[Kind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8263-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="d8263-170">`[Tag <IResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8263-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d8263-171">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="d8263-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d8263-172">`[ClientAffinityEnabled <Boolean?>]`: включить клиентские сходства; прекратить отправку файлов cookie сеанса, которые будут отправлять запросы клиентов в том же сеансе <code>true</code> <code>false</code> в тот же экземпляр.</span><span class="sxs-lookup"><span data-stu-id="d8263-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="d8263-173">Значение по умолчанию <code>true</code> : .</span><span class="sxs-lookup"><span data-stu-id="d8263-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="d8263-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> чтобы включить проверку подлинности сертификата клиента (в общих проверках TLS); в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="d8263-175">Значение по умолчанию <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="d8263-176">`[ClientCertExclusionPath <String>]`: пути исключения, разделенные запятой для проверки подлинности сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="d8263-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="d8263-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: параметры приложений переопределяются для клонированных приложений.</span><span class="sxs-lookup"><span data-stu-id="d8263-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="d8263-178">При этом эти параметры переопределяют параметры, клонированные из приложения-источника.</span><span class="sxs-lookup"><span data-stu-id="d8263-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="d8263-179">В противном случае параметры приложения из источника сохраняются.</span><span class="sxs-lookup"><span data-stu-id="d8263-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="d8263-180">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="d8263-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d8263-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> чтобы клонировать пользовательские имена хостов из source app; в противном <code>false</code> случае.</span><span class="sxs-lookup"><span data-stu-id="d8263-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="d8263-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> чтобы клонировать управление исходным источником из source app; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="d8263-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> чтобы настроить балансировку нагрузки для приложения для назначения и источника.</span><span class="sxs-lookup"><span data-stu-id="d8263-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="d8263-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span><span class="sxs-lookup"><span data-stu-id="d8263-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="d8263-185">Этот ID связывает несколько операций клонирования, чтобы использовать один и тот же моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="d8263-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="d8263-186">`[CloningInfoHostingEnvironment <String>]`: Среда службы приложений.</span><span class="sxs-lookup"><span data-stu-id="d8263-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="d8263-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> чтобы переписать приложение; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="d8263-188">`[CloningInfoSourceWebAppLocation <String>]`: Расположение source app ex: West US or North Europe</span><span class="sxs-lookup"><span data-stu-id="d8263-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="d8263-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ресурса профиля Диспетчера трафика, если он существует.</span><span class="sxs-lookup"><span data-stu-id="d8263-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="d8263-190">Код ресурса Диспетчера трафика имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="d8263-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="d8263-191">`[CloningInfoTrafficManagerProfileName <String>]`: Имя профиля Диспетчера трафика, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="d8263-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="d8263-192">Это необходимо только в том случае, если профиль Диспетчера трафика еще не существует.</span><span class="sxs-lookup"><span data-stu-id="d8263-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="d8263-193">`[Config <ISiteConfig>]`: Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="d8263-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="d8263-194">`IsPushEnabled <Boolean>`: получает или устанавливает флажок, указывающий, включена ли конечная точка push-сигнала.</span><span class="sxs-lookup"><span data-stu-id="d8263-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="d8263-195">`[ActionMinProcessExecutionTime <String>]`: минимальное время, необходимое для выполнения процесса</span><span class="sxs-lookup"><span data-stu-id="d8263-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="d8263-196">`[ActionType <AutoHealActionType?>]`: Предопределированное действие.</span><span class="sxs-lookup"><span data-stu-id="d8263-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="d8263-197">`[AlwaysOn <Boolean?>]`: <code>true</code> если включена always on; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-198">`[ApiDefinitionUrl <String>]`URL-адрес определения API.</span><span class="sxs-lookup"><span data-stu-id="d8263-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="d8263-199">`[ApiManagementConfigId <String>]`: APIM-Api идентификатора.</span><span class="sxs-lookup"><span data-stu-id="d8263-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="d8263-200">`[AppCommandLine <String>]`: запуск командной строки приложения.</span><span class="sxs-lookup"><span data-stu-id="d8263-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="d8263-201">`[AppSetting <INameValuePair[]>]`: Параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="d8263-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="d8263-202">`[Name <String>]`: Парное имя.</span><span class="sxs-lookup"><span data-stu-id="d8263-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="d8263-203">`[Value <String>]`: Парный значение.</span><span class="sxs-lookup"><span data-stu-id="d8263-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="d8263-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> если автосъемка включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-205">`[AutoSwapSlotName <String>]`: название разъема для автоматического обмена.</span><span class="sxs-lookup"><span data-stu-id="d8263-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="d8263-206">`[ConnectionString <IConnStringInfo[]>]`: строки подключения.</span><span class="sxs-lookup"><span data-stu-id="d8263-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="d8263-207">`[ConnectionString <String>]`: строка подключения.</span><span class="sxs-lookup"><span data-stu-id="d8263-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="d8263-208">`[Name <String>]`: Имя строки подключения.</span><span class="sxs-lookup"><span data-stu-id="d8263-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="d8263-209">`[Type <ConnectionStringType?>]`: Тип базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8263-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="d8263-210">`[CorAllowedOrigin <String[]>]`: получает или задает список источников, которые должны быть разрешены для звонков в перекрестных источниках (например: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="d8263-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="d8263-211">Используйте "\*", чтобы разрешить все.</span><span class="sxs-lookup"><span data-stu-id="d8263-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="d8263-212">`[CorSupportCredentials <Boolean?>]`: получает или устанавливает, разрешено ли запросы CORS с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="d8263-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="d8263-213">Дополнительные         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="d8263-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="d8263-214">`[CustomActionExe <String>]`: исполняемый для выполнения.</span><span class="sxs-lookup"><span data-stu-id="d8263-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="d8263-215">`[CustomActionParameter <String>]`: Параметры исполняемого исполняемого параметров.</span><span class="sxs-lookup"><span data-stu-id="d8263-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="d8263-216">`[DefaultDocument <String[]>]`: Документы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8263-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="d8263-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> если включено подробное ведение журнала ошибок; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-218">`[DocumentRoot <String>]`: корневой документ.</span><span class="sxs-lookup"><span data-stu-id="d8263-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="d8263-219">`[DynamicTagsJson <String>]`: возвращает или задает строку JSON, содержащую список динамических тегов, которые будут вычисляться из утверждений пользователей на конечной точке push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="d8263-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="d8263-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: Список правил для работы с новыми бизнес-ами.</span><span class="sxs-lookup"><span data-stu-id="d8263-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="d8263-221">`[ActionHostName <String>]`: Hostname of a slot, to which the traffic will be redirected if decided to.</span><span class="sxs-lookup"><span data-stu-id="d8263-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="d8263-222">Например,</span><span class="sxs-lookup"><span data-stu-id="d8263-222">E.g.</span></span> <span data-ttu-id="d8263-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="d8263-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="d8263-224">`[ChangeDecisionCallbackUrl <String>]`В расширении сайта TiPCallback можно у указывается алгоритм пользовательских решений.</span><span class="sxs-lookup"><span data-stu-id="d8263-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="d8263-225">Подробнее о scaffold и контрактах см. в расширении сайта TiPCallback.</span><span class="sxs-lookup"><span data-stu-id="d8263-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="d8263-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="d8263-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="d8263-227">`[ChangeIntervalInMinute <Int32?>]`: определяет интервал в минутах для повторного проговаривания ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="d8263-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="d8263-228">`[ChangeStep <Double?>]`. В автоматическом сценарии обнуляйте эту возможность, пока не дойдете до <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> или         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="d8263-229">Метрики сайта проверяются каждые N минут, указанные в .\nCustom, алгоритм решения можно у регистрировать в расширении сайта TiPCallback, в котором можно укастить <code>ChangeIntervalInMinutes</code> <code>ChangeDecisionCallbackUrl</code> URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="d8263-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="d8263-230">`[MaxReroutePercentage <Double?>]`: указывает верхнюю границу, под которой будет находиться ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="d8263-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="d8263-231">`[MinReroutePercentage <Double?>]`: указывает нижнюю границу, над которой будет находиться ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="d8263-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="d8263-232">`[Name <String>]`: имя правила маршрутки.</span><span class="sxs-lookup"><span data-stu-id="d8263-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="d8263-233">Рекомендуется указать на слот, в котором будет приниматься трафик в эксперименте.</span><span class="sxs-lookup"><span data-stu-id="d8263-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="d8263-234">`[ReroutePercentage <Double?>]`: процент трафика, на который будет перенаправлен <code>ActionHostName</code> трафик.</span><span class="sxs-lookup"><span data-stu-id="d8263-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="d8263-235">`[FtpsState <FtpsState?>]`: состояние FTP или FTPS</span><span class="sxs-lookup"><span data-stu-id="d8263-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="d8263-236">`[HandlerMapping <IHandlerMapping[]>]`: Сопоставления обработера.</span><span class="sxs-lookup"><span data-stu-id="d8263-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="d8263-237">`[Argument <String>]`: аргументы командной строки, которые передаются в процессор сценариев.</span><span class="sxs-lookup"><span data-stu-id="d8263-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="d8263-238">`[Extension <String>]`: Запросы с этим расширением обрабатываются с помощью указанного приложения FastCGI.</span><span class="sxs-lookup"><span data-stu-id="d8263-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="d8263-239">`[ScriptProcessor <String>]`: абсолютный путь к приложению FastCGI.</span><span class="sxs-lookup"><span data-stu-id="d8263-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="d8263-240">`[HealthCheckPath <String>]`: путь проверки здоровья</span><span class="sxs-lookup"><span data-stu-id="d8263-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="d8263-241">`[Http20Enabled <Boolean?>]`Http20Enabled: настройка веб-сайта для разрешения клиентам подключения через http2.0</span><span class="sxs-lookup"><span data-stu-id="d8263-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="d8263-242">`[HttpLoggingEnabled <Boolean?>]`: если включено ведение журнала <code>true</code> HTTP; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP для основного.</span><span class="sxs-lookup"><span data-stu-id="d8263-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="d8263-244">`[Action <String>]`. Разрешить или запретить доступ для этого диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d8263-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="d8263-245">`[Description <String>]`: Описание правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="d8263-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="d8263-246">`[IPAddress <String>]`: IP-адрес, на который действует ограничение безопасности.</span><span class="sxs-lookup"><span data-stu-id="d8263-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="d8263-247">Оно может быть в чистом ipv4-адресе (обязательном свойстве SubnetMask) или нотации CIDR, например ipv4/mask (совпадение с ведущим битом).</span><span class="sxs-lookup"><span data-stu-id="d8263-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="d8263-248">Для CIDR свойство SubnetMask не должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="d8263-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="d8263-249">`[Name <String>]`: имя правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="d8263-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="d8263-250">`[Priority <Int32?>]`: Приоритет правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="d8263-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="d8263-251">`[SubnetMask <String>]`: Маска подсети для диапазона IP-адресов, на которые действует ограничение.</span><span class="sxs-lookup"><span data-stu-id="d8263-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="d8263-252">`[SubnetTrafficTag <Int32?>]`: (внутренний) тег трафика подсети</span><span class="sxs-lookup"><span data-stu-id="d8263-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="d8263-253">`[Tag <IPFilterTag?>]`: определяет, для чего будет использоваться этот ФИЛЬТР IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d8263-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="d8263-254">Это необходимо для поддержки фильтрации IP-адресов на прокси-прокси.</span><span class="sxs-lookup"><span data-stu-id="d8263-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="d8263-255">`[VnetSubnetResourceId <String>]`: ИД виртуального сетевого ресурса</span><span class="sxs-lookup"><span data-stu-id="d8263-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="d8263-256">`[VnetTrafficTag <Int32?>]`: (внутренний) тег трафика Vnet</span><span class="sxs-lookup"><span data-stu-id="d8263-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="d8263-257">`[JavaContainer <String>]`: контейнер Java.</span><span class="sxs-lookup"><span data-stu-id="d8263-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="d8263-258">`[JavaContainerVersion <String>]`: Версия контейнера Java.</span><span class="sxs-lookup"><span data-stu-id="d8263-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="d8263-259">`[JavaVersion <String>]`: Версия Java.</span><span class="sxs-lookup"><span data-stu-id="d8263-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="d8263-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Максимальный допустимый размер диска в МБ.</span><span class="sxs-lookup"><span data-stu-id="d8263-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="d8263-261">`[LimitMaxMemoryInMb <Int64?>]`: Максимальное разрешено использование памяти в МБ.</span><span class="sxs-lookup"><span data-stu-id="d8263-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="d8263-262">`[LimitMaxPercentageCpu <Double?>]`: Процент использования ЦП (максимально допустимый).</span><span class="sxs-lookup"><span data-stu-id="d8263-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="d8263-263">`[LinuxFxVersion <String>]`: Linux App Framework и версия</span><span class="sxs-lookup"><span data-stu-id="d8263-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="d8263-264">`[LoadBalancing <SiteLoadBalancing?>]`: Балансировка нагрузки сайта.</span><span class="sxs-lookup"><span data-stu-id="d8263-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="d8263-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> чтобы включить локальный MySQL; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-266">`[LogsDirectorySizeLimit <Int32?>]`: ограничение размера каталога http-журналов.</span><span class="sxs-lookup"><span data-stu-id="d8263-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="d8263-267">`[MachineKeyDecryption <String>]`: алгоритм, используемый для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="d8263-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="d8263-268">`[MachineKeyDecryptionKey <String>]`: ключ расшифровки.</span><span class="sxs-lookup"><span data-stu-id="d8263-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="d8263-269">`[MachineKeyValidation <String>]`: Проверка MachineKey.</span><span class="sxs-lookup"><span data-stu-id="d8263-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="d8263-270">`[MachineKeyValidationKey <String>]`: Ключ проверки.</span><span class="sxs-lookup"><span data-stu-id="d8263-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="d8263-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Управляемый режим конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8263-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="d8263-272">`[ManagedServiceIdentityId <Int32?>]`: Идентификатор управляемой службы</span><span class="sxs-lookup"><span data-stu-id="d8263-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="d8263-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: настройка минимальной версии TLS, необходимой для SSL-запросов</span><span class="sxs-lookup"><span data-stu-id="d8263-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="d8263-274">`[NetFrameworkVersion <String>]`: платформа .NET Framework версия.</span><span class="sxs-lookup"><span data-stu-id="d8263-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="d8263-275">`[NodeVersion <String>]`: Версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="d8263-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="d8263-276">`[NumberOfWorker <Int32?>]`: Количество сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d8263-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="d8263-277">`[PhpVersion <String>]`: Версия PHP.</span><span class="sxs-lookup"><span data-stu-id="d8263-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="d8263-278">`[PowerShellVersion <String>]`: версия PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d8263-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="d8263-279">`[PreWarmedInstanceCount <Int32?>]`: Количество предварительно заранее</span><span class="sxs-lookup"><span data-stu-id="d8263-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="d8263-280">Этот параметр применяется только к планам потребления и эластичности.</span><span class="sxs-lookup"><span data-stu-id="d8263-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="d8263-281">`[PublishingUsername <String>]`: имя пользователя публикации.</span><span class="sxs-lookup"><span data-stu-id="d8263-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="d8263-282">`[PushKind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8263-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="d8263-283">`[PythonVersion <String>]`: Version of Python.</span><span class="sxs-lookup"><span data-stu-id="d8263-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="d8263-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> если включена удаленная отладка; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-285">`[RemoteDebuggingVersion <String>]`: Версия удаленного отладки.</span><span class="sxs-lookup"><span data-stu-id="d8263-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="d8263-286">`[RequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="d8263-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="d8263-287">`[RequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="d8263-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="d8263-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> если включена трассировка запроса; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-289">`[RequestTracingExpirationTime <DateTime?>]`: запрос на трассировку срока действия.</span><span class="sxs-lookup"><span data-stu-id="d8263-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="d8263-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP-адресов для SCM.</span><span class="sxs-lookup"><span data-stu-id="d8263-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="d8263-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ограничения безопасности IP-адресов для использования основного.</span><span class="sxs-lookup"><span data-stu-id="d8263-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="d8263-292">`[ScmType <ScmType?>]`: тип SCM.</span><span class="sxs-lookup"><span data-stu-id="d8263-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="d8263-293">`[SlowRequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="d8263-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="d8263-294">`[SlowRequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="d8263-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="d8263-295">`[SlowRequestTimeTaken <String>]`: за взятое время.</span><span class="sxs-lookup"><span data-stu-id="d8263-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="d8263-296">`[TagWhitelistJson <String>]`: возвращает или задает строку JSON, содержащую список тегов, которые будут исключены в белый список для использования конечной точкой push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="d8263-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="d8263-297">`[TagsRequiringAuth <String>]`: возвращает или задает строку JSON, содержащую список тегов, для которых требуется проверка подлинности пользователя в конечной точке push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="d8263-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="d8263-298">Теги могут состоять из букв и цифр и следующих знаков: '_', '@', '#', '.', ':', '-'</span><span class="sxs-lookup"><span data-stu-id="d8263-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="d8263-299">Проверка должна выполняться в pushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="d8263-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="d8263-300">`[TracingOption <String>]`: Параметры трасситуры.</span><span class="sxs-lookup"><span data-stu-id="d8263-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="d8263-301">`[TriggerPrivateBytesInKb <Int32?>]`: правило, основанное на закрытыхбайтах.</span><span class="sxs-lookup"><span data-stu-id="d8263-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="d8263-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: правило, основанное на кодах состояния.</span><span class="sxs-lookup"><span data-stu-id="d8263-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="d8263-303">`[Count <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="d8263-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="d8263-304">`[Status <Int32?>]`: код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="d8263-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="d8263-305">`[SubStatus <Int32?>]`: Запросить состояние подгруппы.</span><span class="sxs-lookup"><span data-stu-id="d8263-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="d8263-306">`[TimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="d8263-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="d8263-307">`[Win32Status <Int32?>]`: код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="d8263-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="d8263-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> использовать процесс 32-битных сотрудников; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-309">`[VirtualApplication <IVirtualApplication[]>]`: Виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="d8263-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="d8263-310">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="d8263-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="d8263-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> если включена предварительная загрузка; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="d8263-312">`[VirtualDirectory <IVirtualDirectory[]>]`: виртуальные каталоги для виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="d8263-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="d8263-313">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="d8263-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="d8263-314">`[VirtualPath <String>]`: Путь к виртуальному приложению.</span><span class="sxs-lookup"><span data-stu-id="d8263-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="d8263-315">`[VirtualPath <String>]`: Виртуальный путь.</span><span class="sxs-lookup"><span data-stu-id="d8263-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="d8263-316">`[VnetName <String>]`: Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d8263-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="d8263-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> если webSocket включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="d8263-318">`[WindowsFxVersion <String>]`: Xenon App Framework и версия</span><span class="sxs-lookup"><span data-stu-id="d8263-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="d8263-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span><span class="sxs-lookup"><span data-stu-id="d8263-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="d8263-320">`[ContainerSize <Int32?>]`: Размер контейнера функции.</span><span class="sxs-lookup"><span data-stu-id="d8263-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="d8263-321">`[DailyMemoryTimeQuota <Int32?>]`: Максимальная квота суточного времени памяти (применима только для динамических приложений).</span><span class="sxs-lookup"><span data-stu-id="d8263-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="d8263-322">`[Enabled <Boolean?>]`: <code>true</code> если приложение включено; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="d8263-323">Если установить для этого значения значение false, приложение отключается (переключает его в автономный режим).</span><span class="sxs-lookup"><span data-stu-id="d8263-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="d8263-324">`[HostNameSslState <IHostNameSslState[]>]`: Состояния SSL hostname используются для управления привязками SSL для имен хостов приложения.</span><span class="sxs-lookup"><span data-stu-id="d8263-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="d8263-325">`[HostType <HostType?>]`: указывает, является ли имя хранилищ стандартным или репозиторием.</span><span class="sxs-lookup"><span data-stu-id="d8263-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="d8263-326">`[Name <String>]`: Hostname ..</span><span class="sxs-lookup"><span data-stu-id="d8263-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="d8263-327">`[SslState <SslState?>]`: Тип SSL.</span><span class="sxs-lookup"><span data-stu-id="d8263-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="d8263-328">`[Thumbprint <String>]`: Эскиз SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="d8263-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="d8263-329">`[ToUpdate <Boolean?>]`: Установите этот <code>true</code> код для обновления существующего имени.</span><span class="sxs-lookup"><span data-stu-id="d8263-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="d8263-330">`[VirtualIP <String>]`: Виртуальный IP-адрес, присвоенный имени хоста, если включен SSL на основе IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d8263-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="d8263-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> чтобы отключить общедоступные имена хостов приложения; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="d8263-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="d8263-332">Если приложение доступно только в процессе управления <code>true</code> API.</span><span class="sxs-lookup"><span data-stu-id="d8263-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="d8263-333">`[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="d8263-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="d8263-334">`[HttpsOnly <Boolean?>]`HttpsOnly: настройка веб-сайта для прием только http-запросов.</span><span class="sxs-lookup"><span data-stu-id="d8263-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="d8263-335">Перенаправление вопросов по http-запросам</span><span class="sxs-lookup"><span data-stu-id="d8263-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="d8263-336">`[HyperV <Boolean?>]`: Hyper-V песочницу.</span><span class="sxs-lookup"><span data-stu-id="d8263-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="d8263-337">`[IdentityType <ManagedServiceIdentityType?>]`: Тип управляемого удостоверения службы.</span><span class="sxs-lookup"><span data-stu-id="d8263-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="d8263-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: список удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="d8263-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="d8263-339">Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторы ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="d8263-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="d8263-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="d8263-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d8263-341">`[IsXenon <Boolean?>]`: Устарело: Hyper-V песочнице.</span><span class="sxs-lookup"><span data-stu-id="d8263-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="d8263-342">`[RedundancyMode <RedundancyMode?>]`: режим избыточности сайта</span><span class="sxs-lookup"><span data-stu-id="d8263-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="d8263-343">`[Reserved <Boolean?>]`: <code>true</code> если зарезервирован; в противном <code>false</code> случае.</span><span class="sxs-lookup"><span data-stu-id="d8263-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="d8263-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> чтобы остановить сайт SCM (KUDU), когда приложение остановлено; в противном <code>false</code> случае.</span><span class="sxs-lookup"><span data-stu-id="d8263-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="d8263-345">Значение по <code>false</code> умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="d8263-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="d8263-346">`[ServerFarmId <String>]`: Код ресурса связанного плана службы приложения в формате "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="d8263-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="d8263-347">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8263-347">RELATED LINKS</span></span>

