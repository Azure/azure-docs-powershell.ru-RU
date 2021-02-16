---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211865"
---
# <span data-ttu-id="61622-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="61622-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="61622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61622-102">SYNOPSIS</span></span>
<span data-ttu-id="61622-103">Повторное сгенерировать ключ доступа CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="61622-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="61622-104">PrimaryKey и SecondaryKey не могут быть повторно сгенерированы одновременно.</span><span class="sxs-lookup"><span data-stu-id="61622-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="61622-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61622-105">SYNTAX</span></span>

### <span data-ttu-id="61622-106">RegenerateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61622-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="61622-107">Повторно сгенерировать</span><span class="sxs-lookup"><span data-stu-id="61622-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="61622-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="61622-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="61622-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="61622-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="61622-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61622-110">DESCRIPTION</span></span>
<span data-ttu-id="61622-111">Повторное сгенерировать ключ доступа CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="61622-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="61622-112">PrimaryKey и SecondaryKey не могут быть повторно сгенерированы одновременно.</span><span class="sxs-lookup"><span data-stu-id="61622-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="61622-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61622-113">EXAMPLES</span></span>

### <span data-ttu-id="61622-114">Пример 1. Повторное сгенерирует первичный ключ с помощью hashtable IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="61622-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="61622-115">Недействительность предыдущего первичного ключа, повторное сгенерирует новый и возвращает его.</span><span class="sxs-lookup"><span data-stu-id="61622-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="61622-116">Пример 2. Повторное сгенерирует дополнительный ключ с помощью KeyType.</span><span class="sxs-lookup"><span data-stu-id="61622-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="61622-117">Недействительность предыдущего дополнительного ключа, повторное сгенерирует новый и возвращает его.</span><span class="sxs-lookup"><span data-stu-id="61622-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="61622-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61622-118">PARAMETERS</span></span>

### <span data-ttu-id="61622-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="61622-119">-CommunicationServiceName</span></span>
<span data-ttu-id="61622-120">Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="61622-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61622-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61622-121">-DefaultProfile</span></span>
<span data-ttu-id="61622-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61622-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61622-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61622-123">-InputObject</span></span>
<span data-ttu-id="61622-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="61622-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61622-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="61622-125">-KeyType</span></span>
<span data-ttu-id="61622-126">The keyType to regenerate.</span><span class="sxs-lookup"><span data-stu-id="61622-126">The keyType to regenerate.</span></span>
<span data-ttu-id="61622-127">Должен быть первичным или дополнительным (без чувствительным к делу).</span><span class="sxs-lookup"><span data-stu-id="61622-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61622-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="61622-128">-Parameter</span></span>
<span data-ttu-id="61622-129">Параметры описывают запрос на повторное создание ключей доступа, см. раздел "ЗАМЕТКИ" для свойств PARAMETER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="61622-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61622-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61622-130">-ResourceGroupName</span></span>
<span data-ttu-id="61622-131">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="61622-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="61622-132">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="61622-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61622-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61622-133">-SubscriptionId</span></span>
<span data-ttu-id="61622-134">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61622-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="61622-135">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="61622-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61622-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61622-136">-Confirm</span></span>
<span data-ttu-id="61622-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="61622-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61622-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61622-138">-WhatIf</span></span>
<span data-ttu-id="61622-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61622-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61622-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61622-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61622-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61622-141">CommonParameters</span></span>
<span data-ttu-id="61622-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61622-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61622-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61622-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61622-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61622-144">INPUTS</span></span>

### <span data-ttu-id="61622-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="61622-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="61622-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="61622-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="61622-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61622-147">OUTPUTS</span></span>

### <span data-ttu-id="61622-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="61622-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="61622-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61622-149">NOTES</span></span>

<span data-ttu-id="61622-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="61622-150">ALIASES</span></span>

<span data-ttu-id="61622-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="61622-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61622-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="61622-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61622-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61622-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61622-154">INPUTOBJECT <ICommunicationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="61622-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61622-155">`[CommunicationServiceName <String>]`: имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="61622-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="61622-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="61622-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61622-157">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="61622-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="61622-158">`[OperationId <String>]`: ID of an ongoing async operation</span><span class="sxs-lookup"><span data-stu-id="61622-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="61622-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="61622-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="61622-160">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="61622-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="61622-161">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61622-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="61622-162">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="61622-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="61622-163">PARAMETER <IRegenerateKeyParameters> : Параметры описывают запрос на повторное повторноегенеративные ключи доступа</span><span class="sxs-lookup"><span data-stu-id="61622-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="61622-164">`[KeyType <KeyType?>]`KeyType для повторного сгенерации.</span><span class="sxs-lookup"><span data-stu-id="61622-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="61622-165">Должен быть первичным или дополнительным (без чувствительным к делу).</span><span class="sxs-lookup"><span data-stu-id="61622-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="61622-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61622-166">RELATED LINKS</span></span>

