---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409212"
---
# <span data-ttu-id="b283c-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="b283c-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="b283c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b283c-102">SYNOPSIS</span></span>
<span data-ttu-id="b283c-103">Свойства монитора SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="b283c-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="b283c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b283c-104">SYNTAX</span></span>

### <span data-ttu-id="b283c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b283c-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b283c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b283c-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b283c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b283c-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b283c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b283c-108">DESCRIPTION</span></span>
<span data-ttu-id="b283c-109">Свойства монитора SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="b283c-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="b283c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b283c-110">EXAMPLES</span></span>

### <span data-ttu-id="b283c-111">Пример 1. По подписке все мониторы SAP</span><span class="sxs-lookup"><span data-stu-id="b283c-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b283c-112">Эта команда получает мониторы SAP в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="b283c-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="b283c-113">Пример 2. Получите монитор SAP по имени</span><span class="sxs-lookup"><span data-stu-id="b283c-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b283c-114">Эта команда получает монитор SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="b283c-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="b283c-115">Пример 3. Просмотр монитора SAP для объекта</span><span class="sxs-lookup"><span data-stu-id="b283c-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b283c-116">Эта команда получает монитор SAP по объекту.</span><span class="sxs-lookup"><span data-stu-id="b283c-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="b283c-117">Пример 4. Просмотр монитора SAP по конвейеру</span><span class="sxs-lookup"><span data-stu-id="b283c-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b283c-118">Эта команда получает монитор SAP в конвейере.</span><span class="sxs-lookup"><span data-stu-id="b283c-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="b283c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b283c-119">PARAMETERS</span></span>

### <span data-ttu-id="b283c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b283c-120">-DefaultProfile</span></span>
<span data-ttu-id="b283c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b283c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b283c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b283c-122">-InputObject</span></span>
<span data-ttu-id="b283c-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b283c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b283c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b283c-124">-Name</span></span>
<span data-ttu-id="b283c-125">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="b283c-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b283c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b283c-126">-ResourceGroupName</span></span>
<span data-ttu-id="b283c-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b283c-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b283c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b283c-128">-SubscriptionId</span></span>
<span data-ttu-id="b283c-129">Идентификация подписки, однозначно определяемая подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b283c-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b283c-130">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b283c-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b283c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b283c-131">CommonParameters</span></span>
<span data-ttu-id="b283c-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b283c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b283c-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b283c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b283c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b283c-134">INPUTS</span></span>

### <span data-ttu-id="b283c-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="b283c-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="b283c-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b283c-136">OUTPUTS</span></span>

### <span data-ttu-id="b283c-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="b283c-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="b283c-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b283c-138">NOTES</span></span>

<span data-ttu-id="b283c-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b283c-139">ALIASES</span></span>

<span data-ttu-id="b283c-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b283c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b283c-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b283c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b283c-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b283c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b283c-143">INPUTOBJECT <IHanaOnAzureIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b283c-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b283c-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b283c-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b283c-145">`[Location <String>]`: расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="b283c-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="b283c-146">`[OperationKind <AccessPolicyUpdateKind?>]`: название операции</span><span class="sxs-lookup"><span data-stu-id="b283c-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="b283c-147">`[ProviderInstanceName <String>]`: имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="b283c-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="b283c-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b283c-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b283c-149">`[ResourceName <String>]`: Имя ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="b283c-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="b283c-150">`[SapMonitorName <String>]`. Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="b283c-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="b283c-151">`[Scope <String>]`. Область поставщика ресурсов для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b283c-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="b283c-152">Родительский ресурс, который расширяется с помощью управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="b283c-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="b283c-153">`[SubscriptionId <String>]`: ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b283c-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b283c-154">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b283c-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b283c-155">`[VaultName <String>]`: имя сейфа</span><span class="sxs-lookup"><span data-stu-id="b283c-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="b283c-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b283c-156">RELATED LINKS</span></span>
