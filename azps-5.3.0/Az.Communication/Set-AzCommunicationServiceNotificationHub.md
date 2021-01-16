---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509277"
---
# <span data-ttu-id="a6156-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a6156-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="a6156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6156-102">SYNOPSIS</span></span>
<span data-ttu-id="a6156-103">Центр уведомлений Azure связывается с этой службой связи.</span><span class="sxs-lookup"><span data-stu-id="a6156-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="a6156-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6156-104">SYNTAX</span></span>

### <span data-ttu-id="a6156-105">LinkExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6156-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6156-106">Ссылка</span><span class="sxs-lookup"><span data-stu-id="a6156-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6156-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6156-107">DESCRIPTION</span></span>
<span data-ttu-id="a6156-108">Центр уведомлений Azure связывается с этой службой связи.</span><span class="sxs-lookup"><span data-stu-id="a6156-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="a6156-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6156-109">EXAMPLES</span></span>

### <span data-ttu-id="a6156-110">Пример 1. Интерактивное предоставление сведений из концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="a6156-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="a6156-111">Связанный центр уведомлений позволяет ресурсу ACS отправлять уведомления об определенных событиях.</span><span class="sxs-lookup"><span data-stu-id="a6156-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="a6156-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6156-112">PARAMETERS</span></span>

### <span data-ttu-id="a6156-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="a6156-113">-CommunicationServiceName</span></span>
<span data-ttu-id="a6156-114">Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a6156-114">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6156-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a6156-115">-ConnectionString</span></span>
<span data-ttu-id="a6156-116">Строка подключения для концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="a6156-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6156-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6156-117">-DefaultProfile</span></span>
<span data-ttu-id="a6156-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6156-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6156-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="a6156-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="a6156-120">Описание концентратора уведомлений Azure, связываемого со службой связи "Создать", см. раздел "ПРИМЕЧАНИЯ" для свойств LINKNOTIFICATIONHUBPARAMETER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a6156-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6156-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a6156-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="a6156-122">ИД ресурса в центре уведомлений</span><span class="sxs-lookup"><span data-stu-id="a6156-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6156-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6156-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6156-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="a6156-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a6156-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="a6156-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6156-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6156-126">-SubscriptionId</span></span>
<span data-ttu-id="a6156-127">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a6156-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6156-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a6156-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6156-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6156-129">-Confirm</span></span>
<span data-ttu-id="a6156-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a6156-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6156-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6156-131">-WhatIf</span></span>
<span data-ttu-id="a6156-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6156-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6156-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6156-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6156-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6156-134">CommonParameters</span></span>
<span data-ttu-id="a6156-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6156-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6156-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6156-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6156-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6156-137">INPUTS</span></span>

### <span data-ttu-id="a6156-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="a6156-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="a6156-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6156-139">OUTPUTS</span></span>

### <span data-ttu-id="a6156-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a6156-140">System.String</span></span>

## <span data-ttu-id="a6156-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6156-141">NOTES</span></span>

<span data-ttu-id="a6156-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a6156-142">ALIASES</span></span>

<span data-ttu-id="a6156-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a6156-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6156-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a6156-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6156-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6156-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6156-146">LINKNOTIFICATIONHUBPARAMETER: описание концентратора уведомлений Azure для ссылки <ILinkNotificationHubParameters> на службу связи</span><span class="sxs-lookup"><span data-stu-id="a6156-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="a6156-147">`ConnectionString <String>`: строка подключения для концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="a6156-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="a6156-148">`ResourceId <String>`: ИД ресурса в центре уведомлений</span><span class="sxs-lookup"><span data-stu-id="a6156-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="a6156-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6156-149">RELATED LINKS</span></span>

