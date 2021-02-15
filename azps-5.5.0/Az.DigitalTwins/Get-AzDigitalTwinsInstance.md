---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237946"
---
# <span data-ttu-id="73301-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="73301-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="73301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73301-102">SYNOPSIS</span></span>
<span data-ttu-id="73301-103">Получить ресурс DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="73301-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="73301-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73301-104">SYNTAX</span></span>

### <span data-ttu-id="73301-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73301-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73301-106">Получить</span><span class="sxs-lookup"><span data-stu-id="73301-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73301-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73301-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="73301-108">Список1</span><span class="sxs-lookup"><span data-stu-id="73301-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="73301-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73301-109">DESCRIPTION</span></span>
<span data-ttu-id="73301-110">Получить ресурс DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="73301-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="73301-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73301-111">EXAMPLES</span></span>

### <span data-ttu-id="73301-112">Пример 1. Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73301-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="73301-113">Получить все DigitalTwinsInstance по умолчанию</span><span class="sxs-lookup"><span data-stu-id="73301-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="73301-114">Пример 2. Получить</span><span class="sxs-lookup"><span data-stu-id="73301-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="73301-115">Получить указанный AzDigitalTwinsInstance от ResourceName</span><span class="sxs-lookup"><span data-stu-id="73301-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="73301-116">Пример 3. GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73301-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="73301-117">Получить указанный AzDigitalTwinsInstance по объекту</span><span class="sxs-lookup"><span data-stu-id="73301-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="73301-118">Пример 4. Список1</span><span class="sxs-lookup"><span data-stu-id="73301-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="73301-119">Получить все DigitalTwinsInstance от ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73301-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="73301-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73301-120">PARAMETERS</span></span>

### <span data-ttu-id="73301-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73301-121">-DefaultProfile</span></span>
<span data-ttu-id="73301-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73301-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73301-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73301-123">-InputObject</span></span>
<span data-ttu-id="73301-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="73301-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73301-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73301-125">-ResourceGroupName</span></span>
<span data-ttu-id="73301-126">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73301-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73301-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="73301-127">-ResourceName</span></span>
<span data-ttu-id="73301-128">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73301-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="73301-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73301-129">-SubscriptionId</span></span>
<span data-ttu-id="73301-130">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="73301-130">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73301-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73301-131">CommonParameters</span></span>
<span data-ttu-id="73301-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73301-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73301-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73301-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73301-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73301-134">INPUTS</span></span>

### <span data-ttu-id="73301-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="73301-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="73301-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73301-136">OUTPUTS</span></span>

### <span data-ttu-id="73301-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="73301-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="73301-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73301-138">NOTES</span></span>

<span data-ttu-id="73301-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="73301-139">ALIASES</span></span>

<span data-ttu-id="73301-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="73301-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73301-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="73301-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73301-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73301-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73301-143">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="73301-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73301-144">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="73301-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="73301-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="73301-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73301-146">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73301-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="73301-147">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73301-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="73301-148">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73301-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="73301-149">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="73301-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="73301-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73301-150">RELATED LINKS</span></span>

