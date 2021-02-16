---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211860"
---
# <span data-ttu-id="24d4d-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="24d4d-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="24d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="24d4d-103">Операция удаления CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="24d4d-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="24d4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24d4d-104">SYNTAX</span></span>

### <span data-ttu-id="24d4d-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24d4d-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24d4d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24d4d-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24d4d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24d4d-107">DESCRIPTION</span></span>
<span data-ttu-id="24d4d-108">Операция удаления CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="24d4d-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="24d4d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24d4d-109">EXAMPLES</span></span>

### <span data-ttu-id="24d4d-110">Пример 1. Удаление указанного информационного ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="24d4d-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="24d4d-111">Удаление информационного ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="24d4d-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="24d4d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24d4d-112">PARAMETERS</span></span>

### <span data-ttu-id="24d4d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24d4d-113">-AsJob</span></span>
<span data-ttu-id="24d4d-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="24d4d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="24d4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d4d-115">-DefaultProfile</span></span>
<span data-ttu-id="24d4d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24d4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d4d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24d4d-117">-InputObject</span></span>
<span data-ttu-id="24d4d-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="24d4d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24d4d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="24d4d-119">-Name</span></span>
<span data-ttu-id="24d4d-120">Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="24d4d-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d4d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="24d4d-121">-NoWait</span></span>
<span data-ttu-id="24d4d-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="24d4d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="24d4d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24d4d-123">-PassThru</span></span>
<span data-ttu-id="24d4d-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="24d4d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="24d4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="24d4d-126">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="24d4d-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="24d4d-127">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="24d4d-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="24d4d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24d4d-128">-SubscriptionId</span></span>
<span data-ttu-id="24d4d-129">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24d4d-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="24d4d-130">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="24d4d-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24d4d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24d4d-131">-Confirm</span></span>
<span data-ttu-id="24d4d-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="24d4d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d4d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d4d-133">-WhatIf</span></span>
<span data-ttu-id="24d4d-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24d4d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d4d-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="24d4d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d4d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d4d-136">CommonParameters</span></span>
<span data-ttu-id="24d4d-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d4d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d4d-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24d4d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d4d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24d4d-139">INPUTS</span></span>

### <span data-ttu-id="24d4d-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="24d4d-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="24d4d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24d4d-141">OUTPUTS</span></span>

### <span data-ttu-id="24d4d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24d4d-142">System.Boolean</span></span>

## <span data-ttu-id="24d4d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24d4d-143">NOTES</span></span>

<span data-ttu-id="24d4d-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="24d4d-144">ALIASES</span></span>

<span data-ttu-id="24d4d-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="24d4d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24d4d-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="24d4d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24d4d-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24d4d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24d4d-148">INPUTOBJECT <ICommunicationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="24d4d-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24d4d-149">`[CommunicationServiceName <String>]`: Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="24d4d-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="24d4d-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="24d4d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24d4d-151">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="24d4d-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="24d4d-152">`[OperationId <String>]`: ID of an ongoing async operation</span><span class="sxs-lookup"><span data-stu-id="24d4d-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="24d4d-153">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="24d4d-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="24d4d-154">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="24d4d-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="24d4d-155">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24d4d-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="24d4d-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="24d4d-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="24d4d-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24d4d-157">RELATED LINKS</span></span>

