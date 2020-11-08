---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243928"
---
# <span data-ttu-id="33d0b-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="33d0b-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="33d0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="33d0b-103">Операция удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="33d0b-103">Operation to delete an App.</span></span>

## <span data-ttu-id="33d0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33d0b-104">SYNTAX</span></span>

### <span data-ttu-id="33d0b-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33d0b-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="33d0b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="33d0b-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33d0b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33d0b-107">DESCRIPTION</span></span>
<span data-ttu-id="33d0b-108">Операция удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="33d0b-108">Operation to delete an App.</span></span>

## <span data-ttu-id="33d0b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33d0b-109">EXAMPLES</span></span>

### <span data-ttu-id="33d0b-110">Пример 1: Удаление приложения с облаком пружины по названию.</span><span class="sxs-lookup"><span data-stu-id="33d0b-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="33d0b-111">Удалить облачное приложение пружины по названию.</span><span class="sxs-lookup"><span data-stu-id="33d0b-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="33d0b-112">Пример 2: удаление весны Cloud App из канала.</span><span class="sxs-lookup"><span data-stu-id="33d0b-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="33d0b-113">Удалите приложение "пружинное облако" из канала.</span><span class="sxs-lookup"><span data-stu-id="33d0b-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="33d0b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33d0b-114">PARAMETERS</span></span>

### <span data-ttu-id="33d0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d0b-115">-DefaultProfile</span></span>
<span data-ttu-id="33d0b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33d0b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d0b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33d0b-117">-InputObject</span></span>
<span data-ttu-id="33d0b-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="33d0b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="33d0b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33d0b-119">-Name</span></span>
<span data-ttu-id="33d0b-120">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="33d0b-120">The name of the App resource.</span></span>

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

### <span data-ttu-id="33d0b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33d0b-121">-PassThru</span></span>
<span data-ttu-id="33d0b-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="33d0b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="33d0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d0b-123">-ResourceGroupName</span></span>
<span data-ttu-id="33d0b-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="33d0b-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="33d0b-125">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="33d0b-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="33d0b-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="33d0b-126">-ServiceName</span></span>
<span data-ttu-id="33d0b-127">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="33d0b-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="33d0b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33d0b-128">-SubscriptionId</span></span>
<span data-ttu-id="33d0b-129">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="33d0b-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="33d0b-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="33d0b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="33d0b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33d0b-131">-Confirm</span></span>
<span data-ttu-id="33d0b-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="33d0b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d0b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d0b-133">-WhatIf</span></span>
<span data-ttu-id="33d0b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="33d0b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33d0b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="33d0b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d0b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d0b-136">CommonParameters</span></span>
<span data-ttu-id="33d0b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33d0b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d0b-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33d0b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d0b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33d0b-139">INPUTS</span></span>

### <span data-ttu-id="33d0b-140">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="33d0b-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="33d0b-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33d0b-141">OUTPUTS</span></span>

### <span data-ttu-id="33d0b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33d0b-142">System.Boolean</span></span>

## <span data-ttu-id="33d0b-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="33d0b-143">NOTES</span></span>

<span data-ttu-id="33d0b-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="33d0b-144">ALIASES</span></span>

<span data-ttu-id="33d0b-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="33d0b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33d0b-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="33d0b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33d0b-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33d0b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33d0b-148">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="33d0b-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33d0b-149">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="33d0b-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="33d0b-150">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="33d0b-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="33d0b-151">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="33d0b-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="33d0b-152">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="33d0b-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="33d0b-153">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="33d0b-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="33d0b-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="33d0b-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33d0b-155">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="33d0b-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="33d0b-156">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="33d0b-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="33d0b-157">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="33d0b-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="33d0b-158">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="33d0b-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="33d0b-159">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="33d0b-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="33d0b-160">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="33d0b-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="33d0b-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33d0b-161">RELATED LINKS</span></span>

