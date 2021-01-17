---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402484"
---
# <span data-ttu-id="66be2-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="66be2-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="66be2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66be2-102">SYNOPSIS</span></span>
<span data-ttu-id="66be2-103">Получить конечную точку DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="66be2-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="66be2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="66be2-104">SYNTAX</span></span>

### <span data-ttu-id="66be2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66be2-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66be2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="66be2-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66be2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="66be2-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="66be2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66be2-108">DESCRIPTION</span></span>
<span data-ttu-id="66be2-109">Получить конечную точку DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="66be2-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="66be2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="66be2-110">EXAMPLES</span></span>

### <span data-ttu-id="66be2-111">Пример 1. List AzDigitalTwinsEndpoint в ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66be2-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="66be2-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66be2-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="66be2-113">Пример 2. Get AzDigitalTwinsEndpoint by EndpointName</span><span class="sxs-lookup"><span data-stu-id="66be2-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="66be2-114">Get AzDigitalTwinsEndpoint by EndpointName в ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66be2-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="66be2-115">Пример 3. Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span><span class="sxs-lookup"><span data-stu-id="66be2-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="66be2-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span><span class="sxs-lookup"><span data-stu-id="66be2-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="66be2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66be2-117">PARAMETERS</span></span>

### <span data-ttu-id="66be2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66be2-118">-DefaultProfile</span></span>
<span data-ttu-id="66be2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66be2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66be2-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="66be2-120">-EndpointName</span></span>
<span data-ttu-id="66be2-121">Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="66be2-121">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66be2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66be2-122">-InputObject</span></span>
<span data-ttu-id="66be2-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="66be2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66be2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66be2-124">-ResourceGroupName</span></span>
<span data-ttu-id="66be2-125">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="66be2-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66be2-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="66be2-126">-ResourceName</span></span>
<span data-ttu-id="66be2-127">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="66be2-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66be2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66be2-128">-SubscriptionId</span></span>
<span data-ttu-id="66be2-129">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="66be2-129">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66be2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66be2-130">CommonParameters</span></span>
<span data-ttu-id="66be2-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66be2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66be2-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66be2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66be2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66be2-133">INPUTS</span></span>

### <span data-ttu-id="66be2-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="66be2-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="66be2-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66be2-135">OUTPUTS</span></span>

### <span data-ttu-id="66be2-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="66be2-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="66be2-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="66be2-137">NOTES</span></span>

<span data-ttu-id="66be2-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="66be2-138">ALIASES</span></span>

<span data-ttu-id="66be2-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="66be2-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66be2-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="66be2-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66be2-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66be2-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66be2-142">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="66be2-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66be2-143">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="66be2-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="66be2-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="66be2-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66be2-145">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="66be2-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="66be2-146">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="66be2-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="66be2-147">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="66be2-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="66be2-148">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="66be2-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="66be2-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66be2-149">RELATED LINKS</span></span>

