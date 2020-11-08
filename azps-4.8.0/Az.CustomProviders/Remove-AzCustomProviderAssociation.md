---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245059"
---
# <span data-ttu-id="3bb85-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="3bb85-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="3bb85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bb85-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb85-103">Удаление связи.</span><span class="sxs-lookup"><span data-stu-id="3bb85-103">Delete an association.</span></span>

## <span data-ttu-id="3bb85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bb85-104">SYNTAX</span></span>

### <span data-ttu-id="3bb85-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3bb85-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3bb85-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bb85-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bb85-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bb85-107">DESCRIPTION</span></span>
<span data-ttu-id="3bb85-108">Удаление связи.</span><span class="sxs-lookup"><span data-stu-id="3bb85-108">Delete an association.</span></span>

## <span data-ttu-id="3bb85-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bb85-109">EXAMPLES</span></span>

### <span data-ttu-id="3bb85-110">Пример 1: Удаление сопоставления настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="3bb85-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="3bb85-111">Удаление сопоставления настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="3bb85-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="3bb85-112">Пример 2: Удаление связи настраиваемого поставщика с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="3bb85-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="3bb85-113">Удалите настраиваемую связь поставщика, используя функцию трубопроводов и PassThru для обозначения успеха или сбоя.</span><span class="sxs-lookup"><span data-stu-id="3bb85-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="3bb85-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bb85-114">PARAMETERS</span></span>

### <span data-ttu-id="3bb85-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bb85-115">-AsJob</span></span>
<span data-ttu-id="3bb85-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3bb85-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3bb85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb85-117">-DefaultProfile</span></span>
<span data-ttu-id="3bb85-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb85-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb85-119">-InputObject</span></span>
<span data-ttu-id="3bb85-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3bb85-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bb85-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3bb85-121">-Name</span></span>
<span data-ttu-id="3bb85-122">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="3bb85-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb85-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="3bb85-123">-NoWait</span></span>
<span data-ttu-id="3bb85-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3bb85-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3bb85-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bb85-125">-PassThru</span></span>
<span data-ttu-id="3bb85-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3bb85-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3bb85-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="3bb85-127">-Scope</span></span>
<span data-ttu-id="3bb85-128">Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="3bb85-128">The scope of the association.</span></span>

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

### <span data-ttu-id="3bb85-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bb85-129">-Confirm</span></span>
<span data-ttu-id="3bb85-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3bb85-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb85-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb85-131">-WhatIf</span></span>
<span data-ttu-id="3bb85-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3bb85-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb85-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3bb85-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb85-134">CommonParameters</span></span>
<span data-ttu-id="3bb85-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bb85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb85-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bb85-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb85-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bb85-137">INPUTS</span></span>

### <span data-ttu-id="3bb85-138">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="3bb85-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="3bb85-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bb85-139">OUTPUTS</span></span>

### <span data-ttu-id="3bb85-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bb85-140">System.Boolean</span></span>

## <span data-ttu-id="3bb85-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bb85-141">NOTES</span></span>

<span data-ttu-id="3bb85-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3bb85-142">ALIASES</span></span>

<span data-ttu-id="3bb85-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3bb85-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bb85-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3bb85-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bb85-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3bb85-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bb85-146">INPUTOBJECT <ICustomProvidersIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="3bb85-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bb85-147">`[AssociationName <String>]`: Имя связи.</span><span class="sxs-lookup"><span data-stu-id="3bb85-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="3bb85-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3bb85-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bb85-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3bb85-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3bb85-150">`[ResourceProviderName <String>]`: Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3bb85-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="3bb85-151">`[Scope <String>]`: Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="3bb85-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="3bb85-152">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb85-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="3bb85-153">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="3bb85-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="3bb85-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bb85-154">RELATED LINKS</span></span>

