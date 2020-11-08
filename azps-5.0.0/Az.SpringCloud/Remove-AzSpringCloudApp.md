---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245227"
---
# <span data-ttu-id="cf4ca-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="cf4ca-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="cf4ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4ca-103">Операция удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-103">Operation to delete an App.</span></span>

## <span data-ttu-id="cf4ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf4ca-104">SYNTAX</span></span>

### <span data-ttu-id="cf4ca-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf4ca-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cf4ca-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf4ca-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf4ca-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf4ca-107">DESCRIPTION</span></span>
<span data-ttu-id="cf4ca-108">Операция удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-108">Operation to delete an App.</span></span>

## <span data-ttu-id="cf4ca-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf4ca-109">EXAMPLES</span></span>

### <span data-ttu-id="cf4ca-110">Пример 1: Удаление приложения с облаком пружины по названию.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="cf4ca-111">Удалить облачное приложение пружины по названию.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="cf4ca-112">Пример 2: удаление весны Cloud App из канала.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="cf4ca-113">Удалите приложение "пружинное облако" из канала.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="cf4ca-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf4ca-114">PARAMETERS</span></span>

### <span data-ttu-id="cf4ca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf4ca-115">-AsJob</span></span>
<span data-ttu-id="cf4ca-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="cf4ca-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cf4ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf4ca-117">-DefaultProfile</span></span>
<span data-ttu-id="cf4ca-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf4ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf4ca-119">-InputObject</span></span>
<span data-ttu-id="cf4ca-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf4ca-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf4ca-121">-Name</span></span>
<span data-ttu-id="cf4ca-122">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4ca-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="cf4ca-123">-NoWait</span></span>
<span data-ttu-id="cf4ca-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="cf4ca-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cf4ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf4ca-125">-PassThru</span></span>
<span data-ttu-id="cf4ca-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cf4ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf4ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf4ca-128">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cf4ca-129">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cf4ca-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cf4ca-130">-ServiceName</span></span>
<span data-ttu-id="cf4ca-131">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="cf4ca-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf4ca-132">-SubscriptionId</span></span>
<span data-ttu-id="cf4ca-133">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf4ca-134">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf4ca-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf4ca-135">-Confirm</span></span>
<span data-ttu-id="cf4ca-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf4ca-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf4ca-137">-WhatIf</span></span>
<span data-ttu-id="cf4ca-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf4ca-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf4ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4ca-140">CommonParameters</span></span>
<span data-ttu-id="cf4ca-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4ca-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf4ca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4ca-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf4ca-143">INPUTS</span></span>

### <span data-ttu-id="cf4ca-144">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="cf4ca-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="cf4ca-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf4ca-145">OUTPUTS</span></span>

### <span data-ttu-id="cf4ca-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf4ca-146">System.Boolean</span></span>

## <span data-ttu-id="cf4ca-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf4ca-147">NOTES</span></span>

<span data-ttu-id="cf4ca-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cf4ca-148">ALIASES</span></span>

<span data-ttu-id="cf4ca-149">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cf4ca-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf4ca-150">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf4ca-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf4ca-152">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="cf4ca-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf4ca-153">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="cf4ca-154">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="cf4ca-155">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="cf4ca-156">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="cf4ca-157">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="cf4ca-158">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="cf4ca-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf4ca-159">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="cf4ca-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="cf4ca-160">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cf4ca-161">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cf4ca-162">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="cf4ca-163">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cf4ca-164">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cf4ca-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cf4ca-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf4ca-165">RELATED LINKS</span></span>

