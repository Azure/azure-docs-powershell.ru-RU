---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 53127b970c3c2f588a54eaec3dcd9ea1174a7053
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991570"
---
# <span data-ttu-id="37c5a-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="37c5a-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="37c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="37c5a-103">Операция обновления существующей службы CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="37c5a-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="37c5a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37c5a-104">SYNTAX</span></span>

### <span data-ttu-id="37c5a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37c5a-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37c5a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37c5a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37c5a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37c5a-107">DESCRIPTION</span></span>
<span data-ttu-id="37c5a-108">Операция обновления существующей службы CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="37c5a-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="37c5a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37c5a-109">EXAMPLES</span></span>

### <span data-ttu-id="37c5a-110">Пример 1. Обновление существующего ресурса ACS с тегами</span><span class="sxs-lookup"><span data-stu-id="37c5a-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="37c5a-111">Прикрепит указанные теги к указанному ресурсу ACS.</span><span class="sxs-lookup"><span data-stu-id="37c5a-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="37c5a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37c5a-112">PARAMETERS</span></span>

### <span data-ttu-id="37c5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c5a-113">-DefaultProfile</span></span>
<span data-ttu-id="37c5a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37c5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c5a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37c5a-115">-InputObject</span></span>
<span data-ttu-id="37c5a-116">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="37c5a-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37c5a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="37c5a-117">-Name</span></span>
<span data-ttu-id="37c5a-118">Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="37c5a-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c5a-119">-ResourceGroupName</span></span>
<span data-ttu-id="37c5a-120">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="37c5a-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="37c5a-121">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="37c5a-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37c5a-122">-SubscriptionId</span></span>
<span data-ttu-id="37c5a-123">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37c5a-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="37c5a-124">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="37c5a-124">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="37c5a-125">-Tag</span></span>
<span data-ttu-id="37c5a-126">Теги службы, которые являются списком пар ключевых значений, которые описывают ресурс.</span><span class="sxs-lookup"><span data-stu-id="37c5a-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37c5a-127">-Confirm</span></span>
<span data-ttu-id="37c5a-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c5a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c5a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c5a-129">-WhatIf</span></span>
<span data-ttu-id="37c5a-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c5a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c5a-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="37c5a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c5a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c5a-132">CommonParameters</span></span>
<span data-ttu-id="37c5a-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c5a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c5a-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37c5a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c5a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37c5a-135">INPUTS</span></span>

### <span data-ttu-id="37c5a-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="37c5a-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="37c5a-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37c5a-137">OUTPUTS</span></span>

### <span data-ttu-id="37c5a-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="37c5a-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="37c5a-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37c5a-139">NOTES</span></span>

<span data-ttu-id="37c5a-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="37c5a-140">ALIASES</span></span>

<span data-ttu-id="37c5a-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="37c5a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37c5a-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="37c5a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37c5a-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37c5a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37c5a-144">INPUTOBJECT <ICommunicationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="37c5a-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37c5a-145">`[CommunicationServiceName <String>]`: Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="37c5a-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="37c5a-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="37c5a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37c5a-147">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="37c5a-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="37c5a-148">`[OperationId <String>]`: ID of an ongoing async operation</span><span class="sxs-lookup"><span data-stu-id="37c5a-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="37c5a-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="37c5a-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="37c5a-150">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="37c5a-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="37c5a-151">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37c5a-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="37c5a-152">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="37c5a-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="37c5a-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37c5a-153">RELATED LINKS</span></span>

