---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243439"
---
# <span data-ttu-id="6e6af-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="6e6af-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="6e6af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e6af-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6af-103">Получение частного облака</span><span class="sxs-lookup"><span data-stu-id="6e6af-103">Get a private cloud</span></span>

## <span data-ttu-id="6e6af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e6af-104">SYNTAX</span></span>

### <span data-ttu-id="6e6af-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e6af-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e6af-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6e6af-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e6af-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e6af-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e6af-108">Список</span><span class="sxs-lookup"><span data-stu-id="6e6af-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e6af-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e6af-109">DESCRIPTION</span></span>
<span data-ttu-id="6e6af-110">Получение частного облака</span><span class="sxs-lookup"><span data-stu-id="6e6af-110">Get a private cloud</span></span>

## <span data-ttu-id="6e6af-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e6af-111">EXAMPLES</span></span>

### <span data-ttu-id="6e6af-112">Пример 1: список Частное облако в подписке</span><span class="sxs-lookup"><span data-stu-id="6e6af-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="6e6af-113">Список частных облаков в подписке</span><span class="sxs-lookup"><span data-stu-id="6e6af-113">List private cloud under subscription</span></span>

### <span data-ttu-id="6e6af-114">Пример 2: список Частное облако в разделе "Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="6e6af-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="6e6af-115">Список Частное облако в разделе "Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="6e6af-115">List private cloud under resource group</span></span>

### <span data-ttu-id="6e6af-116">Пример 3: получение частного облака</span><span class="sxs-lookup"><span data-stu-id="6e6af-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="6e6af-117">Получить частное облако</span><span class="sxs-lookup"><span data-stu-id="6e6af-117">Get private cloud</span></span>

## <span data-ttu-id="6e6af-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e6af-118">PARAMETERS</span></span>

### <span data-ttu-id="6e6af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6af-119">-DefaultProfile</span></span>
<span data-ttu-id="6e6af-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e6af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e6af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e6af-121">-InputObject</span></span>
<span data-ttu-id="6e6af-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6e6af-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e6af-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e6af-123">-Name</span></span>
<span data-ttu-id="6e6af-124">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="6e6af-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e6af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e6af-125">-ResourceGroupName</span></span>
<span data-ttu-id="6e6af-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e6af-126">The name of the resource group.</span></span>
<span data-ttu-id="6e6af-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6e6af-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6e6af-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e6af-128">-SubscriptionId</span></span>
<span data-ttu-id="6e6af-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6e6af-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6e6af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6af-130">CommonParameters</span></span>
<span data-ttu-id="6e6af-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e6af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6af-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e6af-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6af-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e6af-133">INPUTS</span></span>

### <span data-ttu-id="6e6af-134">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="6e6af-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="6e6af-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e6af-135">OUTPUTS</span></span>

### <span data-ttu-id="6e6af-136">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="6e6af-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="6e6af-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e6af-137">NOTES</span></span>

<span data-ttu-id="6e6af-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6e6af-138">ALIASES</span></span>

<span data-ttu-id="6e6af-139">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6e6af-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e6af-140">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6e6af-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e6af-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6e6af-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e6af-142">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="6e6af-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e6af-143">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="6e6af-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="6e6af-144">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="6e6af-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="6e6af-145">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="6e6af-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="6e6af-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="6e6af-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e6af-147">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="6e6af-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="6e6af-148">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="6e6af-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="6e6af-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e6af-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6e6af-150">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6e6af-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="6e6af-151">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6e6af-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6e6af-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e6af-152">RELATED LINKS</span></span>

