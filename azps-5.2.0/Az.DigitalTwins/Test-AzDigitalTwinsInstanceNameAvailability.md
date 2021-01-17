---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402407"
---
# <span data-ttu-id="37ed2-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="37ed2-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="37ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="37ed2-103">Проверьте, доступно ли имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37ed2-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="37ed2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37ed2-104">SYNTAX</span></span>

### <span data-ttu-id="37ed2-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37ed2-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37ed2-106">Проверка</span><span class="sxs-lookup"><span data-stu-id="37ed2-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37ed2-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37ed2-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="37ed2-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37ed2-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37ed2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37ed2-109">DESCRIPTION</span></span>
<span data-ttu-id="37ed2-110">Проверьте, доступно ли имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37ed2-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="37ed2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37ed2-111">EXAMPLES</span></span>

### <span data-ttu-id="37ed2-112">Пример 1. Проверьте имя по расположению и имени.</span><span class="sxs-lookup"><span data-stu-id="37ed2-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="37ed2-113">Проверьте доступность имени по расположению и имени.</span><span class="sxs-lookup"><span data-stu-id="37ed2-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="37ed2-114">Пример 2. Проверьте имя digitalTwinsObject и CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="37ed2-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="37ed2-115">Получите DigitalTwinsInstance и создайте объект Requset, чтобы проверить доступность имени.</span><span class="sxs-lookup"><span data-stu-id="37ed2-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="37ed2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37ed2-116">PARAMETERS</span></span>

### <span data-ttu-id="37ed2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ed2-117">-DefaultProfile</span></span>
<span data-ttu-id="37ed2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37ed2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ed2-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="37ed2-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="37ed2-120">Результат, возвращенный запросом на доступность имени проверки базы данных.</span><span class="sxs-lookup"><span data-stu-id="37ed2-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="37ed2-121">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств DIGITALTWINSINSTANCECHECKNAME и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="37ed2-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37ed2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37ed2-122">-InputObject</span></span>
<span data-ttu-id="37ed2-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="37ed2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37ed2-124">-Location</span><span class="sxs-lookup"><span data-stu-id="37ed2-124">-Location</span></span>
<span data-ttu-id="37ed2-125">Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37ed2-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ed2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="37ed2-126">-Name</span></span>
<span data-ttu-id="37ed2-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="37ed2-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ed2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37ed2-128">-SubscriptionId</span></span>
<span data-ttu-id="37ed2-129">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="37ed2-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ed2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37ed2-130">-Confirm</span></span>
<span data-ttu-id="37ed2-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ed2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ed2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ed2-132">-WhatIf</span></span>
<span data-ttu-id="37ed2-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ed2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ed2-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="37ed2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ed2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ed2-135">CommonParameters</span></span>
<span data-ttu-id="37ed2-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ed2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ed2-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37ed2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ed2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37ed2-138">INPUTS</span></span>

### <span data-ttu-id="37ed2-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="37ed2-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="37ed2-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="37ed2-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="37ed2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37ed2-141">OUTPUTS</span></span>

### <span data-ttu-id="37ed2-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="37ed2-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="37ed2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37ed2-143">NOTES</span></span>

<span data-ttu-id="37ed2-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="37ed2-144">ALIASES</span></span>

<span data-ttu-id="37ed2-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="37ed2-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37ed2-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="37ed2-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37ed2-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37ed2-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37ed2-148">DIGITALTWINSINSTANCECHECKNAME: результат, возвращенный запросом на доступность имени проверки <ICheckNameRequest> базы данных.</span><span class="sxs-lookup"><span data-stu-id="37ed2-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="37ed2-149">`Name <String>`: название ресурса.</span><span class="sxs-lookup"><span data-stu-id="37ed2-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="37ed2-150">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="37ed2-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37ed2-151">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="37ed2-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="37ed2-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="37ed2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37ed2-153">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37ed2-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37ed2-154">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37ed2-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37ed2-155">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37ed2-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37ed2-156">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="37ed2-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="37ed2-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37ed2-157">RELATED LINKS</span></span>

