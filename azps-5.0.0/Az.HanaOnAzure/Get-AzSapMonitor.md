---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245347"
---
# <span data-ttu-id="109aa-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="109aa-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="109aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="109aa-102">SYNOPSIS</span></span>
<span data-ttu-id="109aa-103">Получение свойств монитора SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="109aa-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="109aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="109aa-104">SYNTAX</span></span>

### <span data-ttu-id="109aa-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="109aa-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="109aa-106">Получить</span><span class="sxs-lookup"><span data-stu-id="109aa-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="109aa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="109aa-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="109aa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="109aa-108">DESCRIPTION</span></span>
<span data-ttu-id="109aa-109">Получение свойств монитора SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="109aa-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="109aa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="109aa-110">EXAMPLES</span></span>

### <span data-ttu-id="109aa-111">Пример 1: получение всех мониторов SAP в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="109aa-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="109aa-112">Эта команда получает мониторы SAP в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="109aa-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="109aa-113">Пример 2: получение монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="109aa-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="109aa-114">Эта команда получает монитор SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="109aa-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="109aa-115">Пример 3: получение монитора SAP по объектам</span><span class="sxs-lookup"><span data-stu-id="109aa-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="109aa-116">Эта команда получает монитор SAP по объекту.</span><span class="sxs-lookup"><span data-stu-id="109aa-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="109aa-117">Пример 4: получение монитора SAP по каналу продаж</span><span class="sxs-lookup"><span data-stu-id="109aa-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="109aa-118">Эта команда получает монитор SAP по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="109aa-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="109aa-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="109aa-119">PARAMETERS</span></span>

### <span data-ttu-id="109aa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="109aa-120">-DefaultProfile</span></span>
<span data-ttu-id="109aa-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="109aa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="109aa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="109aa-122">-InputObject</span></span>
<span data-ttu-id="109aa-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="109aa-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="109aa-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="109aa-124">-Name</span></span>
<span data-ttu-id="109aa-125">Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="109aa-125">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="109aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="109aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="109aa-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="109aa-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="109aa-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="109aa-128">-SubscriptionId</span></span>
<span data-ttu-id="109aa-129">Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="109aa-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="109aa-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="109aa-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="109aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="109aa-131">CommonParameters</span></span>
<span data-ttu-id="109aa-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="109aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="109aa-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="109aa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="109aa-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="109aa-134">INPUTS</span></span>

### <span data-ttu-id="109aa-135">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="109aa-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="109aa-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="109aa-136">OUTPUTS</span></span>

### <span data-ttu-id="109aa-137">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="109aa-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="109aa-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="109aa-138">NOTES</span></span>

<span data-ttu-id="109aa-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="109aa-139">ALIASES</span></span>

<span data-ttu-id="109aa-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="109aa-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="109aa-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="109aa-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="109aa-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="109aa-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="109aa-143">INPUTOBJECT <IHanaOnAzureIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="109aa-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="109aa-144">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="109aa-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="109aa-145">`[Location <String>]`: Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="109aa-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="109aa-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Имя операции</span><span class="sxs-lookup"><span data-stu-id="109aa-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="109aa-147">`[ProviderInstanceName <String>]`: Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="109aa-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="109aa-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="109aa-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="109aa-149">`[ResourceName <String>]`: Имя ресурса идентификации.</span><span class="sxs-lookup"><span data-stu-id="109aa-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="109aa-150">`[SapMonitorName <String>]`: Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="109aa-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="109aa-151">`[Scope <String>]`: Область поставщика ресурсов ресурса.</span><span class="sxs-lookup"><span data-stu-id="109aa-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="109aa-152">Родительский ресурс, который расширяется управляемыми идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="109aa-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="109aa-153">`[SubscriptionId <String>]`: Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="109aa-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="109aa-154">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="109aa-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="109aa-155">`[VaultName <String>]`: Имя хранилища</span><span class="sxs-lookup"><span data-stu-id="109aa-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="109aa-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="109aa-156">RELATED LINKS</span></span>

