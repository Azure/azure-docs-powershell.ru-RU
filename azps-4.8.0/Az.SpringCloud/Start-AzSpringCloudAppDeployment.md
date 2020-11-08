---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243288"
---
# <span data-ttu-id="a4c10-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="a4c10-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="a4c10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4c10-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c10-103">Запустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="a4c10-103">Start the deployment.</span></span>

## <span data-ttu-id="a4c10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4c10-104">SYNTAX</span></span>

### <span data-ttu-id="a4c10-105">Начало (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4c10-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4c10-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4c10-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4c10-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c10-107">DESCRIPTION</span></span>
<span data-ttu-id="a4c10-108">Запустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="a4c10-108">Start the deployment.</span></span>

## <span data-ttu-id="a4c10-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4c10-109">EXAMPLES</span></span>

### <span data-ttu-id="a4c10-110">Пример 1: начало весны облачной службы по названию.</span><span class="sxs-lookup"><span data-stu-id="a4c10-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="a4c10-111">Начало весны облачной службы по названию.</span><span class="sxs-lookup"><span data-stu-id="a4c10-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="a4c10-112">Пример 2: начало весны облачной службы из канала.</span><span class="sxs-lookup"><span data-stu-id="a4c10-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="a4c10-113">Запустите облачную службу весны из канала.</span><span class="sxs-lookup"><span data-stu-id="a4c10-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="a4c10-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4c10-114">PARAMETERS</span></span>

### <span data-ttu-id="a4c10-115">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="a4c10-115">-AppName</span></span>
<span data-ttu-id="a4c10-116">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="a4c10-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="a4c10-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4c10-117">-AsJob</span></span>
<span data-ttu-id="a4c10-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a4c10-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a4c10-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c10-119">-DefaultProfile</span></span>
<span data-ttu-id="a4c10-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c10-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4c10-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4c10-121">-InputObject</span></span>
<span data-ttu-id="a4c10-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a4c10-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4c10-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4c10-123">-Name</span></span>
<span data-ttu-id="a4c10-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="a4c10-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="a4c10-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="a4c10-125">-NoWait</span></span>
<span data-ttu-id="a4c10-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a4c10-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a4c10-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4c10-127">-PassThru</span></span>
<span data-ttu-id="a4c10-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a4c10-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a4c10-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c10-129">-ResourceGroupName</span></span>
<span data-ttu-id="a4c10-130">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="a4c10-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a4c10-131">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="a4c10-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a4c10-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a4c10-132">-ServiceName</span></span>
<span data-ttu-id="a4c10-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="a4c10-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="a4c10-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4c10-134">-SubscriptionId</span></span>
<span data-ttu-id="a4c10-135">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c10-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4c10-136">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a4c10-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a4c10-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4c10-137">-Confirm</span></span>
<span data-ttu-id="a4c10-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4c10-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c10-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c10-139">-WhatIf</span></span>
<span data-ttu-id="a4c10-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4c10-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c10-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4c10-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c10-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c10-142">CommonParameters</span></span>
<span data-ttu-id="a4c10-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4c10-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c10-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4c10-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c10-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4c10-145">INPUTS</span></span>

### <span data-ttu-id="a4c10-146">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a4c10-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a4c10-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c10-147">OUTPUTS</span></span>

### <span data-ttu-id="a4c10-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4c10-148">System.Boolean</span></span>

## <span data-ttu-id="a4c10-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4c10-149">NOTES</span></span>

<span data-ttu-id="a4c10-150">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a4c10-150">ALIASES</span></span>

<span data-ttu-id="a4c10-151">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a4c10-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4c10-152">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a4c10-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4c10-153">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4c10-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4c10-154">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a4c10-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4c10-155">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="a4c10-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a4c10-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="a4c10-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a4c10-157">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4c10-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a4c10-158">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="a4c10-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a4c10-159">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="a4c10-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a4c10-160">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a4c10-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4c10-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="a4c10-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a4c10-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="a4c10-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a4c10-163">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="a4c10-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a4c10-164">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="a4c10-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a4c10-165">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c10-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a4c10-166">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a4c10-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a4c10-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4c10-167">RELATED LINKS</span></span>

