---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314462"
---
# <span data-ttu-id="7fc2c-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="7fc2c-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="7fc2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fc2c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc2c-103">Получает манифест настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="7fc2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fc2c-104">SYNTAX</span></span>

### <span data-ttu-id="7fc2c-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fc2c-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fc2c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="7fc2c-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fc2c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7fc2c-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fc2c-108">Список</span><span class="sxs-lookup"><span data-stu-id="7fc2c-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fc2c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fc2c-109">DESCRIPTION</span></span>
<span data-ttu-id="7fc2c-110">Получает манифест настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="7fc2c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fc2c-111">EXAMPLES</span></span>

### <span data-ttu-id="7fc2c-112">Пример 1: список всех настраиваемых поставщиков в подписке</span><span class="sxs-lookup"><span data-stu-id="7fc2c-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="7fc2c-113">Список всех настраиваемых поставщиков в подписке</span><span class="sxs-lookup"><span data-stu-id="7fc2c-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="7fc2c-114">Пример 2: получение одного настраиваемого поставщика</span><span class="sxs-lookup"><span data-stu-id="7fc2c-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="7fc2c-115">Получение сведений об одном пользовательском поставщике.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="7fc2c-116">Используйте Format-List, чтобы отобразить сведения об объекте на экране.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="7fc2c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fc2c-117">PARAMETERS</span></span>

### <span data-ttu-id="7fc2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc2c-118">-DefaultProfile</span></span>
<span data-ttu-id="7fc2c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc2c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fc2c-120">-InputObject</span></span>
<span data-ttu-id="7fc2c-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7fc2c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7fc2c-122">-Name</span></span>
<span data-ttu-id="7fc2c-123">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="7fc2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fc2c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fc2c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fc2c-126">-SubscriptionId</span></span>
<span data-ttu-id="7fc2c-127">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-127">The Azure subscription ID.</span></span>
<span data-ttu-id="7fc2c-128">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7fc2c-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="7fc2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc2c-129">CommonParameters</span></span>
<span data-ttu-id="7fc2c-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc2c-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fc2c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc2c-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fc2c-132">INPUTS</span></span>

### <span data-ttu-id="7fc2c-133">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="7fc2c-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="7fc2c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fc2c-134">OUTPUTS</span></span>

### <span data-ttu-id="7fc2c-135">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="7fc2c-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="7fc2c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fc2c-136">NOTES</span></span>

<span data-ttu-id="7fc2c-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="7fc2c-137">ALIASES</span></span>

<span data-ttu-id="7fc2c-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7fc2c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fc2c-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fc2c-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fc2c-141">INPUTOBJECT <ICustomProvidersIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="7fc2c-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fc2c-142">`[AssociationName <String>]`: Имя связи.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="7fc2c-143">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="7fc2c-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fc2c-144">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7fc2c-145">`[ResourceProviderName <String>]`: Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="7fc2c-146">`[Scope <String>]`: Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="7fc2c-147">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc2c-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7fc2c-148">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7fc2c-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7fc2c-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fc2c-149">RELATED LINKS</span></span>

