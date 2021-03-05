---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: 19ae45bf50c9ae54075e46a8db8fc66cc08e488a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997041"
---
# <span data-ttu-id="99df6-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="99df6-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="99df6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99df6-102">SYNOPSIS</span></span>
<span data-ttu-id="99df6-103">Операция get Domain Service (Получить доменную службу) извлекает json-представление службы домена.</span><span class="sxs-lookup"><span data-stu-id="99df6-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="99df6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99df6-104">SYNTAX</span></span>

### <span data-ttu-id="99df6-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99df6-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99df6-106">Получить</span><span class="sxs-lookup"><span data-stu-id="99df6-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99df6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99df6-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="99df6-108">Список1</span><span class="sxs-lookup"><span data-stu-id="99df6-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="99df6-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99df6-109">DESCRIPTION</span></span>
<span data-ttu-id="99df6-110">Операция get Domain Service (Получить доменную службу) извлекает json-представление службы домена.</span><span class="sxs-lookup"><span data-stu-id="99df6-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="99df6-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99df6-111">EXAMPLES</span></span>

### <span data-ttu-id="99df6-112">Пример 1. Получить все ADDomainService по умолчанию</span><span class="sxs-lookup"><span data-stu-id="99df6-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="99df6-113">Получить все ADDomainService по умолчанию</span><span class="sxs-lookup"><span data-stu-id="99df6-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="99df6-114">Пример 2. Получить ADDomainService по группе ресурсов и имени</span><span class="sxs-lookup"><span data-stu-id="99df6-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="99df6-115">Получить ADDomainService по группе ресурсов и имени</span><span class="sxs-lookup"><span data-stu-id="99df6-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="99df6-116">Пример 3. Получить все ADDomainService по resourceGroup</span><span class="sxs-lookup"><span data-stu-id="99df6-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="99df6-117">Получить все ADDomainService по resourceGroup</span><span class="sxs-lookup"><span data-stu-id="99df6-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="99df6-118">Пример 4. Получить ADDomainService по InputObject</span><span class="sxs-lookup"><span data-stu-id="99df6-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="99df6-119">Получить ADDomainService by InputObject</span><span class="sxs-lookup"><span data-stu-id="99df6-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="99df6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99df6-120">PARAMETERS</span></span>

### <span data-ttu-id="99df6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99df6-121">-DefaultProfile</span></span>
<span data-ttu-id="99df6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99df6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99df6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99df6-123">-InputObject</span></span>
<span data-ttu-id="99df6-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="99df6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99df6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="99df6-125">-Name</span></span>
<span data-ttu-id="99df6-126">Имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="99df6-126">The name of the domain service.</span></span>

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

### <span data-ttu-id="99df6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99df6-127">-ResourceGroupName</span></span>
<span data-ttu-id="99df6-128">Имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="99df6-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="99df6-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="99df6-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="99df6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99df6-130">-SubscriptionId</span></span>
<span data-ttu-id="99df6-131">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99df6-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="99df6-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="99df6-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99df6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99df6-133">CommonParameters</span></span>
<span data-ttu-id="99df6-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99df6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99df6-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99df6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99df6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99df6-136">INPUTS</span></span>

### <span data-ttu-id="99df6-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="99df6-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="99df6-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99df6-138">OUTPUTS</span></span>

### <span data-ttu-id="99df6-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="99df6-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="99df6-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99df6-140">NOTES</span></span>

<span data-ttu-id="99df6-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="99df6-141">ALIASES</span></span>

<span data-ttu-id="99df6-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="99df6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99df6-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="99df6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99df6-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99df6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99df6-145">INPUTOBJECT <IAdDomainServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="99df6-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99df6-146">`[DomainServiceName <String>]`: имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="99df6-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="99df6-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="99df6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99df6-148">`[ResourceGroupName <String>]`: имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="99df6-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="99df6-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="99df6-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="99df6-150">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99df6-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="99df6-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="99df6-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="99df6-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99df6-152">RELATED LINKS</span></span>

