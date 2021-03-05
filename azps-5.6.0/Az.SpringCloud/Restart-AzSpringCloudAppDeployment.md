---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/restart-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
ms.openlocfilehash: fd4d35991364f533eb1a311cc8aac0ce25e1ae17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986401"
---
# <span data-ttu-id="1e68c-101">Restart-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="1e68c-101">Restart-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="1e68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e68c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e68c-103">Перезапустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="1e68c-103">Restart the deployment.</span></span>

## <span data-ttu-id="1e68c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e68c-104">SYNTAX</span></span>

### <span data-ttu-id="1e68c-105">Перезапуск (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e68c-105">Restart (Default)</span></span>
```
Restart-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e68c-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1e68c-106">RestartViaIdentity</span></span>
```
Restart-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e68c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e68c-107">DESCRIPTION</span></span>
<span data-ttu-id="1e68c-108">Перезапустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="1e68c-108">Restart the deployment.</span></span>

## <span data-ttu-id="1e68c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e68c-109">EXAMPLES</span></span>

### <span data-ttu-id="1e68c-110">Пример 1. Перезапустите службу "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="1e68c-110">Example 1: Restart Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Restart-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="1e68c-111">Перезапустите весеннюю облачную службу по имени.</span><span class="sxs-lookup"><span data-stu-id="1e68c-111">Restart Spring Cloud Service by name.</span></span>

### <span data-ttu-id="1e68c-112">Пример 2. Перезапустите службу "Весенние облака" из трубы.</span><span class="sxs-lookup"><span data-stu-id="1e68c-112">Example 2: Restart Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Restart-AzSpringCloud
```

<span data-ttu-id="1e68c-113">Перезапустите службу "Весенние облачные службы" с трубы.</span><span class="sxs-lookup"><span data-stu-id="1e68c-113">Restart Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="1e68c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e68c-114">PARAMETERS</span></span>

### <span data-ttu-id="1e68c-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="1e68c-115">-AppName</span></span>
<span data-ttu-id="1e68c-116">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="1e68c-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e68c-117">-AsJob</span></span>
<span data-ttu-id="1e68c-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1e68c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1e68c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e68c-119">-DefaultProfile</span></span>
<span data-ttu-id="1e68c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e68c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e68c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e68c-121">-InputObject</span></span>
<span data-ttu-id="1e68c-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1e68c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1e68c-123">-Name</span></span>
<span data-ttu-id="1e68c-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="1e68c-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1e68c-125">-NoWait</span></span>
<span data-ttu-id="1e68c-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="1e68c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1e68c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e68c-127">-PassThru</span></span>
<span data-ttu-id="1e68c-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="1e68c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1e68c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e68c-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e68c-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="1e68c-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1e68c-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="1e68c-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1e68c-132">-ServiceName</span></span>
<span data-ttu-id="1e68c-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="1e68c-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e68c-134">-SubscriptionId</span></span>
<span data-ttu-id="1e68c-135">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1e68c-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e68c-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1e68c-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e68c-137">-Confirm</span></span>
<span data-ttu-id="1e68c-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1e68c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e68c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e68c-139">-WhatIf</span></span>
<span data-ttu-id="1e68c-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e68c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e68c-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1e68c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e68c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e68c-142">CommonParameters</span></span>
<span data-ttu-id="1e68c-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e68c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e68c-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e68c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e68c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e68c-145">INPUTS</span></span>

### <span data-ttu-id="1e68c-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="1e68c-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="1e68c-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e68c-147">OUTPUTS</span></span>

### <span data-ttu-id="1e68c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e68c-148">System.Boolean</span></span>

## <span data-ttu-id="1e68c-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e68c-149">NOTES</span></span>

<span data-ttu-id="1e68c-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1e68c-150">ALIASES</span></span>

<span data-ttu-id="1e68c-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1e68c-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e68c-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1e68c-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e68c-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1e68c-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e68c-154">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1e68c-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e68c-155">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="1e68c-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="1e68c-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="1e68c-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="1e68c-157">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="1e68c-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="1e68c-158">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="1e68c-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="1e68c-159">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="1e68c-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="1e68c-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1e68c-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e68c-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="1e68c-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="1e68c-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="1e68c-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1e68c-163">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="1e68c-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1e68c-164">`[ServiceName <String>]`: Название ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="1e68c-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="1e68c-165">`[SubscriptionId <String>]`: получает ИД подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1e68c-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1e68c-166">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1e68c-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1e68c-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e68c-167">RELATED LINKS</span></span>

