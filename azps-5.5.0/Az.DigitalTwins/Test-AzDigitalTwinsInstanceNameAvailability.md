---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237943"
---
# <span data-ttu-id="4e342-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4e342-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="4e342-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e342-102">SYNOPSIS</span></span>
<span data-ttu-id="4e342-103">Проверьте, доступно ли имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4e342-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="4e342-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e342-104">SYNTAX</span></span>

### <span data-ttu-id="4e342-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e342-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e342-106">Проверка</span><span class="sxs-lookup"><span data-stu-id="4e342-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e342-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e342-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4e342-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4e342-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e342-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e342-109">DESCRIPTION</span></span>
<span data-ttu-id="4e342-110">Проверьте, доступно ли имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4e342-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="4e342-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e342-111">EXAMPLES</span></span>

### <span data-ttu-id="4e342-112">Пример 1. Проверьте имя по расположению и имени.</span><span class="sxs-lookup"><span data-stu-id="4e342-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="4e342-113">Проверьте доступность имени по расположению и имени.</span><span class="sxs-lookup"><span data-stu-id="4e342-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="4e342-114">Пример 2. Проверьте имя digitalTwinsObject и CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="4e342-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="4e342-115">Получите DigitalTwinsInstance и создайте объект Requset, чтобы проверить доступность имени.</span><span class="sxs-lookup"><span data-stu-id="4e342-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="4e342-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e342-116">PARAMETERS</span></span>

### <span data-ttu-id="4e342-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e342-117">-DefaultProfile</span></span>
<span data-ttu-id="4e342-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e342-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e342-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="4e342-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="4e342-120">Результат, возвращенный запросом на доступность имени проверки базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e342-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="4e342-121">Чтобы построить новую схему, см. раздел "ЗАМЕТКИ" для свойств DIGITALTWINSINSTANCECHECKNAME и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4e342-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e342-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e342-122">-InputObject</span></span>
<span data-ttu-id="4e342-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4e342-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e342-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4e342-124">-Location</span></span>
<span data-ttu-id="4e342-125">Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4e342-125">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="4e342-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4e342-126">-Name</span></span>
<span data-ttu-id="4e342-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e342-127">Resource name.</span></span>

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

### <span data-ttu-id="4e342-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e342-128">-SubscriptionId</span></span>
<span data-ttu-id="4e342-129">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="4e342-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="4e342-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e342-130">-Confirm</span></span>
<span data-ttu-id="4e342-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e342-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e342-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e342-132">-WhatIf</span></span>
<span data-ttu-id="4e342-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e342-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e342-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e342-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e342-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e342-135">CommonParameters</span></span>
<span data-ttu-id="4e342-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e342-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e342-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e342-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e342-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e342-138">INPUTS</span></span>

### <span data-ttu-id="4e342-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="4e342-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="4e342-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="4e342-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="4e342-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e342-141">OUTPUTS</span></span>

### <span data-ttu-id="4e342-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="4e342-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="4e342-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e342-143">NOTES</span></span>

<span data-ttu-id="4e342-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4e342-144">ALIASES</span></span>

<span data-ttu-id="4e342-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4e342-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e342-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4e342-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e342-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e342-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e342-148">DIGITALTWINSINSTANCECHECKNAME: результат, возвращенный запросом на доступность имени проверки <ICheckNameRequest> базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e342-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="4e342-149">`Name <String>`: название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e342-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="4e342-150">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="4e342-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e342-151">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4e342-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="4e342-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4e342-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e342-153">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4e342-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4e342-154">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4e342-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4e342-155">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4e342-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4e342-156">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="4e342-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4e342-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e342-157">RELATED LINKS</span></span>

