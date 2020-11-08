---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245229"
---
# <span data-ttu-id="e466c-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="e466c-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="e466c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e466c-102">SYNOPSIS</span></span>
<span data-ttu-id="e466c-103">Операция удаления службы.</span><span class="sxs-lookup"><span data-stu-id="e466c-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="e466c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e466c-104">SYNTAX</span></span>

### <span data-ttu-id="e466c-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e466c-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e466c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e466c-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e466c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e466c-107">DESCRIPTION</span></span>
<span data-ttu-id="e466c-108">Операция удаления службы.</span><span class="sxs-lookup"><span data-stu-id="e466c-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="e466c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e466c-109">EXAMPLES</span></span>

### <span data-ttu-id="e466c-110">Пример 1: удаление пружинной облачной службы по названию.</span><span class="sxs-lookup"><span data-stu-id="e466c-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="e466c-111">Удалить пружинную облачную службу по названию.</span><span class="sxs-lookup"><span data-stu-id="e466c-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="e466c-112">Пример 2: удаление пружинной облачной службы из канала.</span><span class="sxs-lookup"><span data-stu-id="e466c-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="e466c-113">Удалить пружинную облачную службу из канала.</span><span class="sxs-lookup"><span data-stu-id="e466c-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="e466c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e466c-114">PARAMETERS</span></span>

### <span data-ttu-id="e466c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e466c-115">-AsJob</span></span>
<span data-ttu-id="e466c-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e466c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e466c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e466c-117">-DefaultProfile</span></span>
<span data-ttu-id="e466c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e466c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e466c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e466c-119">-InputObject</span></span>
<span data-ttu-id="e466c-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e466c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e466c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e466c-121">-Name</span></span>
<span data-ttu-id="e466c-122">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="e466c-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e466c-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="e466c-123">-NoWait</span></span>
<span data-ttu-id="e466c-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="e466c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e466c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e466c-125">-PassThru</span></span>
<span data-ttu-id="e466c-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e466c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e466c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e466c-127">-ResourceGroupName</span></span>
<span data-ttu-id="e466c-128">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="e466c-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e466c-129">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e466c-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e466c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e466c-130">-SubscriptionId</span></span>
<span data-ttu-id="e466c-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e466c-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e466c-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e466c-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e466c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e466c-133">-Confirm</span></span>
<span data-ttu-id="e466c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e466c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e466c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e466c-135">-WhatIf</span></span>
<span data-ttu-id="e466c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e466c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e466c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e466c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e466c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e466c-138">CommonParameters</span></span>
<span data-ttu-id="e466c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e466c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e466c-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e466c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e466c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e466c-141">INPUTS</span></span>

### <span data-ttu-id="e466c-142">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e466c-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e466c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e466c-143">OUTPUTS</span></span>

### <span data-ttu-id="e466c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e466c-144">System.Boolean</span></span>

## <span data-ttu-id="e466c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e466c-145">NOTES</span></span>

<span data-ttu-id="e466c-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e466c-146">ALIASES</span></span>

<span data-ttu-id="e466c-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e466c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e466c-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e466c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e466c-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e466c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e466c-150">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e466c-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e466c-151">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="e466c-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e466c-152">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="e466c-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e466c-153">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="e466c-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e466c-154">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="e466c-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e466c-155">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="e466c-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e466c-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e466c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e466c-157">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="e466c-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e466c-158">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="e466c-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e466c-159">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e466c-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e466c-160">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="e466c-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e466c-161">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e466c-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e466c-162">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e466c-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e466c-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e466c-163">RELATED LINKS</span></span>

