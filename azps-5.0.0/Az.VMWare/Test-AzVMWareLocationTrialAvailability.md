---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318758"
---
# <span data-ttu-id="c0644-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="c0644-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="c0644-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0644-102">SYNOPSIS</span></span>
<span data-ttu-id="c0644-103">Возврат пробного состояния подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="c0644-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="c0644-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0644-104">SYNTAX</span></span>

### <span data-ttu-id="c0644-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0644-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0644-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c0644-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0644-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0644-107">DESCRIPTION</span></span>
<span data-ttu-id="c0644-108">Возврат пробного состояния подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="c0644-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="c0644-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0644-109">EXAMPLES</span></span>

### <span data-ttu-id="c0644-110">Пример 1: Проверка доступности пробной версии</span><span class="sxs-lookup"><span data-stu-id="c0644-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="c0644-111">Проверка доступности пробной версии</span><span class="sxs-lookup"><span data-stu-id="c0644-111">Check trial availability</span></span>

## <span data-ttu-id="c0644-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0644-112">PARAMETERS</span></span>

### <span data-ttu-id="c0644-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0644-113">-DefaultProfile</span></span>
<span data-ttu-id="c0644-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0644-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0644-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0644-115">-InputObject</span></span>
<span data-ttu-id="c0644-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c0644-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0644-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c0644-117">-Location</span></span>
<span data-ttu-id="c0644-118">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="c0644-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0644-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0644-119">-SubscriptionId</span></span>
<span data-ttu-id="c0644-120">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c0644-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0644-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0644-121">-Confirm</span></span>
<span data-ttu-id="c0644-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0644-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0644-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0644-123">-WhatIf</span></span>
<span data-ttu-id="c0644-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0644-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0644-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0644-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0644-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0644-126">CommonParameters</span></span>
<span data-ttu-id="c0644-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0644-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0644-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0644-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0644-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0644-129">INPUTS</span></span>

### <span data-ttu-id="c0644-130">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="c0644-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="c0644-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0644-131">OUTPUTS</span></span>

### <span data-ttu-id="c0644-132">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. ITrial</span><span class="sxs-lookup"><span data-stu-id="c0644-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="c0644-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0644-133">NOTES</span></span>

<span data-ttu-id="c0644-134">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c0644-134">ALIASES</span></span>

<span data-ttu-id="c0644-135">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c0644-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0644-136">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0644-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0644-137">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c0644-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0644-138">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c0644-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c0644-139">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="c0644-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="c0644-140">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="c0644-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="c0644-141">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="c0644-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="c0644-142">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c0644-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0644-143">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="c0644-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="c0644-144">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="c0644-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="c0644-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0644-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c0644-146">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c0644-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="c0644-147">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c0644-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="c0644-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0644-148">RELATED LINKS</span></span>

