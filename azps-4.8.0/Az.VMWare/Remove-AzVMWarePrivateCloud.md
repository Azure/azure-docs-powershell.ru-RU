---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236929"
---
# <span data-ttu-id="cbc49-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="cbc49-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="cbc49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbc49-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc49-103">Удаление частного облака</span><span class="sxs-lookup"><span data-stu-id="cbc49-103">Delete a private cloud</span></span>

## <span data-ttu-id="cbc49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbc49-104">SYNTAX</span></span>

### <span data-ttu-id="cbc49-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbc49-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cbc49-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cbc49-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cbc49-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbc49-107">DESCRIPTION</span></span>
<span data-ttu-id="cbc49-108">Удаление частного облака</span><span class="sxs-lookup"><span data-stu-id="cbc49-108">Delete a private cloud</span></span>

## <span data-ttu-id="cbc49-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbc49-109">EXAMPLES</span></span>

### <span data-ttu-id="cbc49-110">Пример 1: удаление частного облака</span><span class="sxs-lookup"><span data-stu-id="cbc49-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="cbc49-111">Удаление частного облака</span><span class="sxs-lookup"><span data-stu-id="cbc49-111">Delete private cloud</span></span>

## <span data-ttu-id="cbc49-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbc49-112">PARAMETERS</span></span>

### <span data-ttu-id="cbc49-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbc49-113">-AsJob</span></span>
<span data-ttu-id="cbc49-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="cbc49-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cbc49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc49-115">-DefaultProfile</span></span>
<span data-ttu-id="cbc49-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbc49-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbc49-117">-InputObject</span></span>
<span data-ttu-id="cbc49-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="cbc49-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbc49-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbc49-119">-Name</span></span>
<span data-ttu-id="cbc49-120">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="cbc49-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc49-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="cbc49-121">-NoWait</span></span>
<span data-ttu-id="cbc49-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="cbc49-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cbc49-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbc49-123">-PassThru</span></span>
<span data-ttu-id="cbc49-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cbc49-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cbc49-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc49-125">-ResourceGroupName</span></span>
<span data-ttu-id="cbc49-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbc49-126">The name of the resource group.</span></span>
<span data-ttu-id="cbc49-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="cbc49-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cbc49-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbc49-128">-SubscriptionId</span></span>
<span data-ttu-id="cbc49-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cbc49-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cbc49-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbc49-130">-Confirm</span></span>
<span data-ttu-id="cbc49-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbc49-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbc49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbc49-132">-WhatIf</span></span>
<span data-ttu-id="cbc49-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbc49-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbc49-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbc49-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbc49-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc49-135">CommonParameters</span></span>
<span data-ttu-id="cbc49-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbc49-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc49-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbc49-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc49-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbc49-138">INPUTS</span></span>

### <span data-ttu-id="cbc49-139">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="cbc49-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="cbc49-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbc49-140">OUTPUTS</span></span>

### <span data-ttu-id="cbc49-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbc49-141">System.Boolean</span></span>

## <span data-ttu-id="cbc49-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbc49-142">NOTES</span></span>

<span data-ttu-id="cbc49-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cbc49-143">ALIASES</span></span>

<span data-ttu-id="cbc49-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cbc49-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbc49-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cbc49-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbc49-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cbc49-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbc49-147">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="cbc49-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbc49-148">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="cbc49-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="cbc49-149">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="cbc49-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="cbc49-150">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="cbc49-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="cbc49-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="cbc49-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbc49-152">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="cbc49-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="cbc49-153">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="cbc49-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="cbc49-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbc49-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cbc49-155">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="cbc49-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="cbc49-156">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cbc49-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="cbc49-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbc49-157">RELATED LINKS</span></span>

