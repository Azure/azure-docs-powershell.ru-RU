---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 3e2bf7dc031f257849036a3482361f1647379795
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010168"
---
# <span data-ttu-id="c1f32-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="c1f32-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="c1f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1f32-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f32-103">Операция удаления службы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="c1f32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c1f32-104">SYNTAX</span></span>

### <span data-ttu-id="c1f32-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1f32-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1f32-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c1f32-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1f32-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1f32-107">DESCRIPTION</span></span>
<span data-ttu-id="c1f32-108">Операция удаления службы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="c1f32-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c1f32-109">EXAMPLES</span></span>

### <span data-ttu-id="c1f32-110">Пример 1. Удаление службы "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="c1f32-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="c1f32-111">Удалить службу "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="c1f32-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="c1f32-112">Пример 2. Удаление службы "Весенние облачные службы" из трубы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="c1f32-113">Удалите весенние облачные службы из трубы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="c1f32-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1f32-114">PARAMETERS</span></span>

### <span data-ttu-id="c1f32-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1f32-115">-AsJob</span></span>
<span data-ttu-id="c1f32-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c1f32-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c1f32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f32-117">-DefaultProfile</span></span>
<span data-ttu-id="c1f32-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f32-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1f32-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1f32-119">-InputObject</span></span>
<span data-ttu-id="c1f32-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c1f32-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c1f32-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1f32-121">-Name</span></span>
<span data-ttu-id="c1f32-122">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c1f32-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c1f32-123">-NoWait</span></span>
<span data-ttu-id="c1f32-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c1f32-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c1f32-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1f32-125">-PassThru</span></span>
<span data-ttu-id="c1f32-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="c1f32-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c1f32-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f32-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1f32-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="c1f32-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c1f32-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c1f32-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c1f32-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1f32-130">-SubscriptionId</span></span>
<span data-ttu-id="c1f32-131">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f32-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c1f32-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c1f32-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1f32-133">-Confirm</span></span>
<span data-ttu-id="c1f32-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c1f32-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1f32-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1f32-135">-WhatIf</span></span>
<span data-ttu-id="c1f32-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1f32-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1f32-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c1f32-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1f32-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f32-138">CommonParameters</span></span>
<span data-ttu-id="c1f32-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1f32-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f32-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1f32-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f32-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1f32-141">INPUTS</span></span>

### <span data-ttu-id="c1f32-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="c1f32-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="c1f32-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1f32-143">OUTPUTS</span></span>

### <span data-ttu-id="c1f32-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1f32-144">System.Boolean</span></span>

## <span data-ttu-id="c1f32-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c1f32-145">NOTES</span></span>

<span data-ttu-id="c1f32-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c1f32-146">ALIASES</span></span>

<span data-ttu-id="c1f32-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c1f32-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1f32-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c1f32-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1f32-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1f32-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1f32-150">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c1f32-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c1f32-151">`[AppName <String>]`: Название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="c1f32-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="c1f32-152">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="c1f32-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="c1f32-153">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="c1f32-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="c1f32-154">`[DeploymentName <String>]`: Название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="c1f32-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="c1f32-155">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="c1f32-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="c1f32-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c1f32-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c1f32-157">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="c1f32-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="c1f32-158">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="c1f32-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c1f32-159">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c1f32-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c1f32-160">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="c1f32-161">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f32-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c1f32-162">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c1f32-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c1f32-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1f32-163">RELATED LINKS</span></span>

