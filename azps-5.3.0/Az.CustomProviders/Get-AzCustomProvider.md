---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519141"
---
# <span data-ttu-id="1642d-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="1642d-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="1642d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1642d-102">SYNOPSIS</span></span>
<span data-ttu-id="1642d-103">Настраиваемый манифест поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1642d-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="1642d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1642d-104">SYNTAX</span></span>

### <span data-ttu-id="1642d-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1642d-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1642d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="1642d-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1642d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1642d-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1642d-108">Список</span><span class="sxs-lookup"><span data-stu-id="1642d-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1642d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1642d-109">DESCRIPTION</span></span>
<span data-ttu-id="1642d-110">Настраиваемый манифест поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1642d-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="1642d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1642d-111">EXAMPLES</span></span>

### <span data-ttu-id="1642d-112">Пример 1. Список всех пользовательских поставщиков в подписке</span><span class="sxs-lookup"><span data-stu-id="1642d-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="1642d-113">Список всех пользовательских поставщиков подписки</span><span class="sxs-lookup"><span data-stu-id="1642d-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="1642d-114">Пример 2. Получить одного поставщика настраиваемой службы</span><span class="sxs-lookup"><span data-stu-id="1642d-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

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

<span data-ttu-id="1642d-115">Сведения об одном пользовательском поставщике.</span><span class="sxs-lookup"><span data-stu-id="1642d-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="1642d-116">Используйте Format-List для показа сведений об объекте на экране.</span><span class="sxs-lookup"><span data-stu-id="1642d-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="1642d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1642d-117">PARAMETERS</span></span>

### <span data-ttu-id="1642d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1642d-118">-DefaultProfile</span></span>
<span data-ttu-id="1642d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1642d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1642d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1642d-120">-InputObject</span></span>
<span data-ttu-id="1642d-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1642d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1642d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1642d-122">-Name</span></span>
<span data-ttu-id="1642d-123">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1642d-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1642d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1642d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1642d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1642d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1642d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1642d-126">-SubscriptionId</span></span>
<span data-ttu-id="1642d-127">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="1642d-127">The Azure subscription ID.</span></span>
<span data-ttu-id="1642d-128">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="1642d-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1642d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1642d-129">CommonParameters</span></span>
<span data-ttu-id="1642d-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1642d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1642d-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1642d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1642d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1642d-132">INPUTS</span></span>

### <span data-ttu-id="1642d-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="1642d-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="1642d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1642d-134">OUTPUTS</span></span>

### <span data-ttu-id="1642d-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="1642d-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="1642d-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1642d-136">NOTES</span></span>

<span data-ttu-id="1642d-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1642d-137">ALIASES</span></span>

<span data-ttu-id="1642d-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1642d-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1642d-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1642d-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1642d-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1642d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1642d-141">INPUTOBJECT <ICustomProvidersIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1642d-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1642d-142">`[AssociationName <String>]`: Название связи.</span><span class="sxs-lookup"><span data-stu-id="1642d-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="1642d-143">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1642d-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1642d-144">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1642d-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1642d-145">`[ResourceProviderName <String>]`: имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1642d-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="1642d-146">`[Scope <String>]`: область действия связи.</span><span class="sxs-lookup"><span data-stu-id="1642d-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="1642d-147">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="1642d-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="1642d-148">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="1642d-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="1642d-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1642d-149">RELATED LINKS</span></span>

