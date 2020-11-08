---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243571"
---
# <span data-ttu-id="fcef2-101">Restart-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="fcef2-101">Restart-AzFunctionApp</span></span>

## <span data-ttu-id="fcef2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcef2-102">SYNOPSIS</span></span>
<span data-ttu-id="fcef2-103">Перезапускает приложение функции.</span><span class="sxs-lookup"><span data-stu-id="fcef2-103">Restarts a function app.</span></span>

## <span data-ttu-id="fcef2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcef2-104">SYNTAX</span></span>

### <span data-ttu-id="fcef2-105">RestartByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fcef2-105">RestartByName (Default)</span></span>
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fcef2-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="fcef2-106">ByObjectInput</span></span>
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fcef2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcef2-107">DESCRIPTION</span></span>
<span data-ttu-id="fcef2-108">Перезапускает приложение функции.</span><span class="sxs-lookup"><span data-stu-id="fcef2-108">Restarts a function app.</span></span>

## <span data-ttu-id="fcef2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcef2-109">EXAMPLES</span></span>

### <span data-ttu-id="fcef2-110">Пример 1: получение приложения функции по имени и перезапуску.</span><span class="sxs-lookup"><span data-stu-id="fcef2-110">Example 1: Get a function app by name and restart it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

<span data-ttu-id="fcef2-111">Эта команда получает приложение с именем и перезапускает ее.</span><span class="sxs-lookup"><span data-stu-id="fcef2-111">This command gets a function app by name and restarts it.</span></span>

### <span data-ttu-id="fcef2-112">Пример 2. Перезапустите приложение функции по имени.</span><span class="sxs-lookup"><span data-stu-id="fcef2-112">Example 2: Restart a function app by name.</span></span>
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="fcef2-113">Эта команда перезапускает приложение по имени.</span><span class="sxs-lookup"><span data-stu-id="fcef2-113">This command restarts a function app by name.</span></span>

## <span data-ttu-id="fcef2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcef2-114">PARAMETERS</span></span>

### <span data-ttu-id="fcef2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcef2-115">-DefaultProfile</span></span>
<span data-ttu-id="fcef2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcef2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcef2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fcef2-117">-Force</span></span>
<span data-ttu-id="fcef2-118">Принудительно запускает приложение функции без запроса на подтверждение командлета.</span><span class="sxs-lookup"><span data-stu-id="fcef2-118">Forces the cmdlet to restart the function app without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fcef2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcef2-119">-InputObject</span></span>
<span data-ttu-id="fcef2-120">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fcef2-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fcef2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fcef2-121">-Name</span></span>
<span data-ttu-id="fcef2-122">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="fcef2-122">The name of function app.</span></span>

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

### <span data-ttu-id="fcef2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcef2-123">-PassThru</span></span>
<span data-ttu-id="fcef2-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fcef2-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="fcef2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcef2-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="fcef2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fcef2-126">-SubscriptionId</span></span>
<span data-ttu-id="fcef2-127">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="fcef2-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="fcef2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcef2-128">-Confirm</span></span>
<span data-ttu-id="fcef2-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fcef2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcef2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcef2-130">-WhatIf</span></span>
<span data-ttu-id="fcef2-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fcef2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcef2-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fcef2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcef2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcef2-133">CommonParameters</span></span>
<span data-ttu-id="fcef2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcef2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcef2-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcef2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcef2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcef2-136">INPUTS</span></span>

### <span data-ttu-id="fcef2-137">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="fcef2-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="fcef2-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcef2-138">OUTPUTS</span></span>

### <span data-ttu-id="fcef2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fcef2-139">System.Boolean</span></span>

## <span data-ttu-id="fcef2-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcef2-140">NOTES</span></span>

<span data-ttu-id="fcef2-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="fcef2-141">ALIASES</span></span>

<span data-ttu-id="fcef2-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fcef2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fcef2-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fcef2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcef2-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fcef2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fcef2-145">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="fcef2-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="fcef2-146">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="fcef2-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="fcef2-147">`CloningInfoSourceWebAppId <String>`: Идентификатор ресурса ARM исходного приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="fcef2-148">Идентификатор ресурса приложения — это форма/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} для слотов производства и/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} для других слотов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="fcef2-149">`[Kind <String>]`: Типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="fcef2-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="fcef2-150">`[Tag <IResourceTags>]`: Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="fcef2-151">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="fcef2-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fcef2-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> чтобы включить сходство клиентов <code>false</code> , остановите отправку cookie-файлов сходства сеансов, чтобы перенаправлять запросы клиентов в одном сеансе в один и тот же экземпляр.</span><span class="sxs-lookup"><span data-stu-id="fcef2-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="fcef2-153">По умолчанию <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="fcef2-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> Включение проверки подлинности сертификата клиента (TLS-аутентификация); в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="fcef2-155">По умолчанию <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="fcef2-156">`[ClientCertExclusionPath <String>]`: проверка подлинности сертификата клиента с разделителями-запятыми</span><span class="sxs-lookup"><span data-stu-id="fcef2-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="fcef2-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Параметр приложения переопределен для клонированного приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="fcef2-158">Если задано, эти параметры переопределяют параметры, скопированные из исходного приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="fcef2-159">В противном случае сохраняются параметры приложения исходного приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="fcef2-160">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="fcef2-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fcef2-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> позволяет клонировать пользовательские имена узлов из исходного приложения, в противном случае — <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fcef2-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> для клонирования системы управления версиями из исходного приложения, в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fcef2-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> Настройка балансировки нагрузки для исходного и конечного приложений.</span><span class="sxs-lookup"><span data-stu-id="fcef2-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="fcef2-164">`[CloningInfoCorrelationId <String>]`: Идентификатор корреляции операции клонирования.</span><span class="sxs-lookup"><span data-stu-id="fcef2-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="fcef2-165">Этот идентификатор связывает несколько операций клонирования, чтобы использовать один и тот же снимок.</span><span class="sxs-lookup"><span data-stu-id="fcef2-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="fcef2-166">`[CloningInfoHostingEnvironment <String>]`: Среда службы приложений.</span><span class="sxs-lookup"><span data-stu-id="fcef2-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="fcef2-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> чтобы перезаписать конечное приложение, в противном случае — <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fcef2-168">`[CloningInfoSourceWebAppLocation <String>]`: Расположение исходного приложения, например, "Западная часть США" или "Северная Европа"</span><span class="sxs-lookup"><span data-stu-id="fcef2-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="fcef2-169">`[CloningInfoTrafficManagerProfileId <String>]`: Идентификатор ресурса ARM профиля диспетчера трафика, который необходимо использовать, если он существует.</span><span class="sxs-lookup"><span data-stu-id="fcef2-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="fcef2-170">Идентификатор ресурса диспетчера трафика имеет форму/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="fcef2-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="fcef2-171">`[CloningInfoTrafficManagerProfileName <String>]`: Имя создаваемого профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="fcef2-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="fcef2-172">Это требуется, только если профиль диспетчера трафика еще не существует.</span><span class="sxs-lookup"><span data-stu-id="fcef2-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="fcef2-173">`[Config <ISiteConfig>]`: Конфигурация приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="fcef2-174">`IsPushEnabled <Boolean>`: Получает или задает флаг, указывающий, включена ли конечная точка отправки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="fcef2-175">`[ActionMinProcessExecutionTime <String>]`: Минимальное время выполнения процесса перед принятием действия</span><span class="sxs-lookup"><span data-stu-id="fcef2-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="fcef2-176">`[ActionType <AutoHealActionType?>]`: Предопределенные действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="fcef2-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="fcef2-177">`[AlwaysOn <Boolean?>]`: <code>true</code> Если включена постоянная, в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-178">`[ApiDefinitionUrl <String>]`: URL-адрес определения API.</span><span class="sxs-lookup"><span data-stu-id="fcef2-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="fcef2-179">`[ApiManagementConfigId <String>]`: APIM-Api идентификатор.</span><span class="sxs-lookup"><span data-stu-id="fcef2-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="fcef2-180">`[AppCommandLine <String>]`: Командная строка приложения для запуска.</span><span class="sxs-lookup"><span data-stu-id="fcef2-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="fcef2-181">`[AppSetting <INameValuePair[]>]`: Параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="fcef2-182">`[Name <String>]`: Имя пары.</span><span class="sxs-lookup"><span data-stu-id="fcef2-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="fcef2-183">`[Value <String>]`: Значение пары.</span><span class="sxs-lookup"><span data-stu-id="fcef2-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="fcef2-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Если включена функция автоматического автосохранения; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-185">`[AutoSwapSlotName <String>]`: Имя слота автоматического подстановки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="fcef2-186">`[ConnectionString <IConnStringInfo[]>]`: Строки подключения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="fcef2-187">`[ConnectionString <String>]`: Строковое значение подключения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="fcef2-188">`[Name <String>]`: Имя строки подключения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="fcef2-189">`[Type <ConnectionStringType?>]`: Тип базы данных.</span><span class="sxs-lookup"><span data-stu-id="fcef2-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="fcef2-190">`[CorAllowedOrigin <String[]>]`: Возвращает или задает список источников, для которых должны быть разрешены межисточникические вызовы (например: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="fcef2-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="fcef2-191">Используйте "\*" для разрешения всех.</span><span class="sxs-lookup"><span data-stu-id="fcef2-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="fcef2-192">`[CorSupportCredentials <Boolean?>]`: Получает или задает допустимые ли запросы CORS с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="fcef2-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="fcef2-193"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsДля получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="fcef2-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="fcef2-194">`[CustomActionExe <String>]`: Исполняемый файл для запуска.</span><span class="sxs-lookup"><span data-stu-id="fcef2-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="fcef2-195">`[CustomActionParameter <String>]`: Параметры для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="fcef2-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="fcef2-196">`[DefaultDocument <String[]>]`: Документы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fcef2-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="fcef2-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Если включено подробный журнал ошибок; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-198">`[DocumentRoot <String>]`: Корневой каталог документа.</span><span class="sxs-lookup"><span data-stu-id="fcef2-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="fcef2-199">`[DynamicTagsJson <String>]`: Возвращает или задает строку JSON, содержащую список динамических тегов, которые будут вычислены из утверждений пользователей в конечной точке регистрации принудительной отправки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="fcef2-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: Список правил увеличения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="fcef2-201">`[ActionHostName <String>]`: Hostname (область), на который будет перенаправляться трафик, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="fcef2-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="fcef2-202">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="fcef2-202">E.g.</span></span> <span data-ttu-id="fcef2-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="fcef2-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="fcef2-204">`[ChangeDecisionCallbackUrl <String>]`: Настраиваемый алгоритм принятия решений можно задать в расширении сайта TiPCallback, который можно указать URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="fcef2-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="fcef2-205">TiPCallback для формирования шаблонов и контрактов: расширение сайта.</span><span class="sxs-lookup"><span data-stu-id="fcef2-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="fcef2-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="fcef2-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="fcef2-207">`[ChangeIntervalInMinute <Int32?>]`: Определяет интервал в минутах для повторного вычисления ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="fcef2-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="fcef2-208">`[ChangeStep <Double?>]`: В сценарии автоматического увеличения можно добавить/удалить из <code>ReroutePercentage</code> него, пока он не достигнет значения \n <code>MinReroutePercentage</code> или         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="fcef2-209">Показатели сайтов проверяются каждые N минут, указанных в <code>ChangeIntervalInMinutes</code> .\nCustom алгоритме принятия решений, могут быть указаны в TiPCallback сайте расширение сайта, в котором можно указать URL-адрес <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="fcef2-210">`[MaxReroutePercentage <Double?>]`: Определяет верхнюю нижнюю границу, в которой ReroutePercentage остается.</span><span class="sxs-lookup"><span data-stu-id="fcef2-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="fcef2-211">`[MinReroutePercentage <Double?>]`: Определяет нижнюю границу, над которой ReroutePercentage остается.</span><span class="sxs-lookup"><span data-stu-id="fcef2-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="fcef2-212">`[Name <String>]`: Имя правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="fcef2-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="fcef2-213">Рекомендуемое имя должно указывать на слот, который будет принимать трафик в эксперименте.</span><span class="sxs-lookup"><span data-stu-id="fcef2-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="fcef2-214">`[ReroutePercentage <Double?>]`: Процент трафика, на который будут перенаправляться <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="fcef2-215">`[FtpsState <FtpsState?>]`: Состояние службы FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="fcef2-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="fcef2-216">`[HandlerMapping <IHandlerMapping[]>]`: Сопоставления обработчиков.</span><span class="sxs-lookup"><span data-stu-id="fcef2-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="fcef2-217">`[Argument <String>]`: Аргументы командной строки, передаваемые в обработчик сценария.</span><span class="sxs-lookup"><span data-stu-id="fcef2-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="fcef2-218">`[Extension <String>]`: Запросы с этим расширением будут обрабатываться с помощью указанного приложения FastCGI.</span><span class="sxs-lookup"><span data-stu-id="fcef2-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="fcef2-219">`[ScriptProcessor <String>]`: Абсолютный путь к приложению FastCGI.</span><span class="sxs-lookup"><span data-stu-id="fcef2-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="fcef2-220">`[HealthCheckPath <String>]`: Путь проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="fcef2-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="fcef2-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: Настройка веб-сайта, разрешающего клиентам подключаться по протоколу HTTP 2.0</span><span class="sxs-lookup"><span data-stu-id="fcef2-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="fcef2-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Если ведение журнала HTTP включено; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Ограничения IP-безопасности для main.</span><span class="sxs-lookup"><span data-stu-id="fcef2-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="fcef2-224">`[Action <String>]`: Разрешение или запрет доступа для этого диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="fcef2-225">`[Description <String>]`: Описание правила ограничения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="fcef2-226">`[IPAddress <String>]`: IP-адрес, для которого действует ограничение безопасности.</span><span class="sxs-lookup"><span data-stu-id="fcef2-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="fcef2-227">Это может быть только адрес IPv4 (обязательный свойство подсети) или нотация CIDR, например IPv4/маска (первое соответствие разрядов).</span><span class="sxs-lookup"><span data-stu-id="fcef2-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="fcef2-228">Свойство "маска подсети" не должно быть задано для CIDR.</span><span class="sxs-lookup"><span data-stu-id="fcef2-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="fcef2-229">`[Name <String>]`: Имя правила ограничения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="fcef2-230">`[Priority <Int32?>]`: Приоритет правила ограничения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="fcef2-231">`[SubnetMask <String>]`: Маска подсети для диапазона IP-адресов, для которого допустимы ограничения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="fcef2-232">`[SubnetTrafficTag <Int32?>]`: (внутренняя) тег "трафик" подсети</span><span class="sxs-lookup"><span data-stu-id="fcef2-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="fcef2-233">`[Tag <IPFilterTag?>]`: Определяет, для чего будет использоваться этот IP-фильтр.</span><span class="sxs-lookup"><span data-stu-id="fcef2-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="fcef2-234">Это необходимо для поддержки фильтрации IP на прокси-серверах.</span><span class="sxs-lookup"><span data-stu-id="fcef2-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="fcef2-235">`[VnetSubnetResourceId <String>]`: Идентификатор ресурса виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="fcef2-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="fcef2-236">`[VnetTrafficTag <Int32?>]`: (внутренняя) тег "трафик виртуальной сети"</span><span class="sxs-lookup"><span data-stu-id="fcef2-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="fcef2-237">`[JavaContainer <String>]`: Контейнер Java.</span><span class="sxs-lookup"><span data-stu-id="fcef2-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="fcef2-238">`[JavaContainerVersion <String>]`: Версия контейнера Java.</span><span class="sxs-lookup"><span data-stu-id="fcef2-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="fcef2-239">`[JavaVersion <String>]`: Версия Java.</span><span class="sxs-lookup"><span data-stu-id="fcef2-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="fcef2-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Максимально допустимое использование размера диска (МБ).</span><span class="sxs-lookup"><span data-stu-id="fcef2-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="fcef2-241">`[LimitMaxMemoryInMb <Int64?>]`: Максимально допустимое использование памяти в МЕГАБАЙТах.</span><span class="sxs-lookup"><span data-stu-id="fcef2-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="fcef2-242">`[LimitMaxPercentageCpu <Double?>]`: Максимальный разрешенный процент использования ЦП.</span><span class="sxs-lookup"><span data-stu-id="fcef2-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="fcef2-243">`[LinuxFxVersion <String>]`: Платформа и версия приложения для Linux</span><span class="sxs-lookup"><span data-stu-id="fcef2-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="fcef2-244">`[LoadBalancing <SiteLoadBalancing?>]`: Балансировка нагрузки сайта.</span><span class="sxs-lookup"><span data-stu-id="fcef2-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="fcef2-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> для включения Local MySQL; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-журналы. Ограничение размера каталога.</span><span class="sxs-lookup"><span data-stu-id="fcef2-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="fcef2-247">`[MachineKeyDecryption <String>]`: Алгоритм, используемый для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="fcef2-248">`[MachineKeyDecryptionKey <String>]`: Ключ расшифровки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="fcef2-249">`[MachineKeyValidation <String>]`: Проверка MachineKey.</span><span class="sxs-lookup"><span data-stu-id="fcef2-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="fcef2-250">`[MachineKeyValidationKey <String>]`: Ключ проверки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="fcef2-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Режим управляемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="fcef2-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="fcef2-252">`[ManagedServiceIdentityId <Int32?>]`: ИД управляемой службы с удостоверением</span><span class="sxs-lookup"><span data-stu-id="fcef2-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="fcef2-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Настройка минимальной версии TLS, необходимой для запросов SSL</span><span class="sxs-lookup"><span data-stu-id="fcef2-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="fcef2-254">`[NetFrameworkVersion <String>]`: Версия .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fcef2-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="fcef2-255">`[NodeVersion <String>]`: Версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="fcef2-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="fcef2-256">`[NumberOfWorker <Int32?>]`: Количество сотрудников.</span><span class="sxs-lookup"><span data-stu-id="fcef2-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="fcef2-257">`[PhpVersion <String>]`: Версия PHP.</span><span class="sxs-lookup"><span data-stu-id="fcef2-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="fcef2-258">`[PowerShellVersion <String>]`: Версия PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fcef2-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="fcef2-259">`[PreWarmedInstanceCount <Int32?>]`: Количество заданных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="fcef2-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="fcef2-260">Этот параметр применяется только к планам потребления и эластичных БД</span><span class="sxs-lookup"><span data-stu-id="fcef2-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="fcef2-261">`[PublishingUsername <String>]`: Публикация имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="fcef2-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="fcef2-262">`[PushKind <String>]`: Типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="fcef2-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="fcef2-263">`[PythonVersion <String>]`: Версия Python.</span><span class="sxs-lookup"><span data-stu-id="fcef2-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="fcef2-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Если включена удаленная отладка, в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-265">`[RemoteDebuggingVersion <String>]`: Версия удаленной отладки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="fcef2-266">`[RequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="fcef2-267">`[RequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="fcef2-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="fcef2-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> Если трассировка запросов включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-269">`[RequestTracingExpirationTime <DateTime?>]`: Запрос времени окончания срока действия трассировки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="fcef2-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Ограничения IP-безопасности для SCM.</span><span class="sxs-lookup"><span data-stu-id="fcef2-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="fcef2-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Ограничения IP-безопасности для SCM для использования Main.</span><span class="sxs-lookup"><span data-stu-id="fcef2-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="fcef2-272">`[ScmType <ScmType?>]`: Тип SCM.</span><span class="sxs-lookup"><span data-stu-id="fcef2-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="fcef2-273">`[SlowRequestCount <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="fcef2-274">`[SlowRequestTimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="fcef2-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="fcef2-275">`[SlowRequestTimeTaken <String>]`: Затраченное время.</span><span class="sxs-lookup"><span data-stu-id="fcef2-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="fcef2-276">`[TagWhitelistJson <String>]`: Возвращает или задает строку JSON, содержащую список тегов, которые список разрешений использовать для конечной точки регистрации push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="fcef2-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="fcef2-277">`[TagsRequiringAuth <String>]`: Возвращает или задает строку JSON, содержащую список тегов, для использования которых требуется проверка подлинности пользователя в конечной точке регистрации принудительной отправки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="fcef2-278">Теги могут состоять из буквенно-цифровых символов и следующих: "_", "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="fcef2-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="fcef2-279">Проверка должна выполняться на PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="fcef2-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="fcef2-280">`[TracingOption <String>]`: Параметры трассировки.</span><span class="sxs-lookup"><span data-stu-id="fcef2-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="fcef2-281">`[TriggerPrivateBytesInKb <Int32?>]`: Правило, основанное на частных байтах.</span><span class="sxs-lookup"><span data-stu-id="fcef2-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="fcef2-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Правило, основанное на кодах состояния.</span><span class="sxs-lookup"><span data-stu-id="fcef2-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="fcef2-283">`[Count <Int32?>]`: Количество запросов.</span><span class="sxs-lookup"><span data-stu-id="fcef2-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="fcef2-284">`[Status <Int32?>]`: Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="fcef2-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="fcef2-285">`[SubStatus <Int32?>]`: Состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="fcef2-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="fcef2-286">`[TimeInterval <String>]`: Интервал времени.</span><span class="sxs-lookup"><span data-stu-id="fcef2-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="fcef2-287">`[Win32Status <Int32?>]`: Код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="fcef2-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="fcef2-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> использование 32-разрядного рабочего процесса; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-289">`[VirtualApplication <IVirtualApplication[]>]`: Виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="fcef2-290">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="fcef2-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="fcef2-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> , если предварительная загрузка включена; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="fcef2-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Виртуальные каталоги для виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="fcef2-293">`[PhysicalPath <String>]`: Физический путь.</span><span class="sxs-lookup"><span data-stu-id="fcef2-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="fcef2-294">`[VirtualPath <String>]`: Путь к виртуальному приложению.</span><span class="sxs-lookup"><span data-stu-id="fcef2-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="fcef2-295">`[VirtualPath <String>]`: Виртуальный путь.</span><span class="sxs-lookup"><span data-stu-id="fcef2-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="fcef2-296">`[VnetName <String>]`: Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fcef2-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="fcef2-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> Если WebSocket включен; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fcef2-298">`[WindowsFxVersion <String>]`: Платформа и версия приложения ксеноновой</span><span class="sxs-lookup"><span data-stu-id="fcef2-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="fcef2-299">`[XManagedServiceIdentityId <Int32?>]`: Явный идентификатор удостоверения управляемой службы</span><span class="sxs-lookup"><span data-stu-id="fcef2-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="fcef2-300">`[ContainerSize <Int32?>]`: Размер контейнера функций.</span><span class="sxs-lookup"><span data-stu-id="fcef2-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="fcef2-301">`[DailyMemoryTimeQuota <Int32?>]`: Максимально допустимая дневная квота памяти (применимо только к динамическим приложениям).</span><span class="sxs-lookup"><span data-stu-id="fcef2-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="fcef2-302">`[Enabled <Boolean?>]`: <code>true</code> Если приложение включено; в противном случае — <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="fcef2-303">Если задать для этого параметра значение false, приложение будет отключено (приложение переводится в автономный режим).</span><span class="sxs-lookup"><span data-stu-id="fcef2-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="fcef2-304">`[HostNameSslState <IHostNameSslState[]>]`: Состояния SSL hostname используются для управления привязками SSL для имен узлов приложения.</span><span class="sxs-lookup"><span data-stu-id="fcef2-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="fcef2-305">`[HostType <HostType?>]`: Указывает, является ли имя хоста стандартным или именем репозитория.</span><span class="sxs-lookup"><span data-stu-id="fcef2-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="fcef2-306">`[Name <String>]`Имена.</span><span class="sxs-lookup"><span data-stu-id="fcef2-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="fcef2-307">`[SslState <SslState?>]`: Тип SSL.</span><span class="sxs-lookup"><span data-stu-id="fcef2-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="fcef2-308">`[Thumbprint <String>]`: Отпечаток сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="fcef2-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="fcef2-309">`[ToUpdate <Boolean?>]`: Установите для <code>true</code> обновления существующего hostname.</span><span class="sxs-lookup"><span data-stu-id="fcef2-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="fcef2-310">`[VirtualIP <String>]`: Виртуальный IP-адрес, назначенный имени узла, если включен SSL на основе IP.</span><span class="sxs-lookup"><span data-stu-id="fcef2-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="fcef2-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> Отключение общедоступных имен узлов для приложения; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="fcef2-312">Если <code>true</code> приложение доступно только через процесс управления API.</span><span class="sxs-lookup"><span data-stu-id="fcef2-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="fcef2-313">`[HostingEnvironmentProfileId <String>]`: Идентификатор ресурса среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="fcef2-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="fcef2-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: Настройка веб-сайта для приема только запросов HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fcef2-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="fcef2-315">Перенаправление вопросов для HTTP-запросов</span><span class="sxs-lookup"><span data-stu-id="fcef2-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="fcef2-316">`[HyperV <Boolean?>]`: Песочница Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="fcef2-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="fcef2-317">`[IdentityType <ManagedServiceIdentityType?>]`: Тип удостоверения управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="fcef2-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="fcef2-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Список удостоверений пользователей, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="fcef2-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="fcef2-319">Ссылки на ключи словаря удостоверения пользователя будут идентификаторами ресурсов ARM в форме: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="fcef2-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="fcef2-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="fcef2-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fcef2-321">`[IsXenon <Boolean?>]`: Устарело: Песочница Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="fcef2-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="fcef2-322">`[RedundancyMode <RedundancyMode?>]`: Режим избыточности сайта</span><span class="sxs-lookup"><span data-stu-id="fcef2-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="fcef2-323">`[Reserved <Boolean?>]`: <code>true</code> по зарезервированному; в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fcef2-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> чтобы остановить сайт SCM (KUDU), когда приложение остановлено, в противном случае <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="fcef2-325">По умолчанию используется значение <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fcef2-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="fcef2-326">`[ServerFarmId <String>]`: Идентификатор ресурса связанного плана служб приложений, отформатированный как "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="fcef2-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="fcef2-327">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcef2-327">RELATED LINKS</span></span>

