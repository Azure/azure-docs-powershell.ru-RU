---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393007"
---
# <span data-ttu-id="36076-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="36076-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="36076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36076-102">SYNOPSIS</span></span>
<span data-ttu-id="36076-103">Удаление авторизации каналов ExpressRoute в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="36076-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="36076-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36076-104">SYNTAX</span></span>

### <span data-ttu-id="36076-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36076-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="36076-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36076-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36076-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36076-107">DESCRIPTION</span></span>
<span data-ttu-id="36076-108">Удаление авторизации каналов ExpressRoute в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="36076-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="36076-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36076-109">EXAMPLES</span></span>

### <span data-ttu-id="36076-110">Пример 1. Удаление авторизации для закрытого облака</span><span class="sxs-lookup"><span data-stu-id="36076-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="36076-111">Удаление авторизации для закрытого облака</span><span class="sxs-lookup"><span data-stu-id="36076-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="36076-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36076-112">PARAMETERS</span></span>

### <span data-ttu-id="36076-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36076-113">-AsJob</span></span>
<span data-ttu-id="36076-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="36076-114">Run the command as a job</span></span>

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

### <span data-ttu-id="36076-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36076-115">-DefaultProfile</span></span>
<span data-ttu-id="36076-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36076-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36076-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36076-117">-InputObject</span></span>
<span data-ttu-id="36076-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="36076-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36076-119">-Name</span><span class="sxs-lookup"><span data-stu-id="36076-119">-Name</span></span>
<span data-ttu-id="36076-120">Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36076-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="36076-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="36076-121">-NoWait</span></span>
<span data-ttu-id="36076-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="36076-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="36076-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36076-123">-PassThru</span></span>
<span data-ttu-id="36076-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="36076-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="36076-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="36076-125">-PrivateCloudName</span></span>
<span data-ttu-id="36076-126">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="36076-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="36076-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36076-127">-ResourceGroupName</span></span>
<span data-ttu-id="36076-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36076-128">The name of the resource group.</span></span>
<span data-ttu-id="36076-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="36076-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36076-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36076-130">-SubscriptionId</span></span>
<span data-ttu-id="36076-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="36076-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36076-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36076-132">-Confirm</span></span>
<span data-ttu-id="36076-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="36076-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36076-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36076-134">-WhatIf</span></span>
<span data-ttu-id="36076-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36076-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36076-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36076-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36076-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36076-137">CommonParameters</span></span>
<span data-ttu-id="36076-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36076-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36076-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36076-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36076-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36076-140">INPUTS</span></span>

### <span data-ttu-id="36076-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="36076-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="36076-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36076-142">OUTPUTS</span></span>

### <span data-ttu-id="36076-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36076-143">System.Boolean</span></span>

## <span data-ttu-id="36076-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36076-144">NOTES</span></span>

<span data-ttu-id="36076-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="36076-145">ALIASES</span></span>

<span data-ttu-id="36076-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="36076-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36076-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="36076-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36076-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36076-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36076-149">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="36076-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36076-150">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36076-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="36076-151">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36076-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="36076-152">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36076-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="36076-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="36076-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36076-154">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="36076-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="36076-155">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="36076-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="36076-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36076-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="36076-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="36076-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="36076-158">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="36076-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="36076-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36076-159">RELATED LINKS</span></span>

