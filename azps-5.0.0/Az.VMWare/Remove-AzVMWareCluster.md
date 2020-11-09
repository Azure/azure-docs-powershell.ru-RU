---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316829"
---
# <span data-ttu-id="9f10c-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="9f10c-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="9f10c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f10c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f10c-103">Удаление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9f10c-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="9f10c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f10c-104">SYNTAX</span></span>

### <span data-ttu-id="9f10c-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f10c-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9f10c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f10c-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f10c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f10c-107">DESCRIPTION</span></span>
<span data-ttu-id="9f10c-108">Удаление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9f10c-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="9f10c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f10c-109">EXAMPLES</span></span>

### <span data-ttu-id="9f10c-110">Пример 1: Удаление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9f10c-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="9f10c-111">Удаление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9f10c-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="9f10c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f10c-112">PARAMETERS</span></span>

### <span data-ttu-id="9f10c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f10c-113">-AsJob</span></span>
<span data-ttu-id="9f10c-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9f10c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9f10c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f10c-115">-DefaultProfile</span></span>
<span data-ttu-id="9f10c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f10c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f10c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f10c-117">-InputObject</span></span>
<span data-ttu-id="9f10c-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9f10c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f10c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f10c-119">-Name</span></span>
<span data-ttu-id="9f10c-120">Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9f10c-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f10c-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="9f10c-121">-NoWait</span></span>
<span data-ttu-id="9f10c-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="9f10c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f10c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f10c-123">-PassThru</span></span>
<span data-ttu-id="9f10c-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9f10c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9f10c-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="9f10c-125">-PrivateCloudName</span></span>
<span data-ttu-id="9f10c-126">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="9f10c-126">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f10c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f10c-127">-ResourceGroupName</span></span>
<span data-ttu-id="9f10c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f10c-128">The name of the resource group.</span></span>
<span data-ttu-id="9f10c-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9f10c-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f10c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f10c-130">-SubscriptionId</span></span>
<span data-ttu-id="9f10c-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9f10c-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f10c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f10c-132">-Confirm</span></span>
<span data-ttu-id="9f10c-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f10c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f10c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f10c-134">-WhatIf</span></span>
<span data-ttu-id="9f10c-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f10c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f10c-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f10c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f10c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f10c-137">CommonParameters</span></span>
<span data-ttu-id="9f10c-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f10c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f10c-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f10c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f10c-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f10c-140">INPUTS</span></span>

### <span data-ttu-id="9f10c-141">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="9f10c-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="9f10c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f10c-142">OUTPUTS</span></span>

### <span data-ttu-id="9f10c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f10c-143">System.Boolean</span></span>

## <span data-ttu-id="9f10c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f10c-144">NOTES</span></span>

<span data-ttu-id="9f10c-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9f10c-145">ALIASES</span></span>

<span data-ttu-id="9f10c-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9f10c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f10c-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9f10c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f10c-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f10c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f10c-149">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9f10c-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f10c-150">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="9f10c-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9f10c-151">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9f10c-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9f10c-152">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9f10c-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9f10c-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9f10c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f10c-154">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="9f10c-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9f10c-155">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="9f10c-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9f10c-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f10c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9f10c-157">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9f10c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="9f10c-158">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9f10c-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9f10c-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f10c-159">RELATED LINKS</span></span>

