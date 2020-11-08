---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075173"
---
# <span data-ttu-id="46bc8-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="46bc8-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="46bc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="46bc8-103">Получение определенного обновления на месте обновления.</span><span class="sxs-lookup"><span data-stu-id="46bc8-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="46bc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46bc8-104">SYNTAX</span></span>

### <span data-ttu-id="46bc8-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46bc8-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="46bc8-106">Получить</span><span class="sxs-lookup"><span data-stu-id="46bc8-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="46bc8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46bc8-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="46bc8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="46bc8-109">Получение определенного обновления на месте обновления.</span><span class="sxs-lookup"><span data-stu-id="46bc8-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="46bc8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="46bc8-111">Пример 1: получение всех обновлений</span><span class="sxs-lookup"><span data-stu-id="46bc8-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="46bc8-112">При отсутствии каких бы то ни было параметров, Get-AzsUpdate выведет список всех обновлений, которые могут быть обнаружены штампом</span><span class="sxs-lookup"><span data-stu-id="46bc8-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="46bc8-113">Пример 2: получение обновления по имени</span><span class="sxs-lookup"><span data-stu-id="46bc8-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="46bc8-114">Будет получать все обновления, соответствующие указанному имени.</span><span class="sxs-lookup"><span data-stu-id="46bc8-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="46bc8-115">Пример 3: получение всех обновлений по расположению</span><span class="sxs-lookup"><span data-stu-id="46bc8-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="46bc8-116">Будут извлечены все обновления в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="46bc8-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="46bc8-117">В настоящее время поддерживается только одно расположение, так что это эквивалентно Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="46bc8-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="46bc8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46bc8-118">PARAMETERS</span></span>

### <span data-ttu-id="46bc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bc8-119">-DefaultProfile</span></span>
<span data-ttu-id="46bc8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46bc8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46bc8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46bc8-121">-InputObject</span></span>
<span data-ttu-id="46bc8-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="46bc8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="46bc8-123">-Location</span><span class="sxs-lookup"><span data-stu-id="46bc8-123">-Location</span></span>
<span data-ttu-id="46bc8-124">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="46bc8-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46bc8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46bc8-125">-Name</span></span>
<span data-ttu-id="46bc8-126">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="46bc8-126">Name of the update.</span></span>

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

### <span data-ttu-id="46bc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46bc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="46bc8-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46bc8-128">Resource group name.</span></span>

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

### <span data-ttu-id="46bc8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46bc8-129">-SubscriptionId</span></span>
<span data-ttu-id="46bc8-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46bc8-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46bc8-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="46bc8-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="46bc8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bc8-132">CommonParameters</span></span>
<span data-ttu-id="46bc8-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46bc8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bc8-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46bc8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bc8-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46bc8-135">INPUTS</span></span>

### <span data-ttu-id="46bc8-136">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="46bc8-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="46bc8-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46bc8-137">OUTPUTS</span></span>

### <span data-ttu-id="46bc8-138">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. Api20160501. IUpdate</span><span class="sxs-lookup"><span data-stu-id="46bc8-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="46bc8-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="46bc8-139">NOTES</span></span>

<span data-ttu-id="46bc8-140">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="46bc8-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46bc8-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46bc8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="46bc8-142">INPUTOBJECT <IUpdateAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="46bc8-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46bc8-143">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="46bc8-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46bc8-144">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46bc8-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="46bc8-145">`[RunName <String>]`: Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="46bc8-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="46bc8-146">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46bc8-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="46bc8-147">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="46bc8-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="46bc8-148">`[UpdateLocation <String>]`: Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="46bc8-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="46bc8-149">`[UpdateName <String>]`: Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="46bc8-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="46bc8-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46bc8-150">RELATED LINKS</span></span>

