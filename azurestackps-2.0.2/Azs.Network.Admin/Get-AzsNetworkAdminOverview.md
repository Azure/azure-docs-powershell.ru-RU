---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076968"
---
# <span data-ttu-id="92369-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="92369-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="92369-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92369-102">SYNOPSIS</span></span>
<span data-ttu-id="92369-103">Получите общие сведения о состоянии поставщика сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92369-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="92369-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92369-104">SYNTAX</span></span>

### <span data-ttu-id="92369-105">Get (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92369-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92369-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92369-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="92369-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92369-107">DESCRIPTION</span></span>
<span data-ttu-id="92369-108">Получите общие сведения о состоянии поставщика сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92369-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="92369-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92369-109">EXAMPLES</span></span>

### <span data-ttu-id="92369-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="92369-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="92369-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92369-111">PARAMETERS</span></span>

### <span data-ttu-id="92369-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92369-112">-DefaultProfile</span></span>
<span data-ttu-id="92369-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92369-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92369-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92369-114">-InputObject</span></span>
<span data-ttu-id="92369-115">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="92369-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="92369-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92369-116">-SubscriptionId</span></span>
<span data-ttu-id="92369-117">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92369-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="92369-118">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="92369-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92369-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92369-119">CommonParameters</span></span>
<span data-ttu-id="92369-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92369-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92369-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92369-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92369-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92369-122">INPUTS</span></span>

### <span data-ttu-id="92369-123">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="92369-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="92369-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92369-124">OUTPUTS</span></span>

### <span data-ttu-id="92369-125">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="92369-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="92369-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="92369-126">NOTES</span></span>

<span data-ttu-id="92369-127">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="92369-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92369-128">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92369-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="92369-129">INPUTOBJECT <INetworkAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="92369-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92369-130">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="92369-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92369-131">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="92369-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="92369-132">`[ResourceName <String>]`: Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="92369-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="92369-133">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92369-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="92369-134">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="92369-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="92369-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92369-135">RELATED LINKS</span></span>

