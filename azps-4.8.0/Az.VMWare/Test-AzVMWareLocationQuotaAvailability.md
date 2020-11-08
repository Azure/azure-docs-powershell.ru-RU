---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236928"
---
# <span data-ttu-id="ea499-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="ea499-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="ea499-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea499-102">SYNOPSIS</span></span>
<span data-ttu-id="ea499-103">Возврат квоты для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="ea499-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="ea499-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea499-104">SYNTAX</span></span>

### <span data-ttu-id="ea499-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea499-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea499-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ea499-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea499-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea499-107">DESCRIPTION</span></span>
<span data-ttu-id="ea499-108">Возврат квоты для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="ea499-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="ea499-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea499-109">EXAMPLES</span></span>

### <span data-ttu-id="ea499-110">Пример 1: Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="ea499-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="ea499-111">Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="ea499-111">Check quota availability</span></span>

## <span data-ttu-id="ea499-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea499-112">PARAMETERS</span></span>

### <span data-ttu-id="ea499-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea499-113">-DefaultProfile</span></span>
<span data-ttu-id="ea499-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea499-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea499-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea499-115">-InputObject</span></span>
<span data-ttu-id="ea499-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ea499-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ea499-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ea499-117">-Location</span></span>
<span data-ttu-id="ea499-118">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="ea499-118">Azure region</span></span>

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

### <span data-ttu-id="ea499-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea499-119">-SubscriptionId</span></span>
<span data-ttu-id="ea499-120">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ea499-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ea499-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea499-121">-Confirm</span></span>
<span data-ttu-id="ea499-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea499-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea499-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea499-123">-WhatIf</span></span>
<span data-ttu-id="ea499-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea499-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea499-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea499-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea499-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea499-126">CommonParameters</span></span>
<span data-ttu-id="ea499-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea499-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea499-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea499-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea499-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea499-129">INPUTS</span></span>

### <span data-ttu-id="ea499-130">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="ea499-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ea499-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea499-131">OUTPUTS</span></span>

### <span data-ttu-id="ea499-132">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="ea499-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="ea499-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea499-133">NOTES</span></span>

<span data-ttu-id="ea499-134">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ea499-134">ALIASES</span></span>

<span data-ttu-id="ea499-135">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ea499-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea499-136">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ea499-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea499-137">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea499-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea499-138">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="ea499-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea499-139">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="ea499-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ea499-140">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="ea499-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ea499-141">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="ea499-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ea499-142">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ea499-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea499-143">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="ea499-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ea499-144">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="ea499-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ea499-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea499-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ea499-146">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="ea499-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="ea499-147">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ea499-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ea499-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea499-148">RELATED LINKS</span></span>

