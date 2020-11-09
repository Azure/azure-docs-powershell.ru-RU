---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314432"
---
# <span data-ttu-id="d1725-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="d1725-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="d1725-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1725-102">SYNOPSIS</span></span>
<span data-ttu-id="d1725-103">Удаление настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1725-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="d1725-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1725-104">SYNTAX</span></span>

### <span data-ttu-id="d1725-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1725-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1725-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1725-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1725-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1725-107">DESCRIPTION</span></span>
<span data-ttu-id="d1725-108">Удаление настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1725-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="d1725-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1725-109">EXAMPLES</span></span>

### <span data-ttu-id="d1725-110">Пример 1: Удаление настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="d1725-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="d1725-111">Удаление настраиваемого поставщика</span><span class="sxs-lookup"><span data-stu-id="d1725-111">Remove a custom provider</span></span>

### <span data-ttu-id="d1725-112">Пример 2: Удаление настраиваемого поставщика с помощью PassThru</span><span class="sxs-lookup"><span data-stu-id="d1725-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="d1725-113">Удаление настраиваемого поставщика с помощью функции PassThru для обозначения успеха или сбоя.</span><span class="sxs-lookup"><span data-stu-id="d1725-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="d1725-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1725-114">PARAMETERS</span></span>

### <span data-ttu-id="d1725-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1725-115">-AsJob</span></span>
<span data-ttu-id="d1725-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d1725-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d1725-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1725-117">-DefaultProfile</span></span>
<span data-ttu-id="d1725-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1725-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1725-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1725-119">-InputObject</span></span>
<span data-ttu-id="d1725-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d1725-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1725-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1725-121">-Name</span></span>
<span data-ttu-id="d1725-122">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1725-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="d1725-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="d1725-123">-NoWait</span></span>
<span data-ttu-id="d1725-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d1725-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d1725-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1725-125">-PassThru</span></span>
<span data-ttu-id="d1725-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d1725-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d1725-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1725-127">-ResourceGroupName</span></span>
<span data-ttu-id="d1725-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1725-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1725-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1725-129">-SubscriptionId</span></span>
<span data-ttu-id="d1725-130">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d1725-130">The Azure subscription ID.</span></span>
<span data-ttu-id="d1725-131">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="d1725-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="d1725-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1725-132">-Confirm</span></span>
<span data-ttu-id="d1725-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1725-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1725-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1725-134">-WhatIf</span></span>
<span data-ttu-id="d1725-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1725-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1725-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1725-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1725-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1725-137">CommonParameters</span></span>
<span data-ttu-id="d1725-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1725-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1725-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1725-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1725-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1725-140">INPUTS</span></span>

### <span data-ttu-id="d1725-141">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="d1725-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="d1725-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1725-142">OUTPUTS</span></span>

### <span data-ttu-id="d1725-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1725-143">System.Boolean</span></span>

## <span data-ttu-id="d1725-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1725-144">NOTES</span></span>

<span data-ttu-id="d1725-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d1725-145">ALIASES</span></span>

<span data-ttu-id="d1725-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d1725-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1725-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1725-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1725-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1725-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1725-149">INPUTOBJECT <ICustomProvidersIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d1725-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1725-150">`[AssociationName <String>]`: Имя связи.</span><span class="sxs-lookup"><span data-stu-id="d1725-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="d1725-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d1725-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1725-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1725-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d1725-153">`[ResourceProviderName <String>]`: Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1725-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="d1725-154">`[Scope <String>]`: Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="d1725-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="d1725-155">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d1725-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="d1725-156">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="d1725-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="d1725-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1725-157">RELATED LINKS</span></span>

