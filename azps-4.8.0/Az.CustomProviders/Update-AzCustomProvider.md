---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079738"
---
# <span data-ttu-id="e2f5f-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="e2f5f-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="e2f5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f5f-103">Обновляет существующий настраиваемый поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="e2f5f-104">Единственным значением, которое может быть обновлено посредством исправления, является тег.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="e2f5f-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2f5f-105">SYNTAX</span></span>

### <span data-ttu-id="e2f5f-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2f5f-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2f5f-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e2f5f-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2f5f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f5f-108">DESCRIPTION</span></span>
<span data-ttu-id="e2f5f-109">Обновляет существующий настраиваемый поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="e2f5f-110">Единственным значением, которое может быть обновлено посредством исправления, является тег.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="e2f5f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2f5f-111">EXAMPLES</span></span>

### <span data-ttu-id="e2f5f-112">Пример 1: Добавление тегов к настраиваемому поставщику</span><span class="sxs-lookup"><span data-stu-id="e2f5f-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="e2f5f-113">Обновите Теги настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="e2f5f-114">Пример 2: Обновление настраиваемого поставщика с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="e2f5f-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="e2f5f-115">Обновление настраиваемого поставщика с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="e2f5f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2f5f-116">PARAMETERS</span></span>

### <span data-ttu-id="e2f5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f5f-117">-DefaultProfile</span></span>
<span data-ttu-id="e2f5f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f5f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f5f-119">-InputObject</span></span>
<span data-ttu-id="e2f5f-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f5f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2f5f-121">-Name</span></span>
<span data-ttu-id="e2f5f-122">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2f5f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f5f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2f5f-125">-SubscriptionId</span></span>
<span data-ttu-id="e2f5f-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-126">The Azure subscription ID.</span></span>
<span data-ttu-id="e2f5f-127">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="e2f5f-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f5f-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="e2f5f-128">-Tag</span></span>
<span data-ttu-id="e2f5f-129">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2f5f-129">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f5f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f5f-130">-Confirm</span></span>
<span data-ttu-id="e2f5f-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f5f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f5f-132">-WhatIf</span></span>
<span data-ttu-id="e2f5f-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f5f-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f5f-135">CommonParameters</span></span>
<span data-ttu-id="e2f5f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f5f-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2f5f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f5f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2f5f-138">INPUTS</span></span>

### <span data-ttu-id="e2f5f-139">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="e2f5f-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="e2f5f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f5f-140">OUTPUTS</span></span>

### <span data-ttu-id="e2f5f-141">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="e2f5f-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="e2f5f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2f5f-142">NOTES</span></span>

<span data-ttu-id="e2f5f-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e2f5f-143">ALIASES</span></span>

<span data-ttu-id="e2f5f-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e2f5f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2f5f-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2f5f-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2f5f-147">INPUTOBJECT <ICustomProvidersIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e2f5f-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2f5f-148">`[AssociationName <String>]`: Имя связи.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="e2f5f-149">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e2f5f-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2f5f-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e2f5f-151">`[ResourceProviderName <String>]`: Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="e2f5f-152">`[Scope <String>]`: Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="e2f5f-153">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f5f-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="e2f5f-154">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="e2f5f-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="e2f5f-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2f5f-155">RELATED LINKS</span></span>

