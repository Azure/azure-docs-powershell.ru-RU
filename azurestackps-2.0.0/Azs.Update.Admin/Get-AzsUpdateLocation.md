---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909301"
---
# <span data-ttu-id="fd308-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="fd308-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="fd308-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd308-102">SYNOPSIS</span></span>
<span data-ttu-id="fd308-103">Получение места для обновления на основе имени.</span><span class="sxs-lookup"><span data-stu-id="fd308-103">Get an update location based on name.</span></span>

## <span data-ttu-id="fd308-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd308-104">SYNTAX</span></span>

### <span data-ttu-id="fd308-105">Get (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd308-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd308-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd308-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd308-107">Список</span><span class="sxs-lookup"><span data-stu-id="fd308-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd308-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd308-108">DESCRIPTION</span></span>
<span data-ttu-id="fd308-109">Получение места для обновления на основе имени.</span><span class="sxs-lookup"><span data-stu-id="fd308-109">Get an update location based on name.</span></span>

## <span data-ttu-id="fd308-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd308-110">EXAMPLES</span></span>

### <span data-ttu-id="fd308-111">Пример 1: получение всех местоположений обновлений</span><span class="sxs-lookup"><span data-stu-id="fd308-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="fd308-112">При отсутствии каких бы то ни было параметров этот unifiedgroup будет получать все расположения для обновления.</span><span class="sxs-lookup"><span data-stu-id="fd308-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="fd308-113">Пример 2: получение всех местоположений обновлений по имени</span><span class="sxs-lookup"><span data-stu-id="fd308-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="fd308-114">Загружает все расположения обновлений, соответствующие указанному параметру имени.</span><span class="sxs-lookup"><span data-stu-id="fd308-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="fd308-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd308-115">PARAMETERS</span></span>

### <span data-ttu-id="fd308-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd308-116">-DefaultProfile</span></span>
<span data-ttu-id="fd308-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd308-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd308-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd308-118">-InputObject</span></span>
<span data-ttu-id="fd308-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fd308-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fd308-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd308-120">-Name</span></span>
<span data-ttu-id="fd308-121">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="fd308-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd308-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd308-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd308-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd308-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd308-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd308-124">-SubscriptionId</span></span>
<span data-ttu-id="fd308-125">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd308-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd308-126">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fd308-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd308-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd308-127">CommonParameters</span></span>
<span data-ttu-id="fd308-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd308-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd308-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd308-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd308-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd308-130">INPUTS</span></span>

### <span data-ttu-id="fd308-131">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fd308-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="fd308-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd308-132">OUTPUTS</span></span>

### <span data-ttu-id="fd308-133">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="fd308-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="fd308-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd308-134">NOTES</span></span>

<span data-ttu-id="fd308-135">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fd308-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd308-136">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd308-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fd308-137">INPUTOBJECT <IUpdateAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="fd308-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd308-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="fd308-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd308-139">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd308-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="fd308-140">`[RunName <String>]`: Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="fd308-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="fd308-141">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd308-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="fd308-142">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fd308-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fd308-143">`[UpdateLocation <String>]`: Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="fd308-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="fd308-144">`[UpdateName <String>]`: Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="fd308-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="fd308-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd308-145">RELATED LINKS</span></span>

