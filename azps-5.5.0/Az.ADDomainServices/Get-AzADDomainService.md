---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: ec52bea37eed3bb785da80beb8dfba02d0a426cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210673"
---
# <span data-ttu-id="a7e63-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="a7e63-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="a7e63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e63-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e63-103">Операция get Domain Service (Получить доменную службу) извлекает json-представление службы домена.</span><span class="sxs-lookup"><span data-stu-id="a7e63-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="a7e63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7e63-104">SYNTAX</span></span>

### <span data-ttu-id="a7e63-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7e63-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7e63-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a7e63-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7e63-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e63-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7e63-108">List1</span><span class="sxs-lookup"><span data-stu-id="a7e63-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e63-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7e63-109">DESCRIPTION</span></span>
<span data-ttu-id="a7e63-110">Операция get Domain Service (Получить доменную службу) извлекает json-представление службы домена.</span><span class="sxs-lookup"><span data-stu-id="a7e63-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="a7e63-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7e63-111">EXAMPLES</span></span>

### <span data-ttu-id="a7e63-112">Пример 1. Получить все ADDomainService по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a7e63-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a7e63-113">Получить все ADDomainService по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a7e63-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="a7e63-114">Пример 2. Получить ADDomainService по группе ресурсов и имени</span><span class="sxs-lookup"><span data-stu-id="a7e63-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a7e63-115">Получить ADDomainService по группе ресурсов и имени</span><span class="sxs-lookup"><span data-stu-id="a7e63-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="a7e63-116">Пример 3. Получить все ADDomainService по resourceGroup</span><span class="sxs-lookup"><span data-stu-id="a7e63-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a7e63-117">Получить все ADDomainService по resourceGroup</span><span class="sxs-lookup"><span data-stu-id="a7e63-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="a7e63-118">Пример 4. Получить ADDomainService по InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e63-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a7e63-119">Получить ADDomainService by InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e63-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="a7e63-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7e63-120">PARAMETERS</span></span>

### <span data-ttu-id="a7e63-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e63-121">-DefaultProfile</span></span>
<span data-ttu-id="a7e63-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e63-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7e63-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e63-123">-InputObject</span></span>
<span data-ttu-id="a7e63-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a7e63-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e63-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a7e63-125">-Name</span></span>
<span data-ttu-id="a7e63-126">Имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="a7e63-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e63-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7e63-128">Имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7e63-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="a7e63-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a7e63-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a7e63-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7e63-130">-SubscriptionId</span></span>
<span data-ttu-id="a7e63-131">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e63-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a7e63-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a7e63-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a7e63-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e63-133">CommonParameters</span></span>
<span data-ttu-id="a7e63-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e63-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e63-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7e63-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e63-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7e63-136">INPUTS</span></span>

### <span data-ttu-id="a7e63-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e63-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="a7e63-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7e63-138">OUTPUTS</span></span>

### <span data-ttu-id="a7e63-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="a7e63-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="a7e63-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7e63-140">NOTES</span></span>

<span data-ttu-id="a7e63-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a7e63-141">ALIASES</span></span>

<span data-ttu-id="a7e63-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a7e63-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7e63-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a7e63-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7e63-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7e63-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7e63-145">INPUTOBJECT <IAdDomainServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a7e63-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7e63-146">`[DomainServiceName <String>]`: имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="a7e63-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="a7e63-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a7e63-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7e63-148">`[ResourceGroupName <String>]`: имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7e63-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="a7e63-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a7e63-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="a7e63-150">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e63-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a7e63-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a7e63-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a7e63-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7e63-152">RELATED LINKS</span></span>

