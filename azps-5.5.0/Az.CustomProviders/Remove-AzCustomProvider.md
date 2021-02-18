---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215217"
---
# <span data-ttu-id="c4c58-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="c4c58-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="c4c58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4c58-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c58-103">Удаляет поставщика настраиваемой службы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4c58-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="c4c58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4c58-104">SYNTAX</span></span>

### <span data-ttu-id="c4c58-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4c58-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4c58-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4c58-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4c58-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4c58-107">DESCRIPTION</span></span>
<span data-ttu-id="c4c58-108">Удаляет поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4c58-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="c4c58-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4c58-109">EXAMPLES</span></span>

### <span data-ttu-id="c4c58-110">Пример 1. Удаление пользовательского поставщика.</span><span class="sxs-lookup"><span data-stu-id="c4c58-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="c4c58-111">Удаление поставщика настраиваемой службы</span><span class="sxs-lookup"><span data-stu-id="c4c58-111">Remove a custom provider</span></span>

### <span data-ttu-id="c4c58-112">Пример 2. Удаление пользовательского поставщика с помощью passThru</span><span class="sxs-lookup"><span data-stu-id="c4c58-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="c4c58-113">Удалите поставщика, указать успех или неудачу с помощью функции PassThru.</span><span class="sxs-lookup"><span data-stu-id="c4c58-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="c4c58-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4c58-114">PARAMETERS</span></span>

### <span data-ttu-id="c4c58-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4c58-115">-AsJob</span></span>
<span data-ttu-id="c4c58-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c4c58-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c4c58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c58-117">-DefaultProfile</span></span>
<span data-ttu-id="c4c58-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c58-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4c58-119">-InputObject</span></span>
<span data-ttu-id="c4c58-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c4c58-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c58-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c4c58-121">-Name</span></span>
<span data-ttu-id="c4c58-122">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4c58-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c58-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4c58-123">-NoWait</span></span>
<span data-ttu-id="c4c58-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c4c58-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4c58-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4c58-125">-PassThru</span></span>
<span data-ttu-id="c4c58-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="c4c58-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4c58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c58-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4c58-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4c58-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4c58-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4c58-129">-SubscriptionId</span></span>
<span data-ttu-id="c4c58-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c58-130">The Azure subscription ID.</span></span>
<span data-ttu-id="c4c58-131">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="c4c58-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c4c58-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4c58-132">-Confirm</span></span>
<span data-ttu-id="c4c58-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c58-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c58-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c58-134">-WhatIf</span></span>
<span data-ttu-id="c4c58-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c58-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c58-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4c58-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c58-137">CommonParameters</span></span>
<span data-ttu-id="c4c58-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c58-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4c58-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c58-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4c58-140">INPUTS</span></span>

### <span data-ttu-id="c4c58-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="c4c58-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="c4c58-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4c58-142">OUTPUTS</span></span>

### <span data-ttu-id="c4c58-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4c58-143">System.Boolean</span></span>

## <span data-ttu-id="c4c58-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4c58-144">NOTES</span></span>

<span data-ttu-id="c4c58-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c4c58-145">ALIASES</span></span>

<span data-ttu-id="c4c58-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c4c58-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4c58-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c4c58-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4c58-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4c58-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4c58-149">INPUTOBJECT <ICustomProvidersIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c4c58-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4c58-150">`[AssociationName <String>]`: название связи.</span><span class="sxs-lookup"><span data-stu-id="c4c58-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="c4c58-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c4c58-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4c58-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4c58-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c4c58-153">`[ResourceProviderName <String>]`: имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4c58-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="c4c58-154">`[Scope <String>]`: область действия связи.</span><span class="sxs-lookup"><span data-stu-id="c4c58-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="c4c58-155">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c58-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c4c58-156">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="c4c58-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c4c58-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4c58-157">RELATED LINKS</span></span>

