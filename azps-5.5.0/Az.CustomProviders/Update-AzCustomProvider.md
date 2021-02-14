---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215209"
---
# <span data-ttu-id="6c767-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="6c767-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="6c767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c767-102">SYNOPSIS</span></span>
<span data-ttu-id="6c767-103">Обновляет существующего пользовательского поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c767-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="6c767-104">В настоящее время с помощью исправления можно обновлять только теги.</span><span class="sxs-lookup"><span data-stu-id="6c767-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="6c767-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c767-105">SYNTAX</span></span>

### <span data-ttu-id="6c767-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c767-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c767-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6c767-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c767-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c767-108">DESCRIPTION</span></span>
<span data-ttu-id="6c767-109">Обновляет существующего пользовательского поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c767-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="6c767-110">В настоящее время с помощью исправления можно обновлять только теги.</span><span class="sxs-lookup"><span data-stu-id="6c767-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="6c767-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c767-111">EXAMPLES</span></span>

### <span data-ttu-id="6c767-112">Пример 1. Добавление тегов к пользовательскому поставщику</span><span class="sxs-lookup"><span data-stu-id="6c767-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="6c767-113">Обновив теги настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c767-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="6c767-114">Пример 2. Обновление пользовательского поставщика с помощью piping</span><span class="sxs-lookup"><span data-stu-id="6c767-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="6c767-115">Обновление пользовательского поставщика с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="6c767-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="6c767-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c767-116">PARAMETERS</span></span>

### <span data-ttu-id="6c767-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c767-117">-DefaultProfile</span></span>
<span data-ttu-id="6c767-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c767-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c767-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c767-119">-InputObject</span></span>
<span data-ttu-id="6c767-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="6c767-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6c767-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6c767-121">-Name</span></span>
<span data-ttu-id="6c767-122">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c767-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="6c767-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c767-123">-ResourceGroupName</span></span>
<span data-ttu-id="6c767-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c767-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c767-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c767-125">-SubscriptionId</span></span>
<span data-ttu-id="6c767-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="6c767-126">The Azure subscription ID.</span></span>
<span data-ttu-id="6c767-127">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="6c767-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6c767-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c767-128">-Tag</span></span>
<span data-ttu-id="6c767-129">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c767-129">Resource tags</span></span>

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

### <span data-ttu-id="6c767-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c767-130">-Confirm</span></span>
<span data-ttu-id="6c767-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c767-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c767-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c767-132">-WhatIf</span></span>
<span data-ttu-id="6c767-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c767-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c767-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6c767-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c767-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c767-135">CommonParameters</span></span>
<span data-ttu-id="6c767-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c767-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c767-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c767-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c767-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c767-138">INPUTS</span></span>

### <span data-ttu-id="6c767-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="6c767-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="6c767-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c767-140">OUTPUTS</span></span>

### <span data-ttu-id="6c767-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="6c767-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="6c767-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c767-142">NOTES</span></span>

<span data-ttu-id="6c767-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6c767-143">ALIASES</span></span>

<span data-ttu-id="6c767-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6c767-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c767-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="6c767-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c767-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6c767-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c767-147">INPUTOBJECT <ICustomProvidersIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="6c767-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c767-148">`[AssociationName <String>]`: Название связи.</span><span class="sxs-lookup"><span data-stu-id="6c767-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="6c767-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="6c767-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c767-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c767-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6c767-151">`[ResourceProviderName <String>]`: имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c767-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="6c767-152">`[Scope <String>]`: область действия связи.</span><span class="sxs-lookup"><span data-stu-id="6c767-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="6c767-153">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="6c767-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6c767-154">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="6c767-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6c767-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c767-155">RELATED LINKS</span></span>

