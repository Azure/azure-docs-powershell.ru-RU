---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: 3101ca2b120860dfa6df95786e235fc88fd0fc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519675"
---
# <span data-ttu-id="9ba69-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="9ba69-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="9ba69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba69-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba69-103">Получите службу CommunicationService и ее свойства.</span><span class="sxs-lookup"><span data-stu-id="9ba69-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="9ba69-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ba69-104">SYNTAX</span></span>

### <span data-ttu-id="9ba69-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ba69-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ba69-106">Получить</span><span class="sxs-lookup"><span data-stu-id="9ba69-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ba69-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ba69-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba69-108">Список1</span><span class="sxs-lookup"><span data-stu-id="9ba69-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9ba69-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ba69-109">DESCRIPTION</span></span>
<span data-ttu-id="9ba69-110">Получите службу CommunicationService и ее свойства.</span><span class="sxs-lookup"><span data-stu-id="9ba69-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="9ba69-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ba69-111">EXAMPLES</span></span>

### <span data-ttu-id="9ba69-112">Пример 1. Список существующих служб Связи для подписки</span><span class="sxs-lookup"><span data-stu-id="9ba69-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="9ba69-113">Возвращает список всех ресурсов ACS в рамках этой подписки.</span><span class="sxs-lookup"><span data-stu-id="9ba69-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="9ba69-114">Пример 2. Получить сведения о указанном информационном ресурсе Azure</span><span class="sxs-lookup"><span data-stu-id="9ba69-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="9ba69-115">Возвращает сведения о ресурсе ACS, если найден один совпадающий предоставленный параметр.</span><span class="sxs-lookup"><span data-stu-id="9ba69-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="9ba69-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ba69-116">PARAMETERS</span></span>

### <span data-ttu-id="9ba69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba69-117">-DefaultProfile</span></span>
<span data-ttu-id="9ba69-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ba69-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ba69-119">-InputObject</span></span>
<span data-ttu-id="9ba69-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9ba69-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba69-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9ba69-121">-Name</span></span>
<span data-ttu-id="9ba69-122">Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9ba69-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba69-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ba69-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="9ba69-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9ba69-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="9ba69-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba69-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ba69-126">-SubscriptionId</span></span>
<span data-ttu-id="9ba69-127">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba69-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9ba69-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9ba69-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba69-129">CommonParameters</span></span>
<span data-ttu-id="9ba69-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba69-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ba69-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba69-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ba69-132">INPUTS</span></span>

### <span data-ttu-id="9ba69-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="9ba69-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="9ba69-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ba69-134">OUTPUTS</span></span>

### <span data-ttu-id="9ba69-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="9ba69-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="9ba69-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ba69-136">NOTES</span></span>

<span data-ttu-id="9ba69-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9ba69-137">ALIASES</span></span>

<span data-ttu-id="9ba69-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9ba69-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ba69-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9ba69-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ba69-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ba69-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ba69-141">INPUTOBJECT <ICommunicationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9ba69-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ba69-142">`[CommunicationServiceName <String>]`: имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9ba69-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="9ba69-143">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9ba69-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ba69-144">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="9ba69-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="9ba69-145">`[OperationId <String>]`: ID of an ongoing async operation</span><span class="sxs-lookup"><span data-stu-id="9ba69-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="9ba69-146">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="9ba69-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9ba69-147">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="9ba69-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9ba69-148">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba69-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="9ba69-149">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9ba69-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9ba69-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ba69-150">RELATED LINKS</span></span>

