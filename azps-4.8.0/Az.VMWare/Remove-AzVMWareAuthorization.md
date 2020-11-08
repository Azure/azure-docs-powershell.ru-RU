---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236937"
---
# <span data-ttu-id="d676f-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="d676f-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="d676f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d676f-102">SYNOPSIS</span></span>
<span data-ttu-id="d676f-103">Удаление авторизации канала ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="d676f-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="d676f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d676f-104">SYNTAX</span></span>

### <span data-ttu-id="d676f-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d676f-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d676f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d676f-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d676f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d676f-107">DESCRIPTION</span></span>
<span data-ttu-id="d676f-108">Удаление авторизации канала ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="d676f-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="d676f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d676f-109">EXAMPLES</span></span>

### <span data-ttu-id="d676f-110">Пример 1: удаление авторизации для частного облака</span><span class="sxs-lookup"><span data-stu-id="d676f-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="d676f-111">Удаление авторизации для частного облака</span><span class="sxs-lookup"><span data-stu-id="d676f-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="d676f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d676f-112">PARAMETERS</span></span>

### <span data-ttu-id="d676f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d676f-113">-AsJob</span></span>
<span data-ttu-id="d676f-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d676f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d676f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d676f-115">-DefaultProfile</span></span>
<span data-ttu-id="d676f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d676f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d676f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d676f-117">-InputObject</span></span>
<span data-ttu-id="d676f-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d676f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d676f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d676f-119">-Name</span></span>
<span data-ttu-id="d676f-120">Имя авторизации канала ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="d676f-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d676f-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="d676f-121">-NoWait</span></span>
<span data-ttu-id="d676f-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d676f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d676f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d676f-123">-PassThru</span></span>
<span data-ttu-id="d676f-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d676f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d676f-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="d676f-125">-PrivateCloudName</span></span>
<span data-ttu-id="d676f-126">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="d676f-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="d676f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d676f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d676f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d676f-128">The name of the resource group.</span></span>
<span data-ttu-id="d676f-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d676f-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d676f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d676f-130">-SubscriptionId</span></span>
<span data-ttu-id="d676f-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d676f-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d676f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d676f-132">-Confirm</span></span>
<span data-ttu-id="d676f-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d676f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d676f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d676f-134">-WhatIf</span></span>
<span data-ttu-id="d676f-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d676f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d676f-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d676f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d676f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d676f-137">CommonParameters</span></span>
<span data-ttu-id="d676f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d676f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d676f-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d676f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d676f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d676f-140">INPUTS</span></span>

### <span data-ttu-id="d676f-141">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="d676f-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="d676f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d676f-142">OUTPUTS</span></span>

### <span data-ttu-id="d676f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d676f-143">System.Boolean</span></span>

## <span data-ttu-id="d676f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d676f-144">NOTES</span></span>

<span data-ttu-id="d676f-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d676f-145">ALIASES</span></span>

<span data-ttu-id="d676f-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d676f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d676f-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d676f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d676f-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d676f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d676f-149">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d676f-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d676f-150">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="d676f-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d676f-151">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="d676f-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d676f-152">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="d676f-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d676f-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d676f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d676f-154">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="d676f-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d676f-155">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="d676f-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d676f-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d676f-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d676f-157">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d676f-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="d676f-158">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d676f-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d676f-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d676f-159">RELATED LINKS</span></span>

