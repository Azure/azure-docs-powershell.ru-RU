---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419748"
---
# <span data-ttu-id="94257-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="94257-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="94257-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94257-102">SYNOPSIS</span></span>
<span data-ttu-id="94257-103">Запустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="94257-103">Start the deployment.</span></span>

## <span data-ttu-id="94257-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94257-104">SYNTAX</span></span>

### <span data-ttu-id="94257-105">Начало (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94257-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94257-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94257-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94257-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94257-107">DESCRIPTION</span></span>
<span data-ttu-id="94257-108">Запустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="94257-108">Start the deployment.</span></span>

## <span data-ttu-id="94257-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94257-109">EXAMPLES</span></span>

### <span data-ttu-id="94257-110">Пример 1. Запуск службы "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="94257-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="94257-111">Запустите службу "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="94257-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="94257-112">Пример 2. Запуск службы "Весенние облачные службы" из трубы.</span><span class="sxs-lookup"><span data-stu-id="94257-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="94257-113">Запустите службу "Весенние облачные службы" из трубы.</span><span class="sxs-lookup"><span data-stu-id="94257-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="94257-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94257-114">PARAMETERS</span></span>

### <span data-ttu-id="94257-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="94257-115">-AppName</span></span>
<span data-ttu-id="94257-116">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="94257-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94257-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94257-117">-AsJob</span></span>
<span data-ttu-id="94257-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="94257-118">Run the command as a job</span></span>

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

### <span data-ttu-id="94257-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94257-119">-DefaultProfile</span></span>
<span data-ttu-id="94257-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94257-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94257-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94257-121">-InputObject</span></span>
<span data-ttu-id="94257-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="94257-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94257-123">-Name</span><span class="sxs-lookup"><span data-stu-id="94257-123">-Name</span></span>
<span data-ttu-id="94257-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="94257-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94257-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="94257-125">-NoWait</span></span>
<span data-ttu-id="94257-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="94257-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94257-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94257-127">-PassThru</span></span>
<span data-ttu-id="94257-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="94257-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94257-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94257-129">-ResourceGroupName</span></span>
<span data-ttu-id="94257-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="94257-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="94257-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="94257-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94257-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="94257-132">-ServiceName</span></span>
<span data-ttu-id="94257-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="94257-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94257-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94257-134">-SubscriptionId</span></span>
<span data-ttu-id="94257-135">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94257-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="94257-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="94257-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94257-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94257-137">-Confirm</span></span>
<span data-ttu-id="94257-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="94257-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94257-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94257-139">-WhatIf</span></span>
<span data-ttu-id="94257-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94257-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94257-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94257-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94257-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94257-142">CommonParameters</span></span>
<span data-ttu-id="94257-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94257-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94257-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94257-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94257-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94257-145">INPUTS</span></span>

### <span data-ttu-id="94257-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="94257-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="94257-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94257-147">OUTPUTS</span></span>

### <span data-ttu-id="94257-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94257-148">System.Boolean</span></span>

## <span data-ttu-id="94257-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94257-149">NOTES</span></span>

<span data-ttu-id="94257-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="94257-150">ALIASES</span></span>

<span data-ttu-id="94257-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="94257-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94257-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="94257-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94257-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94257-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94257-154">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="94257-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94257-155">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="94257-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="94257-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="94257-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="94257-157">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="94257-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="94257-158">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="94257-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="94257-159">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="94257-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="94257-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="94257-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94257-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="94257-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="94257-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="94257-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="94257-163">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="94257-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="94257-164">`[ServiceName <String>]`: Название ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="94257-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="94257-165">`[SubscriptionId <String>]`: получает ИД подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94257-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="94257-166">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="94257-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94257-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94257-167">RELATED LINKS</span></span>

