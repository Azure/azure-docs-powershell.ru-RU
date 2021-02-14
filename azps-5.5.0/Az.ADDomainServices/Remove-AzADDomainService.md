---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: f29fbbdd805abb9891f707ed983bcf8aebefc46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210657"
---
# <span data-ttu-id="9d485-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="9d485-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="9d485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d485-102">SYNOPSIS</span></span>
<span data-ttu-id="9d485-103">В ходе операции удаления доменной службы удаляется существующая доменная служба.</span><span class="sxs-lookup"><span data-stu-id="9d485-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="9d485-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d485-104">SYNTAX</span></span>

### <span data-ttu-id="9d485-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d485-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9d485-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9d485-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d485-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d485-107">DESCRIPTION</span></span>
<span data-ttu-id="9d485-108">В ходе операции удаления доменной службы удаляется существующая доменная служба.</span><span class="sxs-lookup"><span data-stu-id="9d485-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="9d485-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d485-109">EXAMPLES</span></span>

### <span data-ttu-id="9d485-110">Пример 1. Удаление AzADDomain по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="9d485-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="9d485-111">Удаление AzADDomain по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="9d485-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="9d485-112">Пример 2. Удаление AzADDomain с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="9d485-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="9d485-113">Удаление AzADDomain с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="9d485-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="9d485-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d485-114">PARAMETERS</span></span>

### <span data-ttu-id="9d485-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d485-115">-AsJob</span></span>
<span data-ttu-id="9d485-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9d485-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9d485-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d485-117">-DefaultProfile</span></span>
<span data-ttu-id="9d485-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d485-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d485-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d485-119">-InputObject</span></span>
<span data-ttu-id="9d485-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9d485-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d485-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9d485-121">-Name</span></span>
<span data-ttu-id="9d485-122">Имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="9d485-122">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d485-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9d485-123">-NoWait</span></span>
<span data-ttu-id="9d485-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9d485-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9d485-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d485-125">-PassThru</span></span>
<span data-ttu-id="9d485-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="9d485-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9d485-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d485-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d485-128">Имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="9d485-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="9d485-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9d485-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9d485-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d485-130">-SubscriptionId</span></span>
<span data-ttu-id="9d485-131">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9d485-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9d485-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9d485-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9d485-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d485-133">-Confirm</span></span>
<span data-ttu-id="9d485-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d485-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d485-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d485-135">-WhatIf</span></span>
<span data-ttu-id="9d485-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d485-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d485-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d485-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d485-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d485-138">CommonParameters</span></span>
<span data-ttu-id="9d485-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d485-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d485-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d485-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d485-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d485-141">INPUTS</span></span>

### <span data-ttu-id="9d485-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="9d485-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="9d485-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d485-143">OUTPUTS</span></span>

### <span data-ttu-id="9d485-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d485-144">System.Boolean</span></span>

## <span data-ttu-id="9d485-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d485-145">NOTES</span></span>

<span data-ttu-id="9d485-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9d485-146">ALIASES</span></span>

<span data-ttu-id="9d485-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9d485-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d485-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9d485-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d485-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9d485-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d485-150">INPUTOBJECT <IAdDomainServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9d485-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d485-151">`[DomainServiceName <String>]`: имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="9d485-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="9d485-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9d485-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d485-153">`[ResourceGroupName <String>]`: имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="9d485-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="9d485-154">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9d485-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="9d485-155">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9d485-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="9d485-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9d485-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9d485-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d485-157">RELATED LINKS</span></span>

