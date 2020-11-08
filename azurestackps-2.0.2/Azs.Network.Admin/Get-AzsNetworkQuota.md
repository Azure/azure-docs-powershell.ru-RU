---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077116"
---
# <span data-ttu-id="8570f-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="8570f-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="8570f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8570f-102">SYNOPSIS</span></span>
<span data-ttu-id="8570f-103">Получить квоту по имени.</span><span class="sxs-lookup"><span data-stu-id="8570f-103">Get a quota by name.</span></span>

## <span data-ttu-id="8570f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8570f-104">SYNTAX</span></span>

### <span data-ttu-id="8570f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8570f-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8570f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8570f-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8570f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8570f-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8570f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8570f-108">DESCRIPTION</span></span>
<span data-ttu-id="8570f-109">Список всех квот.</span><span class="sxs-lookup"><span data-stu-id="8570f-109">List all quotas.</span></span>
<span data-ttu-id="8570f-110">Ограничьте список, передав имя или фильтр.</span><span class="sxs-lookup"><span data-stu-id="8570f-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="8570f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8570f-111">EXAMPLES</span></span>

### <span data-ttu-id="8570f-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8570f-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="8570f-113">В этой статье перечислены все сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="8570f-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="8570f-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8570f-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="8570f-115">Получает указанную квоту сети.</span><span class="sxs-lookup"><span data-stu-id="8570f-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="8570f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8570f-116">PARAMETERS</span></span>

### <span data-ttu-id="8570f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8570f-117">-DefaultProfile</span></span>
<span data-ttu-id="8570f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8570f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8570f-119">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8570f-119">-Filter</span></span>
<span data-ttu-id="8570f-120">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="8570f-120">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8570f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8570f-121">-InputObject</span></span>
<span data-ttu-id="8570f-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="8570f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8570f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8570f-123">-Location</span></span>
<span data-ttu-id="8570f-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8570f-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8570f-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8570f-125">-Name</span></span>
<span data-ttu-id="8570f-126">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="8570f-126">Name of the resource.</span></span>

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

### <span data-ttu-id="8570f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8570f-127">-PassThru</span></span>
<span data-ttu-id="8570f-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8570f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8570f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8570f-129">-SubscriptionId</span></span>
<span data-ttu-id="8570f-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8570f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8570f-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8570f-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8570f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8570f-132">CommonParameters</span></span>
<span data-ttu-id="8570f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8570f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8570f-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8570f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8570f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8570f-135">INPUTS</span></span>

### <span data-ttu-id="8570f-136">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8570f-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="8570f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8570f-137">OUTPUTS</span></span>

### <span data-ttu-id="8570f-138">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="8570f-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="8570f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8570f-139">NOTES</span></span>

<span data-ttu-id="8570f-140">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8570f-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8570f-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8570f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8570f-142">INPUTOBJECT <INetworkAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="8570f-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8570f-143">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="8570f-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8570f-144">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8570f-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8570f-145">`[ResourceName <String>]`: Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="8570f-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="8570f-146">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8570f-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8570f-147">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8570f-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8570f-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8570f-148">RELATED LINKS</span></span>

