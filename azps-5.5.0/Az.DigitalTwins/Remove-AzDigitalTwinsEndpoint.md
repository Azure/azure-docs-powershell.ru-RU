---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230433"
---
# <span data-ttu-id="80c64-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c64-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="80c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c64-102">SYNOPSIS</span></span>
<span data-ttu-id="80c64-103">Удаление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80c64-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="80c64-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80c64-104">SYNTAX</span></span>

### <span data-ttu-id="80c64-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80c64-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="80c64-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80c64-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80c64-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80c64-107">DESCRIPTION</span></span>
<span data-ttu-id="80c64-108">Удаление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80c64-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="80c64-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80c64-109">EXAMPLES</span></span>

### <span data-ttu-id="80c64-110">Пример 1. Удаление azDigitalTwinsEndPoint от EndPointName</span><span class="sxs-lookup"><span data-stu-id="80c64-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="80c64-111">Удаление azDigitalTwinsEndPoint от EndPointName ResourceGroupName и ResourceName</span><span class="sxs-lookup"><span data-stu-id="80c64-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="80c64-112">Пример 2. Удаление azDigitalTwinsEndPoint по объекту</span><span class="sxs-lookup"><span data-stu-id="80c64-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="80c64-113">Удаление azDigitalTwinsEndPoint по объекту</span><span class="sxs-lookup"><span data-stu-id="80c64-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="80c64-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80c64-114">PARAMETERS</span></span>

### <span data-ttu-id="80c64-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80c64-115">-AsJob</span></span>
<span data-ttu-id="80c64-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="80c64-116">Run the command as a job</span></span>

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

### <span data-ttu-id="80c64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c64-117">-DefaultProfile</span></span>
<span data-ttu-id="80c64-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80c64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c64-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="80c64-119">-EndpointName</span></span>
<span data-ttu-id="80c64-120">Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="80c64-120">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c64-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80c64-121">-InputObject</span></span>
<span data-ttu-id="80c64-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="80c64-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80c64-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80c64-123">-NoWait</span></span>
<span data-ttu-id="80c64-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="80c64-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80c64-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80c64-125">-PassThru</span></span>
<span data-ttu-id="80c64-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="80c64-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80c64-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c64-127">-ResourceGroupName</span></span>
<span data-ttu-id="80c64-128">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80c64-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c64-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="80c64-129">-ResourceName</span></span>
<span data-ttu-id="80c64-130">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80c64-130">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c64-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80c64-131">-SubscriptionId</span></span>
<span data-ttu-id="80c64-132">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="80c64-132">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c64-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80c64-133">-Confirm</span></span>
<span data-ttu-id="80c64-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c64-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c64-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c64-135">-WhatIf</span></span>
<span data-ttu-id="80c64-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c64-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c64-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="80c64-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c64-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c64-138">CommonParameters</span></span>
<span data-ttu-id="80c64-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c64-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c64-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c64-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c64-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80c64-141">INPUTS</span></span>

### <span data-ttu-id="80c64-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="80c64-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="80c64-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80c64-143">OUTPUTS</span></span>

### <span data-ttu-id="80c64-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="80c64-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="80c64-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80c64-145">NOTES</span></span>

<span data-ttu-id="80c64-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="80c64-146">ALIASES</span></span>

<span data-ttu-id="80c64-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="80c64-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80c64-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="80c64-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80c64-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80c64-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80c64-150">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="80c64-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80c64-151">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="80c64-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="80c64-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="80c64-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80c64-153">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80c64-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80c64-154">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80c64-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80c64-155">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80c64-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80c64-156">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="80c64-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="80c64-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80c64-157">RELATED LINKS</span></span>

