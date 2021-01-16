---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326762"
---
# <span data-ttu-id="68874-101">Restart-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="68874-101">Restart-AzFunctionApp</span></span>

## <span data-ttu-id="68874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68874-102">SYNOPSIS</span></span>
<span data-ttu-id="68874-103">Перезапуск приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="68874-103">Restarts a function app.</span></span>

## <span data-ttu-id="68874-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68874-104">SYNTAX</span></span>

### <span data-ttu-id="68874-105">RestartByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68874-105">RestartByName (Default)</span></span>
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68874-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="68874-106">ByObjectInput</span></span>
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68874-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68874-107">DESCRIPTION</span></span>
<span data-ttu-id="68874-108">Перезапуск приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="68874-108">Restarts a function app.</span></span>

## <span data-ttu-id="68874-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68874-109">EXAMPLES</span></span>

### <span data-ttu-id="68874-110">Пример 1. Получите приложение функции по имени и перезапустите его.</span><span class="sxs-lookup"><span data-stu-id="68874-110">Example 1: Get a function app by name and restart it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

<span data-ttu-id="68874-111">Эта команда получает приложение функции по имени и перезапускает его.</span><span class="sxs-lookup"><span data-stu-id="68874-111">This command gets a function app by name and restarts it.</span></span>

### <span data-ttu-id="68874-112">Пример 2. Перезапустите приложение функции по имени.</span><span class="sxs-lookup"><span data-stu-id="68874-112">Example 2: Restart a function app by name.</span></span>
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="68874-113">Эта команда перезапускет приложение функции по имени.</span><span class="sxs-lookup"><span data-stu-id="68874-113">This command restarts a function app by name.</span></span>

## <span data-ttu-id="68874-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68874-114">PARAMETERS</span></span>

### <span data-ttu-id="68874-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68874-115">-DefaultProfile</span></span>
<span data-ttu-id="68874-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68874-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68874-117">-Force</span><span class="sxs-lookup"><span data-stu-id="68874-117">-Force</span></span>
<span data-ttu-id="68874-118">Этот пуск позволяет перезапустить приложение функции, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="68874-118">Forces the cmdlet to restart the function app without prompting for confirmation.</span></span>

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

### <span data-ttu-id="68874-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68874-119">-InputObject</span></span>
<span data-ttu-id="68874-120">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="68874-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="68874-121">-Name</span><span class="sxs-lookup"><span data-stu-id="68874-121">-Name</span></span>
<span data-ttu-id="68874-122">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="68874-122">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68874-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68874-123">-PassThru</span></span>
<span data-ttu-id="68874-124">Возвращает "Истина" в случае успешного наоборот.</span><span class="sxs-lookup"><span data-stu-id="68874-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="68874-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68874-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68874-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68874-126">-SubscriptionId</span></span>
<span data-ttu-id="68874-127">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="68874-127">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68874-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68874-128">-Confirm</span></span>
<span data-ttu-id="68874-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="68874-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68874-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68874-130">-WhatIf</span></span>
<span data-ttu-id="68874-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68874-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68874-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="68874-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68874-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68874-133">CommonParameters</span></span>
<span data-ttu-id="68874-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68874-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68874-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68874-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68874-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68874-136">INPUTS</span></span>

### <span data-ttu-id="68874-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="68874-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="68874-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68874-138">OUTPUTS</span></span>

### <span data-ttu-id="68874-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68874-139">System.Boolean</span></span>

## <span data-ttu-id="68874-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68874-140">NOTES</span></span>

<span data-ttu-id="68874-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="68874-141">ALIASES</span></span>

<span data-ttu-id="68874-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="68874-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68874-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="68874-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68874-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68874-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68874-145"><ISite>INPUTOBJECT:</span><span class="sxs-lookup"><span data-stu-id="68874-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="68874-146">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="68874-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="68874-147">`CloningInfoSourceWebAppId <String>`: ARM ресурса в приложении-источнике.</span><span class="sxs-lookup"><span data-stu-id="68874-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="68874-148">ИД ресурса приложения имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} для производственных слотов и /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} для других слотов.</span><span class="sxs-lookup"><span data-stu-id="68874-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="68874-149">`[Kind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="68874-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="68874-150">`[Tag <IResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68874-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="68874-151">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="68874-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="68874-152">`[ClientAffinityEnabled <Boolean?>]`: включить клиентские сходства; прекратить отправку файлов cookie сеанса, которые будут маршрутить запросы клиентов в том же сеансе <code>true</code> <code>false</code> в тот же экземпляр.</span><span class="sxs-lookup"><span data-stu-id="68874-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="68874-153">Значение по умолчанию <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="68874-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> чтобы включить проверку подлинности сертификата клиента (в общих проверках TLS); в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="68874-155">Значение по умолчанию <code>false</code> : .</span><span class="sxs-lookup"><span data-stu-id="68874-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="68874-156">`[ClientCertExclusionPath <String>]`: пути исключения, разделенные запятой для проверки подлинности сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="68874-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="68874-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: параметры приложений переопределяются для клонированных приложений.</span><span class="sxs-lookup"><span data-stu-id="68874-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="68874-158">При этом эти параметры переопределяют параметры, клонированные из приложения-источника.</span><span class="sxs-lookup"><span data-stu-id="68874-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="68874-159">В противном случае параметры приложения из источника сохраняются.</span><span class="sxs-lookup"><span data-stu-id="68874-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="68874-160">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="68874-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="68874-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> для клонирования пользовательских имен хостов из приложения-источника; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="68874-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> чтобы клонировать управление исходным источником из source app; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="68874-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> чтобы настроить балансировку нагрузки для приложения для назначения и источника.</span><span class="sxs-lookup"><span data-stu-id="68874-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="68874-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span><span class="sxs-lookup"><span data-stu-id="68874-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="68874-165">Этот ID связывает несколько операций клонирования, чтобы использовать один и тот же моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="68874-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="68874-166">`[CloningInfoHostingEnvironment <String>]`: Среда службы приложений.</span><span class="sxs-lookup"><span data-stu-id="68874-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="68874-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> чтобы переписать приложение; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="68874-168">`[CloningInfoSourceWebAppLocation <String>]`: Расположение source app ex: West US or North Europe</span><span class="sxs-lookup"><span data-stu-id="68874-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="68874-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ресурса профиля Диспетчера трафика, если он существует.</span><span class="sxs-lookup"><span data-stu-id="68874-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="68874-170">Код ресурса Диспетчера трафика имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="68874-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="68874-171">`[CloningInfoTrafficManagerProfileName <String>]`: Имя профиля Диспетчера трафика, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="68874-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="68874-172">Это необходимо только в том случае, если профиль Диспетчера трафика еще не существует.</span><span class="sxs-lookup"><span data-stu-id="68874-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="68874-173">`[Config <ISiteConfig>]`: Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="68874-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="68874-174">`IsPushEnabled <Boolean>`: получает или устанавливает флажок, указывающий, включена ли конечная точка push-сигнала.</span><span class="sxs-lookup"><span data-stu-id="68874-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="68874-175">`[ActionMinProcessExecutionTime <String>]`: минимальное время, необходимое для выполнения процесса перед выполнением действия</span><span class="sxs-lookup"><span data-stu-id="68874-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="68874-176">`[ActionType <AutoHealActionType?>]`: Предопределяемая мера.</span><span class="sxs-lookup"><span data-stu-id="68874-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="68874-177">`[AlwaysOn <Boolean?>]`: <code>true</code> если включена always on; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-178">`[ApiDefinitionUrl <String>]`URL-адрес определения API.</span><span class="sxs-lookup"><span data-stu-id="68874-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="68874-179">`[ApiManagementConfigId <String>]`: APIM-Api идентификатора.</span><span class="sxs-lookup"><span data-stu-id="68874-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="68874-180">`[AppCommandLine <String>]`: запуск командной строки приложения.</span><span class="sxs-lookup"><span data-stu-id="68874-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="68874-181">`[AppSetting <INameValuePair[]>]`: Параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="68874-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="68874-182">`[Name <String>]`: Парное имя.</span><span class="sxs-lookup"><span data-stu-id="68874-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="68874-183">`[Value <String>]`: Парный значение.</span><span class="sxs-lookup"><span data-stu-id="68874-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="68874-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> если автосъемка включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-185">`[AutoSwapSlotName <String>]`: название разъема для автоматического обмена.</span><span class="sxs-lookup"><span data-stu-id="68874-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="68874-186">`[ConnectionString <IConnStringInfo[]>]`: строки подключения.</span><span class="sxs-lookup"><span data-stu-id="68874-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="68874-187">`[ConnectionString <String>]`: строка подключения.</span><span class="sxs-lookup"><span data-stu-id="68874-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="68874-188">`[Name <String>]`: Имя строки подключения.</span><span class="sxs-lookup"><span data-stu-id="68874-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="68874-189">`[Type <ConnectionStringType?>]`: Тип базы данных.</span><span class="sxs-lookup"><span data-stu-id="68874-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="68874-190">`[CorAllowedOrigin <String[]>]`: получает или задает список источников, которые должны быть разрешены для звонков в перекрестных источниках (например: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="68874-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="68874-191">Используйте "\*", чтобы разрешить все.</span><span class="sxs-lookup"><span data-stu-id="68874-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="68874-192">`[CorSupportCredentials <Boolean?>]`: получает или устанавливает, разрешено ли запросы CORS с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="68874-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="68874-193">Дополнительные         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="68874-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="68874-194">`[CustomActionExe <String>]`: исполняемый для выполнения.</span><span class="sxs-lookup"><span data-stu-id="68874-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="68874-195">`[CustomActionParameter <String>]`: Параметры исполняемого исполняемого параметров.</span><span class="sxs-lookup"><span data-stu-id="68874-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="68874-196">`[DefaultDocument <String[]>]`: Документы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68874-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="68874-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> если включено подробное ведение журнала ошибок; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-198">`[DocumentRoot <String>]`: корневой документ.</span><span class="sxs-lookup"><span data-stu-id="68874-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="68874-199">`[DynamicTagsJson <String>]`: возвращает или задает строку JSON, содержащую список динамических тегов, которые будут вычисляться из утверждений пользователей на конечной точке push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="68874-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="68874-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: Список правил для работы с новыми бизнес-ами.</span><span class="sxs-lookup"><span data-stu-id="68874-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="68874-201">`[ActionHostName <String>]`: Hostname of a slot, to which the traffic will be redirected if decided to.</span><span class="sxs-lookup"><span data-stu-id="68874-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="68874-202">Например,</span><span class="sxs-lookup"><span data-stu-id="68874-202">E.g.</span></span> <span data-ttu-id="68874-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="68874-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="68874-204">`[ChangeDecisionCallbackUrl <String>]`В расширении сайта TiPCallback можно у указывается алгоритм пользовательского решения.</span><span class="sxs-lookup"><span data-stu-id="68874-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="68874-205">Подробнее о scaffold и контрактах см. в расширении сайта TiPCallback.</span><span class="sxs-lookup"><span data-stu-id="68874-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="68874-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="68874-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="68874-207">`[ChangeIntervalInMinute <Int32?>]`: определяет интервал в минутах для повторного проговаривания ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="68874-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="68874-208">`[ChangeStep <Double?>]`. В автоматическом сценарии обнуляйте эту возможность, пока не дойдете до <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> или         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="68874-209">Метрики сайта проверяются каждые N минут, указанные в .\nCustom, алгоритм решения можно у регистрировать в расширении сайта TiPCallback, в котором можно укастить <code>ChangeIntervalInMinutes</code> <code>ChangeDecisionCallbackUrl</code> URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="68874-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="68874-210">`[MaxReroutePercentage <Double?>]`: указывает верхнюю границу, под которой будет находиться ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="68874-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="68874-211">`[MinReroutePercentage <Double?>]`: указывает нижнюю границу, над которой будет находиться ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="68874-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="68874-212">`[Name <String>]`: имя правила маршрутки.</span><span class="sxs-lookup"><span data-stu-id="68874-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="68874-213">Рекомендуется указать на слот, в котором будет приниматься трафик в эксперименте.</span><span class="sxs-lookup"><span data-stu-id="68874-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="68874-214">`[ReroutePercentage <Double?>]`: процент трафика, на который будет перенаправлен <code>ActionHostName</code> трафик.</span><span class="sxs-lookup"><span data-stu-id="68874-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="68874-215">`[FtpsState <FtpsState?>]`: состояние FTP или FTPS</span><span class="sxs-lookup"><span data-stu-id="68874-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="68874-216">`[HandlerMapping <IHandlerMapping[]>]`: Сопоставления обработера.</span><span class="sxs-lookup"><span data-stu-id="68874-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="68874-217">`[Argument <String>]`: аргументы командной строки, которые передаются в процессор сценариев.</span><span class="sxs-lookup"><span data-stu-id="68874-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="68874-218">`[Extension <String>]`: Запросы с этим расширением обрабатываются с помощью указанного приложения FastCGI.</span><span class="sxs-lookup"><span data-stu-id="68874-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="68874-219">`[ScriptProcessor <String>]`— абсолютный путь к приложению FastCGI.</span><span class="sxs-lookup"><span data-stu-id="68874-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="68874-220">`[HealthCheckPath <String>]`: путь проверки здоровья</span><span class="sxs-lookup"><span data-stu-id="68874-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="68874-221">`[Http20Enabled <Boolean?>]`Http20Enabled: настройка веб-сайта для разрешения клиентам подключения через http2.0</span><span class="sxs-lookup"><span data-stu-id="68874-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="68874-222">`[HttpLoggingEnabled <Boolean?>]`: если включено ведение журнала <code>true</code> HTTP; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP для основного.</span><span class="sxs-lookup"><span data-stu-id="68874-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="68874-224">`[Action <String>]`. Разрешить или запретить доступ для этого диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="68874-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="68874-225">`[Description <String>]`: Описание правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="68874-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="68874-226">`[IPAddress <String>]`: IP-адрес, на который действует ограничение безопасности.</span><span class="sxs-lookup"><span data-stu-id="68874-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="68874-227">Оно может быть в виде чистого ipv4-адреса (обязательного свойства SubnetMask) или нотации CIDR, например ipv4/mask (совпадение с ведущим битом).</span><span class="sxs-lookup"><span data-stu-id="68874-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="68874-228">Для CIDR свойство SubnetMask не должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="68874-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="68874-229">`[Name <String>]`: имя правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="68874-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="68874-230">`[Priority <Int32?>]`: Приоритет правила ограничения IP.</span><span class="sxs-lookup"><span data-stu-id="68874-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="68874-231">`[SubnetMask <String>]`: Маска подсети для диапазона IP-адресов, на которые действует ограничение.</span><span class="sxs-lookup"><span data-stu-id="68874-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="68874-232">`[SubnetTrafficTag <Int32?>]`: (внутренний) тег трафика подсети</span><span class="sxs-lookup"><span data-stu-id="68874-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="68874-233">`[Tag <IPFilterTag?>]`: определяет, для чего будет использоваться этот ФИЛЬТР IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="68874-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="68874-234">Это необходимо для поддержки фильтрации по IP-адресам на прокси-прокси.</span><span class="sxs-lookup"><span data-stu-id="68874-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="68874-235">`[VnetSubnetResourceId <String>]`: ИД виртуального сетевого ресурса</span><span class="sxs-lookup"><span data-stu-id="68874-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="68874-236">`[VnetTrafficTag <Int32?>]`: (внутренний) тег трафика Vnet</span><span class="sxs-lookup"><span data-stu-id="68874-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="68874-237">`[JavaContainer <String>]`: контейнер Java.</span><span class="sxs-lookup"><span data-stu-id="68874-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="68874-238">`[JavaContainerVersion <String>]`: Версия контейнера Java.</span><span class="sxs-lookup"><span data-stu-id="68874-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="68874-239">`[JavaVersion <String>]`: Версия Java.</span><span class="sxs-lookup"><span data-stu-id="68874-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="68874-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Максимальный допустимый размер диска в МБ.</span><span class="sxs-lookup"><span data-stu-id="68874-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="68874-241">`[LimitMaxMemoryInMb <Int64?>]`: Максимальное разрешено использование памяти в МБ.</span><span class="sxs-lookup"><span data-stu-id="68874-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="68874-242">`[LimitMaxPercentageCpu <Double?>]`: Процент использования ЦП (максимально допустимый).</span><span class="sxs-lookup"><span data-stu-id="68874-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="68874-243">`[LinuxFxVersion <String>]`: Linux App Framework и версия</span><span class="sxs-lookup"><span data-stu-id="68874-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="68874-244">`[LoadBalancing <SiteLoadBalancing?>]`: Балансировка нагрузки сайта.</span><span class="sxs-lookup"><span data-stu-id="68874-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="68874-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> чтобы включить локальный MySQL; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-246">`[LogsDirectorySizeLimit <Int32?>]`: ограничение размера каталога http-журналов.</span><span class="sxs-lookup"><span data-stu-id="68874-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="68874-247">`[MachineKeyDecryption <String>]`: алгоритм, используемый для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="68874-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="68874-248">`[MachineKeyDecryptionKey <String>]`: ключ расшифровки.</span><span class="sxs-lookup"><span data-stu-id="68874-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="68874-249">`[MachineKeyValidation <String>]`: Проверка MachineKey.</span><span class="sxs-lookup"><span data-stu-id="68874-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="68874-250">`[MachineKeyValidationKey <String>]`: Ключ проверки.</span><span class="sxs-lookup"><span data-stu-id="68874-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="68874-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Управляемый режим конвейера.</span><span class="sxs-lookup"><span data-stu-id="68874-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="68874-252">`[ManagedServiceIdentityId <Int32?>]`: Идентификатор управляемой службы</span><span class="sxs-lookup"><span data-stu-id="68874-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="68874-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: настройка минимальной версии TLS, необходимой для SSL-запросов</span><span class="sxs-lookup"><span data-stu-id="68874-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="68874-254">`[NetFrameworkVersion <String>]`: версия .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="68874-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="68874-255">`[NodeVersion <String>]`: Версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="68874-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="68874-256">`[NumberOfWorker <Int32?>]`: Количество сотрудников.</span><span class="sxs-lookup"><span data-stu-id="68874-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="68874-257">`[PhpVersion <String>]`: Версия PHP.</span><span class="sxs-lookup"><span data-stu-id="68874-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="68874-258">`[PowerShellVersion <String>]`: версия PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68874-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="68874-259">`[PreWarmedInstanceCount <Int32?>]`: Количество предварительно заранее заархи</span><span class="sxs-lookup"><span data-stu-id="68874-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="68874-260">Этот параметр применяется только к планам потребления и эластичности.</span><span class="sxs-lookup"><span data-stu-id="68874-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="68874-261">`[PublishingUsername <String>]`: имя пользователя публикации.</span><span class="sxs-lookup"><span data-stu-id="68874-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="68874-262">`[PushKind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="68874-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="68874-263">`[PythonVersion <String>]`: Version of Python.</span><span class="sxs-lookup"><span data-stu-id="68874-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="68874-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> если включена удаленная отладка; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-265">`[RemoteDebuggingVersion <String>]`: Версия удаленного отладки.</span><span class="sxs-lookup"><span data-stu-id="68874-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="68874-266">`[RequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="68874-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="68874-267">`[RequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="68874-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="68874-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> если включена трассировка запроса; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-269">`[RequestTracingExpirationTime <DateTime?>]`: запрос на трассировку срока действия.</span><span class="sxs-lookup"><span data-stu-id="68874-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="68874-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP-адресов для SCM.</span><span class="sxs-lookup"><span data-stu-id="68874-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="68874-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ограничения безопасности IP-адресов для использования основного.</span><span class="sxs-lookup"><span data-stu-id="68874-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="68874-272">`[ScmType <ScmType?>]`: тип SCM.</span><span class="sxs-lookup"><span data-stu-id="68874-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="68874-273">`[SlowRequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="68874-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="68874-274">`[SlowRequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="68874-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="68874-275">`[SlowRequestTimeTaken <String>]`: время, за взятое.</span><span class="sxs-lookup"><span data-stu-id="68874-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="68874-276">`[TagWhitelistJson <String>]`: возвращает или задает строку JSON, содержащую список тегов, которые будут исключены в белый список для использования конечной точкой push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="68874-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="68874-277">`[TagsRequiringAuth <String>]`: возвращает или задает строку JSON, содержащую список тегов, для которых требуется проверка подлинности пользователя в конечной точке push-регистрации.</span><span class="sxs-lookup"><span data-stu-id="68874-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="68874-278">Теги могут состоять из букв и цифр и следующих знаков: '_', '@', '#', '.', ':', '-'</span><span class="sxs-lookup"><span data-stu-id="68874-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="68874-279">Проверка должна выполняться в pushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="68874-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="68874-280">`[TracingOption <String>]`: Параметры трасситуры.</span><span class="sxs-lookup"><span data-stu-id="68874-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="68874-281">`[TriggerPrivateBytesInKb <Int32?>]`: правило, основанное на закрытыхбайтах.</span><span class="sxs-lookup"><span data-stu-id="68874-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="68874-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: правило, основанное на кодах состояния.</span><span class="sxs-lookup"><span data-stu-id="68874-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="68874-283">`[Count <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="68874-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="68874-284">`[Status <Int32?>]`: код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="68874-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="68874-285">`[SubStatus <Int32?>]`: Запросить состояние подгруппы.</span><span class="sxs-lookup"><span data-stu-id="68874-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="68874-286">`[TimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="68874-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="68874-287">`[Win32Status <Int32?>]`: код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="68874-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="68874-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> использовать процесс 32-битных сотрудников; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-289">`[VirtualApplication <IVirtualApplication[]>]`: Виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="68874-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="68874-290">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="68874-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="68874-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> если включена предварительная загрузка; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="68874-292">`[VirtualDirectory <IVirtualDirectory[]>]`: виртуальные каталоги для виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="68874-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="68874-293">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="68874-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="68874-294">`[VirtualPath <String>]`: Путь к виртуальному приложению.</span><span class="sxs-lookup"><span data-stu-id="68874-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="68874-295">`[VirtualPath <String>]`: Виртуальный путь.</span><span class="sxs-lookup"><span data-stu-id="68874-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="68874-296">`[VnetName <String>]`: Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="68874-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="68874-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> если webSocket включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="68874-298">`[WindowsFxVersion <String>]`: Xenon App Framework и версия</span><span class="sxs-lookup"><span data-stu-id="68874-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="68874-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span><span class="sxs-lookup"><span data-stu-id="68874-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="68874-300">`[ContainerSize <Int32?>]`: Размер контейнера функции.</span><span class="sxs-lookup"><span data-stu-id="68874-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="68874-301">`[DailyMemoryTimeQuota <Int32?>]`: Максимальная квота суточного времени памяти (применима только для динамических приложений).</span><span class="sxs-lookup"><span data-stu-id="68874-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="68874-302">`[Enabled <Boolean?>]`: <code>true</code> если приложение включено; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="68874-303">Если установить для этого значения значение false, приложение отключается (переключает его в автономный режим).</span><span class="sxs-lookup"><span data-stu-id="68874-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="68874-304">`[HostNameSslState <IHostNameSslState[]>]`: Состояния SSL hostname используются для управления привязками SSL для имен хостов приложения.</span><span class="sxs-lookup"><span data-stu-id="68874-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="68874-305">`[HostType <HostType?>]`: указывает, является ли имя хранилищ стандартным или репозиторием.</span><span class="sxs-lookup"><span data-stu-id="68874-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="68874-306">`[Name <String>]`: Hostname ..</span><span class="sxs-lookup"><span data-stu-id="68874-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="68874-307">`[SslState <SslState?>]`: Тип SSL.</span><span class="sxs-lookup"><span data-stu-id="68874-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="68874-308">`[Thumbprint <String>]`: Эскиз SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="68874-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="68874-309">`[ToUpdate <Boolean?>]`: Установите этот <code>true</code> код для обновления существующего имени.</span><span class="sxs-lookup"><span data-stu-id="68874-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="68874-310">`[VirtualIP <String>]`: Виртуальный IP-адрес, присвоенный имени хоста, если включен SSL на основе IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="68874-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="68874-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> чтобы отключить общедоступные имена хостов приложения; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="68874-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="68874-312">Если приложение доступно только в процессе управления <code>true</code> API.</span><span class="sxs-lookup"><span data-stu-id="68874-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="68874-313">`[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="68874-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="68874-314">`[HttpsOnly <Boolean?>]`HttpsOnly: настройка веб-сайта для прием только http-запросов.</span><span class="sxs-lookup"><span data-stu-id="68874-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="68874-315">Перенаправление вопросов по http-запросам</span><span class="sxs-lookup"><span data-stu-id="68874-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="68874-316">`[HyperV <Boolean?>]`: "песочница Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="68874-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="68874-317">`[IdentityType <ManagedServiceIdentityType?>]`: Тип управляемого удостоверения службы.</span><span class="sxs-lookup"><span data-stu-id="68874-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="68874-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`Список удостоверений, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="68874-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="68874-319">Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторы ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="68874-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="68874-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="68874-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="68874-321">`[IsXenon <Boolean?>]`: Устарело: песочница Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="68874-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="68874-322">`[RedundancyMode <RedundancyMode?>]`: режим избыточности сайта</span><span class="sxs-lookup"><span data-stu-id="68874-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="68874-323">`[Reserved <Boolean?>]`: <code>true</code> если зарезервирован; в противном <code>false</code> случае.</span><span class="sxs-lookup"><span data-stu-id="68874-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="68874-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> чтобы остановить сайт SCM (KUDU), когда приложение остановлено; в противном <code>false</code> случае.</span><span class="sxs-lookup"><span data-stu-id="68874-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="68874-325">Значение по <code>false</code> умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="68874-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="68874-326">`[ServerFarmId <String>]`: Код ресурса связанного плана службы приложения в формате "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="68874-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="68874-327">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68874-327">RELATED LINKS</span></span>
