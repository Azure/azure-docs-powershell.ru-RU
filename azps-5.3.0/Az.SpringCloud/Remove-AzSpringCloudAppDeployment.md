---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419756"
---
# <span data-ttu-id="7cbfb-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="7cbfb-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="7cbfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cbfb-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbfb-103">Операция удаления развертывания.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="7cbfb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7cbfb-104">SYNTAX</span></span>

### <span data-ttu-id="7cbfb-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7cbfb-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cbfb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7cbfb-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cbfb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cbfb-107">DESCRIPTION</span></span>
<span data-ttu-id="7cbfb-108">Операция удаления развертывания.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="7cbfb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7cbfb-109">EXAMPLES</span></span>

### <span data-ttu-id="7cbfb-110">Пример 1. Удаление названия службы "Весенние облачные развертывания".</span><span class="sxs-lookup"><span data-stu-id="7cbfb-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="7cbfb-111">Удалить по имени развертывание в облаке "Весенний".</span><span class="sxs-lookup"><span data-stu-id="7cbfb-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="7cbfb-112">Пример 2. Удаление источника "Весенние облачные развертывания" из трубы.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="7cbfb-113">Удалите весенние облачные развертывания из трубы.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="7cbfb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cbfb-114">PARAMETERS</span></span>

### <span data-ttu-id="7cbfb-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="7cbfb-115">-AppName</span></span>
<span data-ttu-id="7cbfb-116">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="7cbfb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cbfb-117">-AsJob</span></span>
<span data-ttu-id="7cbfb-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="7cbfb-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7cbfb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbfb-119">-DefaultProfile</span></span>
<span data-ttu-id="7cbfb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cbfb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cbfb-121">-InputObject</span></span>
<span data-ttu-id="7cbfb-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7cbfb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7cbfb-123">-Name</span></span>
<span data-ttu-id="7cbfb-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbfb-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7cbfb-125">-NoWait</span></span>
<span data-ttu-id="7cbfb-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="7cbfb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7cbfb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cbfb-127">-PassThru</span></span>
<span data-ttu-id="7cbfb-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7cbfb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbfb-129">-ResourceGroupName</span></span>
<span data-ttu-id="7cbfb-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7cbfb-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7cbfb-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7cbfb-132">-ServiceName</span></span>
<span data-ttu-id="7cbfb-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="7cbfb-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cbfb-134">-SubscriptionId</span></span>
<span data-ttu-id="7cbfb-135">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7cbfb-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7cbfb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cbfb-137">-Confirm</span></span>
<span data-ttu-id="7cbfb-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbfb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbfb-139">-WhatIf</span></span>
<span data-ttu-id="7cbfb-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbfb-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbfb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbfb-142">CommonParameters</span></span>
<span data-ttu-id="7cbfb-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbfb-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cbfb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbfb-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cbfb-145">INPUTS</span></span>

### <span data-ttu-id="7cbfb-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7cbfb-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7cbfb-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7cbfb-147">OUTPUTS</span></span>

### <span data-ttu-id="7cbfb-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7cbfb-148">System.Boolean</span></span>

## <span data-ttu-id="7cbfb-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7cbfb-149">NOTES</span></span>

<span data-ttu-id="7cbfb-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7cbfb-150">ALIASES</span></span>

<span data-ttu-id="7cbfb-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7cbfb-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cbfb-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cbfb-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cbfb-154">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="7cbfb-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7cbfb-155">`[AppName <String>]`: Название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7cbfb-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7cbfb-157">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7cbfb-158">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7cbfb-159">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7cbfb-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="7cbfb-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cbfb-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="7cbfb-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7cbfb-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7cbfb-163">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7cbfb-164">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7cbfb-165">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7cbfb-166">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="7cbfb-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7cbfb-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cbfb-167">RELATED LINKS</span></span>

