---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245225"
---
# <span data-ttu-id="55ddd-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="55ddd-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="55ddd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="55ddd-103">Остановите развертывание.</span><span class="sxs-lookup"><span data-stu-id="55ddd-103">Stop the deployment.</span></span>

## <span data-ttu-id="55ddd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55ddd-104">SYNTAX</span></span>

### <span data-ttu-id="55ddd-105">Остановить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55ddd-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55ddd-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55ddd-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55ddd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="55ddd-108">Остановите развертывание.</span><span class="sxs-lookup"><span data-stu-id="55ddd-108">Stop the deployment.</span></span>

## <span data-ttu-id="55ddd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55ddd-109">EXAMPLES</span></span>

### <span data-ttu-id="55ddd-110">Пример 1: остановка весны облачной службы по имени.</span><span class="sxs-lookup"><span data-stu-id="55ddd-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="55ddd-111">Остановите облачную службу весны по имени.</span><span class="sxs-lookup"><span data-stu-id="55ddd-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="55ddd-112">Пример 2: прекращение весны облачной службы из канала.</span><span class="sxs-lookup"><span data-stu-id="55ddd-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="55ddd-113">Остановите облачную службу весны из канала.</span><span class="sxs-lookup"><span data-stu-id="55ddd-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="55ddd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55ddd-114">PARAMETERS</span></span>

### <span data-ttu-id="55ddd-115">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="55ddd-115">-AppName</span></span>
<span data-ttu-id="55ddd-116">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="55ddd-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="55ddd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55ddd-117">-AsJob</span></span>
<span data-ttu-id="55ddd-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="55ddd-118">Run the command as a job</span></span>

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

### <span data-ttu-id="55ddd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ddd-119">-DefaultProfile</span></span>
<span data-ttu-id="55ddd-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55ddd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ddd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55ddd-121">-InputObject</span></span>
<span data-ttu-id="55ddd-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="55ddd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55ddd-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55ddd-123">-Name</span></span>
<span data-ttu-id="55ddd-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="55ddd-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="55ddd-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="55ddd-125">-NoWait</span></span>
<span data-ttu-id="55ddd-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="55ddd-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55ddd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55ddd-127">-PassThru</span></span>
<span data-ttu-id="55ddd-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="55ddd-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="55ddd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ddd-129">-ResourceGroupName</span></span>
<span data-ttu-id="55ddd-130">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="55ddd-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="55ddd-131">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="55ddd-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="55ddd-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="55ddd-132">-ServiceName</span></span>
<span data-ttu-id="55ddd-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="55ddd-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="55ddd-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55ddd-134">-SubscriptionId</span></span>
<span data-ttu-id="55ddd-135">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="55ddd-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="55ddd-136">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="55ddd-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="55ddd-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55ddd-137">-Confirm</span></span>
<span data-ttu-id="55ddd-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55ddd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ddd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ddd-139">-WhatIf</span></span>
<span data-ttu-id="55ddd-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55ddd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ddd-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55ddd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ddd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ddd-142">CommonParameters</span></span>
<span data-ttu-id="55ddd-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55ddd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ddd-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55ddd-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ddd-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55ddd-145">INPUTS</span></span>

### <span data-ttu-id="55ddd-146">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="55ddd-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="55ddd-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55ddd-147">OUTPUTS</span></span>

### <span data-ttu-id="55ddd-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55ddd-148">System.Boolean</span></span>

## <span data-ttu-id="55ddd-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="55ddd-149">NOTES</span></span>

<span data-ttu-id="55ddd-150">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="55ddd-150">ALIASES</span></span>

<span data-ttu-id="55ddd-151">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="55ddd-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55ddd-152">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="55ddd-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55ddd-153">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55ddd-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55ddd-154">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="55ddd-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55ddd-155">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="55ddd-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="55ddd-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="55ddd-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="55ddd-157">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="55ddd-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="55ddd-158">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="55ddd-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="55ddd-159">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="55ddd-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="55ddd-160">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="55ddd-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55ddd-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="55ddd-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="55ddd-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="55ddd-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="55ddd-163">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="55ddd-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="55ddd-164">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="55ddd-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="55ddd-165">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="55ddd-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="55ddd-166">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="55ddd-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="55ddd-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55ddd-167">RELATED LINKS</span></span>

