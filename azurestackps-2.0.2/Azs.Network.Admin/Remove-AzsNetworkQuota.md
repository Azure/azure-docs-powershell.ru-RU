---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076622"
---
# <span data-ttu-id="b04f7-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b04f7-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="b04f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b04f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b04f7-103">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b04f7-103">Delete a quota by name.</span></span>

## <span data-ttu-id="b04f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b04f7-104">SYNTAX</span></span>

### <span data-ttu-id="b04f7-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b04f7-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b04f7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b04f7-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b04f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b04f7-107">DESCRIPTION</span></span>
<span data-ttu-id="b04f7-108">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b04f7-108">Delete a quota by name.</span></span>

## <span data-ttu-id="b04f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b04f7-109">EXAMPLES</span></span>

### <span data-ttu-id="b04f7-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b04f7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="b04f7-111">Удаление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b04f7-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="b04f7-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b04f7-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="b04f7-113">Удалите сетевую квоту, используя канал.</span><span class="sxs-lookup"><span data-stu-id="b04f7-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="b04f7-114">--------------------------ПРИМЕР 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="b04f7-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="b04f7-115">Удалите сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="b04f7-115">Remove a network quota.</span></span>

## <span data-ttu-id="b04f7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b04f7-116">PARAMETERS</span></span>

### <span data-ttu-id="b04f7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b04f7-117">-AsJob</span></span>
<span data-ttu-id="b04f7-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b04f7-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b04f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04f7-119">-DefaultProfile</span></span>
<span data-ttu-id="b04f7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b04f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b04f7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b04f7-121">-InputObject</span></span>
<span data-ttu-id="b04f7-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="b04f7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b04f7-123">-Location</span><span class="sxs-lookup"><span data-stu-id="b04f7-123">-Location</span></span>
<span data-ttu-id="b04f7-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b04f7-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b04f7-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b04f7-125">-Name</span></span>
<span data-ttu-id="b04f7-126">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b04f7-126">Name of the resource.</span></span>

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

### <span data-ttu-id="b04f7-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="b04f7-127">-NoWait</span></span>
<span data-ttu-id="b04f7-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="b04f7-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b04f7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b04f7-129">-PassThru</span></span>
<span data-ttu-id="b04f7-130">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b04f7-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b04f7-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b04f7-131">-SubscriptionId</span></span>
<span data-ttu-id="b04f7-132">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b04f7-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b04f7-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b04f7-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b04f7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b04f7-134">-Confirm</span></span>
<span data-ttu-id="b04f7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b04f7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04f7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04f7-136">-WhatIf</span></span>
<span data-ttu-id="b04f7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b04f7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b04f7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b04f7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04f7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04f7-139">CommonParameters</span></span>
<span data-ttu-id="b04f7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b04f7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04f7-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b04f7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04f7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b04f7-142">INPUTS</span></span>

### <span data-ttu-id="b04f7-143">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b04f7-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="b04f7-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b04f7-144">OUTPUTS</span></span>

### <span data-ttu-id="b04f7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b04f7-145">System.Boolean</span></span>



## <span data-ttu-id="b04f7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b04f7-146">NOTES</span></span>

<span data-ttu-id="b04f7-147">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b04f7-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b04f7-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b04f7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b04f7-149">INPUTOBJECT <INetworkAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="b04f7-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b04f7-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="b04f7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b04f7-151">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b04f7-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b04f7-152">`[ResourceName <String>]`: Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b04f7-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="b04f7-153">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b04f7-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b04f7-154">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b04f7-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b04f7-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b04f7-155">RELATED LINKS</span></span>

