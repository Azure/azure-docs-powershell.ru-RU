---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504852"
---
# <span data-ttu-id="82301-101">Remove-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="82301-101">Remove-AzFunctionAppSetting</span></span>

## <span data-ttu-id="82301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82301-102">SYNOPSIS</span></span>
<span data-ttu-id="82301-103">Удаляет параметры приложения из приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="82301-103">Removes app settings from a function app.</span></span>

## <span data-ttu-id="82301-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82301-104">SYNTAX</span></span>

### <span data-ttu-id="82301-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82301-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="82301-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="82301-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82301-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82301-107">DESCRIPTION</span></span>
<span data-ttu-id="82301-108">Удаляет параметры приложения из приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="82301-108">Removes app settings from a function app.</span></span>

## <span data-ttu-id="82301-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82301-109">EXAMPLES</span></span>

### <span data-ttu-id="82301-110">Пример 1. Удаление параметров приложения в приложении с функцией.</span><span class="sxs-lookup"><span data-stu-id="82301-110">Example 1: Remove app settings in a function app.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

<span data-ttu-id="82301-111">Эта команда удаляет параметры приложения в приложении с функцией.</span><span class="sxs-lookup"><span data-stu-id="82301-111">This command removes app settings in a function app.</span></span>

## <span data-ttu-id="82301-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82301-112">PARAMETERS</span></span>

### <span data-ttu-id="82301-113">-AppSettingName</span><span class="sxs-lookup"><span data-stu-id="82301-113">-AppSettingName</span></span>
<span data-ttu-id="82301-114">Список параметров приложения функций, удаляемого из приложения этой функции.</span><span class="sxs-lookup"><span data-stu-id="82301-114">List of function app settings to be removed from the function app.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82301-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82301-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="82301-116">-Force</span><span class="sxs-lookup"><span data-stu-id="82301-116">-Force</span></span>
<span data-ttu-id="82301-117">Позволяет удалить параметр приложения функции, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="82301-117">Forces the cmdlet to remove function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="82301-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82301-118">-InputObject</span></span>
<span data-ttu-id="82301-119">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="82301-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="82301-120">-Name</span><span class="sxs-lookup"><span data-stu-id="82301-120">-Name</span></span>
<span data-ttu-id="82301-121">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="82301-121">Name of the function app.</span></span>

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

### <span data-ttu-id="82301-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82301-122">-ResourceGroupName</span></span>
<span data-ttu-id="82301-123">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="82301-123">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="82301-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82301-124">-SubscriptionId</span></span>
<span data-ttu-id="82301-125">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="82301-125">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="82301-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82301-126">-Confirm</span></span>
<span data-ttu-id="82301-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="82301-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82301-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82301-128">-WhatIf</span></span>
<span data-ttu-id="82301-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82301-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82301-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82301-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82301-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82301-131">CommonParameters</span></span>
<span data-ttu-id="82301-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82301-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82301-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82301-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82301-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82301-134">INPUTS</span></span>

### <span data-ttu-id="82301-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="82301-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="82301-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82301-136">OUTPUTS</span></span>

### <span data-ttu-id="82301-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="82301-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="82301-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82301-138">NOTES</span></span>

<span data-ttu-id="82301-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="82301-139">ALIASES</span></span>

<span data-ttu-id="82301-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="82301-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82301-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="82301-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82301-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="82301-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82301-143"><ISite>INPUTOBJECT:</span><span class="sxs-lookup"><span data-stu-id="82301-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="82301-144">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="82301-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="82301-145">`CloningInfoSourceWebAppId <String>`: ARM ресурса в приложении-источнике.</span><span class="sxs-lookup"><span data-stu-id="82301-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="82301-146">ИД ресурса приложения имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} для производственных слотов и /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} для других слотов.</span><span class="sxs-lookup"><span data-stu-id="82301-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="82301-147">`[Kind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="82301-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="82301-148">`[Tag <IResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82301-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="82301-149">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="82301-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="82301-150">`[ClientAffinityEnabled <Boolean?>]`: включить клиентские сходства; прекратить отправку файлов cookie сеанса, которые будут маршрутить запросы клиентов в том же сеансе <code>true</code> <code>false</code> в тот же экземпляр.</span><span class="sxs-lookup"><span data-stu-id="82301-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="82301-151">Значение по умолчанию <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="82301-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> чтобы включить проверку подлинности сертификата клиента (в общих проверках TLS); в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="82301-153">Значение по умолчанию <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="82301-154">`[ClientCertExclusionPath <String>]`: пути исключения, разделенные запятой для проверки подлинности сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="82301-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="82301-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: параметры приложений переопределяются для клонированных приложений.</span><span class="sxs-lookup"><span data-stu-id="82301-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="82301-156">Если задан этот параметр, эти параметры переопределяют параметры, клонированные из источника.</span><span class="sxs-lookup"><span data-stu-id="82301-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="82301-157">В противном случае параметры приложения из источника сохраняются.</span><span class="sxs-lookup"><span data-stu-id="82301-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="82301-158">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="82301-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="82301-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> для клонирования пользовательских имен хостов из приложения-источника; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82301-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> чтобы клонировать управление исходным источником из source app; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82301-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> чтобы настроить балансировку нагрузки для приложения для назначения и источника.</span><span class="sxs-lookup"><span data-stu-id="82301-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="82301-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span><span class="sxs-lookup"><span data-stu-id="82301-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="82301-163">Этот ID связывает несколько операций клонирования, чтобы использовать один и тот же моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="82301-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="82301-164">`[CloningInfoHostingEnvironment <String>]`: Среда службы приложений.</span><span class="sxs-lookup"><span data-stu-id="82301-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="82301-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> чтобы переписать приложение; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82301-166">`[CloningInfoSourceWebAppLocation <String>]`: Расположение source app ex: West US or North Europe</span><span class="sxs-lookup"><span data-stu-id="82301-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="82301-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ресурса профиля Диспетчера трафика, если он существует.</span><span class="sxs-lookup"><span data-stu-id="82301-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="82301-168">Код ресурса Диспетчера трафика имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="82301-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="82301-169">`[CloningInfoTrafficManagerProfileName <String>]`: Имя профиля Диспетчера трафика, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="82301-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="82301-170">Это необходимо только в том случае, если профиль Диспетчера трафика еще не существует.</span><span class="sxs-lookup"><span data-stu-id="82301-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="82301-171">`[Config <ISiteConfig>]`: Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="82301-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="82301-172">`IsPushEnabled <Boolean>`: получает или устанавливает флажок, указывающий, включена ли конечная точка push-сигнала.</span><span class="sxs-lookup"><span data-stu-id="82301-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="82301-173">`[ActionMinProcessExecutionTime <String>]`: минимальное время, необходимое для выполнения процесса</span><span class="sxs-lookup"><span data-stu-id="82301-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="82301-174">`[ActionType <AutoHealActionType?>]`: Предопределированное действие.</span><span class="sxs-lookup"><span data-stu-id="82301-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="82301-175">`[AlwaysOn <Boolean?>]`: <code>true</code> если включена always on; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-176">`[ApiDefinitionUrl <String>]`URL-адрес определения API.</span><span class="sxs-lookup"><span data-stu-id="82301-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="82301-177">`[ApiManagementConfigId <String>]`: APIM-Api идентификатора.</span><span class="sxs-lookup"><span data-stu-id="82301-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="82301-178">`[AppCommandLine <String>]`: запуск командной строки приложения.</span><span class="sxs-lookup"><span data-stu-id="82301-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="82301-179">`[AppSetting <INameValuePair[]>]`: Параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="82301-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="82301-180">`[Name <String>]`: Парное имя.</span><span class="sxs-lookup"><span data-stu-id="82301-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="82301-181">`[Value <String>]`: Парный значение.</span><span class="sxs-lookup"><span data-stu-id="82301-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="82301-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> если автосъемка включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-183">`[AutoSwapSlotName <String>]`: название разъема для автоматического обмена.</span><span class="sxs-lookup"><span data-stu-id="82301-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="82301-184">`[ConnectionString <IConnStringInfo[]>]`: строки подключения.</span><span class="sxs-lookup"><span data-stu-id="82301-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="82301-185">`[ConnectionString <String>]`: строка подключения.</span><span class="sxs-lookup"><span data-stu-id="82301-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="82301-186">`[Name <String>]`: Имя строки подключения.</span><span class="sxs-lookup"><span data-stu-id="82301-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="82301-187">`[Type <ConnectionStringType?>]`: Тип базы данных.</span><span class="sxs-lookup"><span data-stu-id="82301-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="82301-188">`[CorAllowedOrigin <String[]>]`: получает или задает список источников, которые должны быть разрешены для звонков в перекрестных источниках (например: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="82301-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="82301-189">Используйте "\*", чтобы разрешить все.</span><span class="sxs-lookup"><span data-stu-id="82301-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="82301-190">`[CorSupportCredentials <Boolean?>]`: получает или устанавливает, разрешено ли запросы CORS с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="82301-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="82301-191">Дополнительные         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="82301-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="82301-192">`[CustomActionExe <String>]`: исполняемый для выполнения.</span><span class="sxs-lookup"><span data-stu-id="82301-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="82301-193">`[CustomActionParameter <String>]`: Параметры исполняемого исполняемого параметров.</span><span class="sxs-lookup"><span data-stu-id="82301-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="82301-194">`[DefaultDocument <String[]>]`: Документы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82301-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="82301-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> если включено подробное ведение журнала ошибок; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-196">`[DocumentRoot <String>]`: корневой документ.</span><span class="sxs-lookup"><span data-stu-id="82301-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="82301-197">`[DynamicTagsJson <String>]`: возвращает или задает строку JSON, содержащую список динамических тегов, которые будут вычисляться из утверждений пользователей на конечной точке push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="82301-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="82301-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: список правил для работы с новыми бизнес-ами.</span><span class="sxs-lookup"><span data-stu-id="82301-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="82301-199">`[ActionHostName <String>]`: Hostname of a slot, to which the traffic will be redirected if decided to.</span><span class="sxs-lookup"><span data-stu-id="82301-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="82301-200">Например,</span><span class="sxs-lookup"><span data-stu-id="82301-200">E.g.</span></span> <span data-ttu-id="82301-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="82301-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="82301-202">`[ChangeDecisionCallbackUrl <String>]`В расширении сайта TiPCallback можно у указывается алгоритм пользовательских решений.</span><span class="sxs-lookup"><span data-stu-id="82301-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="82301-203">Подробнее о scaffold и контрактах см. в расширении сайта TiPCallback.</span><span class="sxs-lookup"><span data-stu-id="82301-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="82301-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="82301-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="82301-205">`[ChangeIntervalInMinute <Int32?>]`: определяет интервал в минутах для повторного проговаривания ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="82301-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="82301-206">`[ChangeStep <Double?>]`. В автоматическом сценарии обнуляйте эту возможность, пока не дойдете до <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> или         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="82301-207">Метрики сайта проверяются каждые N минут, указанные в .\nCustom, алгоритм решения можно у регистрировать в расширении сайта TiPCallback, в котором можно укастить <code>ChangeIntervalInMinutes</code> <code>ChangeDecisionCallbackUrl</code> URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="82301-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="82301-208">`[MaxReroutePercentage <Double?>]`: указывает верхнюю границу, под которой будет находиться ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="82301-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="82301-209">`[MinReroutePercentage <Double?>]`: указывает нижнюю границу, над которой будет находиться ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="82301-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="82301-210">`[Name <String>]`: имя правила маршрутки.</span><span class="sxs-lookup"><span data-stu-id="82301-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="82301-211">Рекомендуется указать на слот, в котором будет приниматься трафик в эксперименте.</span><span class="sxs-lookup"><span data-stu-id="82301-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="82301-212">`[ReroutePercentage <Double?>]`: процент трафика, на который будет перенаправлен <code>ActionHostName</code> трафик.</span><span class="sxs-lookup"><span data-stu-id="82301-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="82301-213">`[FtpsState <FtpsState?>]`: состояние FTP или FTPS</span><span class="sxs-lookup"><span data-stu-id="82301-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="82301-214">`[HandlerMapping <IHandlerMapping[]>]`: Сопоставления обработера.</span><span class="sxs-lookup"><span data-stu-id="82301-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="82301-215">`[Argument <String>]`: аргументы командной строки, которые передаются в процессор сценариев.</span><span class="sxs-lookup"><span data-stu-id="82301-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="82301-216">`[Extension <String>]`: Запросы с этим расширением обрабатываются с помощью указанного приложения FastCGI.</span><span class="sxs-lookup"><span data-stu-id="82301-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="82301-217">`[ScriptProcessor <String>]`— абсолютный путь к приложению FastCGI.</span><span class="sxs-lookup"><span data-stu-id="82301-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="82301-218">`[HealthCheckPath <String>]`: путь проверки здоровья</span><span class="sxs-lookup"><span data-stu-id="82301-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="82301-219">`[Http20Enabled <Boolean?>]`Http20Enabled: настройка веб-сайта для разрешения клиентам подключения через http2.0</span><span class="sxs-lookup"><span data-stu-id="82301-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="82301-220">`[HttpLoggingEnabled <Boolean?>]`: если включено ведение журнала <code>true</code> HTTP; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP для основного.</span><span class="sxs-lookup"><span data-stu-id="82301-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="82301-222">`[Action <String>]`. Разрешить или запретить доступ для этого диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="82301-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="82301-223">`[Description <String>]`: Описание правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="82301-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="82301-224">`[IPAddress <String>]`: IP-адрес, на который действует ограничение безопасности.</span><span class="sxs-lookup"><span data-stu-id="82301-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="82301-225">Оно может быть в виде чистого ipv4-адреса (обязательного свойства SubnetMask) или нотации CIDR, например ipv4/mask (совпадение с ведущим битом).</span><span class="sxs-lookup"><span data-stu-id="82301-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="82301-226">Для CIDR свойство SubnetMask не должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="82301-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="82301-227">`[Name <String>]`: имя правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="82301-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="82301-228">`[Priority <Int32?>]`: Приоритет правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="82301-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="82301-229">`[SubnetMask <String>]`: Маска подсети для диапазона IP-адресов, на которые действует ограничение.</span><span class="sxs-lookup"><span data-stu-id="82301-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="82301-230">`[SubnetTrafficTag <Int32?>]`: (внутренний) тег трафика подсети</span><span class="sxs-lookup"><span data-stu-id="82301-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="82301-231">`[Tag <IPFilterTag?>]`: определяет, для чего будет использоваться этот ФИЛЬТР IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="82301-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="82301-232">Это необходимо для поддержки фильтрации по IP-адресам на прокси-прокси.</span><span class="sxs-lookup"><span data-stu-id="82301-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="82301-233">`[VnetSubnetResourceId <String>]`: ИД виртуального сетевого ресурса</span><span class="sxs-lookup"><span data-stu-id="82301-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="82301-234">`[VnetTrafficTag <Int32?>]`: (внутренний) тег трафика Vnet</span><span class="sxs-lookup"><span data-stu-id="82301-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="82301-235">`[JavaContainer <String>]`: контейнер Java.</span><span class="sxs-lookup"><span data-stu-id="82301-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="82301-236">`[JavaContainerVersion <String>]`: Версия контейнера Java.</span><span class="sxs-lookup"><span data-stu-id="82301-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="82301-237">`[JavaVersion <String>]`: Версия Java.</span><span class="sxs-lookup"><span data-stu-id="82301-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="82301-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Максимальный допустимый размер диска в МБ.</span><span class="sxs-lookup"><span data-stu-id="82301-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="82301-239">`[LimitMaxMemoryInMb <Int64?>]`: Максимальное разрешено использование памяти в МБ.</span><span class="sxs-lookup"><span data-stu-id="82301-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="82301-240">`[LimitMaxPercentageCpu <Double?>]`: Процент использования ЦП (максимально допустимый).</span><span class="sxs-lookup"><span data-stu-id="82301-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="82301-241">`[LinuxFxVersion <String>]`: Linux App Framework и версия</span><span class="sxs-lookup"><span data-stu-id="82301-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="82301-242">`[LoadBalancing <SiteLoadBalancing?>]`: Балансировка нагрузки сайта.</span><span class="sxs-lookup"><span data-stu-id="82301-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="82301-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> чтобы включить локальный MySQL; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-244">`[LogsDirectorySizeLimit <Int32?>]`: ограничение размера каталога http-журналов.</span><span class="sxs-lookup"><span data-stu-id="82301-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="82301-245">`[MachineKeyDecryption <String>]`: алгоритм, используемый для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="82301-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="82301-246">`[MachineKeyDecryptionKey <String>]`: ключ расшифровки.</span><span class="sxs-lookup"><span data-stu-id="82301-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="82301-247">`[MachineKeyValidation <String>]`: Проверка MachineKey.</span><span class="sxs-lookup"><span data-stu-id="82301-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="82301-248">`[MachineKeyValidationKey <String>]`: Ключ проверки.</span><span class="sxs-lookup"><span data-stu-id="82301-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="82301-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Управляемый режим конвейера.</span><span class="sxs-lookup"><span data-stu-id="82301-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="82301-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span><span class="sxs-lookup"><span data-stu-id="82301-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="82301-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: настройка минимальной версии TLS, необходимой для SSL-запросов</span><span class="sxs-lookup"><span data-stu-id="82301-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="82301-252">`[NetFrameworkVersion <String>]`: версия .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="82301-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="82301-253">`[NodeVersion <String>]`: Версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="82301-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="82301-254">`[NumberOfWorker <Int32?>]`: Количество сотрудников.</span><span class="sxs-lookup"><span data-stu-id="82301-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="82301-255">`[PhpVersion <String>]`: Версия PHP.</span><span class="sxs-lookup"><span data-stu-id="82301-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="82301-256">`[PowerShellVersion <String>]`: версия PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82301-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="82301-257">`[PreWarmedInstanceCount <Int32?>]`: Количество предварительно заранее</span><span class="sxs-lookup"><span data-stu-id="82301-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="82301-258">Этот параметр применяется только к планам потребления и эластичности.</span><span class="sxs-lookup"><span data-stu-id="82301-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="82301-259">`[PublishingUsername <String>]`: имя пользователя публикации.</span><span class="sxs-lookup"><span data-stu-id="82301-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="82301-260">`[PushKind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="82301-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="82301-261">`[PythonVersion <String>]`: Version of Python.</span><span class="sxs-lookup"><span data-stu-id="82301-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="82301-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> если включена удаленная отладка; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-263">`[RemoteDebuggingVersion <String>]`: Версия удаленного отладки.</span><span class="sxs-lookup"><span data-stu-id="82301-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="82301-264">`[RequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="82301-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="82301-265">`[RequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="82301-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="82301-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> если включена трассировка запроса; в противном случае <code>false</code> — .</span><span class="sxs-lookup"><span data-stu-id="82301-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-267">`[RequestTracingExpirationTime <DateTime?>]`: запрос на трассировку срока действия.</span><span class="sxs-lookup"><span data-stu-id="82301-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="82301-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP-адресов для SCM.</span><span class="sxs-lookup"><span data-stu-id="82301-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="82301-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ограничения безопасности IP-адресов для использования основного.</span><span class="sxs-lookup"><span data-stu-id="82301-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="82301-270">`[ScmType <ScmType?>]`: тип SCM.</span><span class="sxs-lookup"><span data-stu-id="82301-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="82301-271">`[SlowRequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="82301-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="82301-272">`[SlowRequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="82301-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="82301-273">`[SlowRequestTimeTaken <String>]`: время, за взятое.</span><span class="sxs-lookup"><span data-stu-id="82301-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="82301-274">`[TagWhitelistJson <String>]`: возвращает или задает строку JSON, содержащую список тегов, которые будут исключены в белый список для использования конечной точкой push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="82301-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="82301-275">`[TagsRequiringAuth <String>]`: возвращает или задает строку JSON, содержащую список тегов, для которых требуется проверка подлинности пользователя в конечной точке push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="82301-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="82301-276">Теги могут состоять из букв и цифр и следующих знаков: '_', '@', '#', '.', ':', '-'</span><span class="sxs-lookup"><span data-stu-id="82301-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="82301-277">Проверка должна выполняться в pushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="82301-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="82301-278">`[TracingOption <String>]`: Параметры трасситуры.</span><span class="sxs-lookup"><span data-stu-id="82301-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="82301-279">`[TriggerPrivateBytesInKb <Int32?>]`: правило, основанное на закрытыхбайтах.</span><span class="sxs-lookup"><span data-stu-id="82301-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="82301-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: правило, основанное на кодах состояния.</span><span class="sxs-lookup"><span data-stu-id="82301-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="82301-281">`[Count <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="82301-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="82301-282">`[Status <Int32?>]`: код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="82301-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="82301-283">`[SubStatus <Int32?>]`: Запросить состояние подгруппы.</span><span class="sxs-lookup"><span data-stu-id="82301-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="82301-284">`[TimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="82301-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="82301-285">`[Win32Status <Int32?>]`: код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="82301-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="82301-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> использовать процесс 32-битных сотрудников; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-287">`[VirtualApplication <IVirtualApplication[]>]`: Виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="82301-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="82301-288">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="82301-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="82301-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> если включена предварительная загрузка; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="82301-290">`[VirtualDirectory <IVirtualDirectory[]>]`: виртуальные каталоги для виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="82301-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="82301-291">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="82301-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="82301-292">`[VirtualPath <String>]`: Путь к виртуальному приложению.</span><span class="sxs-lookup"><span data-stu-id="82301-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="82301-293">`[VirtualPath <String>]`: Виртуальный путь.</span><span class="sxs-lookup"><span data-stu-id="82301-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="82301-294">`[VnetName <String>]`: Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="82301-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="82301-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> если webSocket включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82301-296">`[WindowsFxVersion <String>]`: Xenon App Framework и версия</span><span class="sxs-lookup"><span data-stu-id="82301-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="82301-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span><span class="sxs-lookup"><span data-stu-id="82301-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="82301-298">`[ContainerSize <Int32?>]`: Размер контейнера функции.</span><span class="sxs-lookup"><span data-stu-id="82301-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="82301-299">`[DailyMemoryTimeQuota <Int32?>]`: Максимальная квота суточного времени памяти (применима только для динамических приложений).</span><span class="sxs-lookup"><span data-stu-id="82301-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="82301-300">`[Enabled <Boolean?>]`: <code>true</code> если приложение включено; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="82301-301">Если установить для этого значения значение false, приложение отключается (переключает его в автономный режим).</span><span class="sxs-lookup"><span data-stu-id="82301-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="82301-302">`[HostNameSslState <IHostNameSslState[]>]`: Состояния SSL hostname используются для управления привязками SSL для имен хостов приложения.</span><span class="sxs-lookup"><span data-stu-id="82301-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="82301-303">`[HostType <HostType?>]`: указывает, является ли имя хранилищ стандартным или репозиторием.</span><span class="sxs-lookup"><span data-stu-id="82301-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="82301-304">`[Name <String>]`: Hostname ..</span><span class="sxs-lookup"><span data-stu-id="82301-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="82301-305">`[SslState <SslState?>]`: Тип SSL.</span><span class="sxs-lookup"><span data-stu-id="82301-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="82301-306">`[Thumbprint <String>]`: Эскиз SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="82301-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="82301-307">`[ToUpdate <Boolean?>]`: Установите этот <code>true</code> код для обновления существующего имени.</span><span class="sxs-lookup"><span data-stu-id="82301-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="82301-308">`[VirtualIP <String>]`: Виртуальный IP-адрес, присвоенный имени хоста, если включен SSL на основе IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="82301-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="82301-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> чтобы отключить общедоступные имена хостов приложения; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82301-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="82301-310">Если приложение доступно только в процессе управления <code>true</code> API.</span><span class="sxs-lookup"><span data-stu-id="82301-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="82301-311">`[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="82301-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="82301-312">`[HttpsOnly <Boolean?>]`HttpsOnly: настройка веб-сайта для прием только http-запросов.</span><span class="sxs-lookup"><span data-stu-id="82301-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="82301-313">Перенаправление вопросов по http-запросам</span><span class="sxs-lookup"><span data-stu-id="82301-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="82301-314">`[HyperV <Boolean?>]`: "песочница Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="82301-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="82301-315">`[IdentityType <ManagedServiceIdentityType?>]`: Тип управляемого удостоверения службы.</span><span class="sxs-lookup"><span data-stu-id="82301-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="82301-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`Список удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="82301-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="82301-317">Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторы ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="82301-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="82301-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="82301-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="82301-319">`[IsXenon <Boolean?>]`: Устарело: песочница Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="82301-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="82301-320">`[RedundancyMode <RedundancyMode?>]`: режим избыточности сайта</span><span class="sxs-lookup"><span data-stu-id="82301-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="82301-321">`[Reserved <Boolean?>]`: <code>true</code> если зарезервирован; в противном <code>false</code> случае.</span><span class="sxs-lookup"><span data-stu-id="82301-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82301-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> чтобы остановить сайт SCM (KUDU), когда приложение остановлено; в противном <code>false</code> случае.</span><span class="sxs-lookup"><span data-stu-id="82301-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="82301-323">Значение по <code>false</code> умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="82301-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="82301-324">`[ServerFarmId <String>]`: Код ресурса связанного плана службы приложения в формате "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="82301-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="82301-325">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82301-325">RELATED LINKS</span></span>

