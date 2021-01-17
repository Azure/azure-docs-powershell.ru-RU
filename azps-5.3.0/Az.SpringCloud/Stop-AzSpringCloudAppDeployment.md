---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419740"
---
# <span data-ttu-id="9f797-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="9f797-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="9f797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f797-102">SYNOPSIS</span></span>
<span data-ttu-id="9f797-103">Остановите развертывание.</span><span class="sxs-lookup"><span data-stu-id="9f797-103">Stop the deployment.</span></span>

## <span data-ttu-id="9f797-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f797-104">SYNTAX</span></span>

### <span data-ttu-id="9f797-105">Остановка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f797-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9f797-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f797-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f797-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f797-107">DESCRIPTION</span></span>
<span data-ttu-id="9f797-108">Остановите развертывание.</span><span class="sxs-lookup"><span data-stu-id="9f797-108">Stop the deployment.</span></span>

## <span data-ttu-id="9f797-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f797-109">EXAMPLES</span></span>

### <span data-ttu-id="9f797-110">Пример 1. Остановка службы "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="9f797-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="9f797-111">Остановка службы "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="9f797-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="9f797-112">Пример 2. Остановка службы "Весенние облачные службы" из трубы.</span><span class="sxs-lookup"><span data-stu-id="9f797-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="9f797-113">Остановка службы "Весенние облачные службы" из трубы.</span><span class="sxs-lookup"><span data-stu-id="9f797-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="9f797-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f797-114">PARAMETERS</span></span>

### <span data-ttu-id="9f797-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="9f797-115">-AppName</span></span>
<span data-ttu-id="9f797-116">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="9f797-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f797-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f797-117">-AsJob</span></span>
<span data-ttu-id="9f797-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9f797-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9f797-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f797-119">-DefaultProfile</span></span>
<span data-ttu-id="9f797-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f797-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f797-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f797-121">-InputObject</span></span>
<span data-ttu-id="9f797-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9f797-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f797-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9f797-123">-Name</span></span>
<span data-ttu-id="9f797-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="9f797-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f797-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f797-125">-NoWait</span></span>
<span data-ttu-id="9f797-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9f797-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f797-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f797-127">-PassThru</span></span>
<span data-ttu-id="9f797-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="9f797-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9f797-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f797-129">-ResourceGroupName</span></span>
<span data-ttu-id="9f797-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="9f797-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9f797-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="9f797-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f797-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9f797-132">-ServiceName</span></span>
<span data-ttu-id="9f797-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="9f797-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f797-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f797-134">-SubscriptionId</span></span>
<span data-ttu-id="9f797-135">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f797-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f797-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9f797-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f797-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f797-137">-Confirm</span></span>
<span data-ttu-id="9f797-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f797-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f797-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f797-139">-WhatIf</span></span>
<span data-ttu-id="9f797-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f797-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f797-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f797-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f797-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f797-142">CommonParameters</span></span>
<span data-ttu-id="9f797-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f797-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f797-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f797-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f797-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f797-145">INPUTS</span></span>

### <span data-ttu-id="9f797-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="9f797-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="9f797-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f797-147">OUTPUTS</span></span>

### <span data-ttu-id="9f797-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f797-148">System.Boolean</span></span>

## <span data-ttu-id="9f797-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f797-149">NOTES</span></span>

<span data-ttu-id="9f797-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9f797-150">ALIASES</span></span>

<span data-ttu-id="9f797-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9f797-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f797-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9f797-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f797-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f797-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f797-154">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9f797-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f797-155">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="9f797-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="9f797-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="9f797-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="9f797-157">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="9f797-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="9f797-158">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="9f797-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="9f797-159">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="9f797-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="9f797-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9f797-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f797-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="9f797-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="9f797-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="9f797-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9f797-163">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="9f797-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9f797-164">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="9f797-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="9f797-165">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f797-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="9f797-166">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9f797-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9f797-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f797-167">RELATED LINKS</span></span>

