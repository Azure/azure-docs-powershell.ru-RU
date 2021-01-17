---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416020"
---
# <span data-ttu-id="10ba3-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="10ba3-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="10ba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="10ba3-103">Получите связь.</span><span class="sxs-lookup"><span data-stu-id="10ba3-103">Get an association.</span></span>

## <span data-ttu-id="10ba3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10ba3-104">SYNTAX</span></span>

### <span data-ttu-id="10ba3-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10ba3-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="10ba3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="10ba3-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="10ba3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="10ba3-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="10ba3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10ba3-108">DESCRIPTION</span></span>
<span data-ttu-id="10ba3-109">Получите связь.</span><span class="sxs-lookup"><span data-stu-id="10ba3-109">Get an association.</span></span>

## <span data-ttu-id="10ba3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10ba3-110">EXAMPLES</span></span>

### <span data-ttu-id="10ba3-111">Пример 1. Списки настраиваемой связи поставщиков</span><span class="sxs-lookup"><span data-stu-id="10ba3-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="10ba3-112">Список всех настраиваемой связи поставщиков для заданной области.</span><span class="sxs-lookup"><span data-stu-id="10ba3-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="10ba3-113">Пример 2. Получить связь</span><span class="sxs-lookup"><span data-stu-id="10ba3-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="10ba3-114">Сведения об одной связи CustomProvider</span><span class="sxs-lookup"><span data-stu-id="10ba3-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="10ba3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10ba3-115">PARAMETERS</span></span>

### <span data-ttu-id="10ba3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ba3-116">-DefaultProfile</span></span>
<span data-ttu-id="10ba3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10ba3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ba3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10ba3-118">-InputObject</span></span>
<span data-ttu-id="10ba3-119">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="10ba3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="10ba3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="10ba3-120">-Name</span></span>
<span data-ttu-id="10ba3-121">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="10ba3-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ba3-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="10ba3-122">-Scope</span></span>
<span data-ttu-id="10ba3-123">Область действия связи.</span><span class="sxs-lookup"><span data-stu-id="10ba3-123">The scope of the association.</span></span>

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

### <span data-ttu-id="10ba3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ba3-124">CommonParameters</span></span>
<span data-ttu-id="10ba3-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ba3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ba3-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10ba3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ba3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10ba3-127">INPUTS</span></span>

### <span data-ttu-id="10ba3-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="10ba3-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="10ba3-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10ba3-129">OUTPUTS</span></span>

### <span data-ttu-id="10ba3-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="10ba3-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="10ba3-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10ba3-131">NOTES</span></span>

<span data-ttu-id="10ba3-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="10ba3-132">ALIASES</span></span>

<span data-ttu-id="10ba3-133">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="10ba3-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10ba3-134">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="10ba3-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10ba3-135">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10ba3-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10ba3-136">INPUTOBJECT <ICustomProvidersIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="10ba3-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="10ba3-137">`[AssociationName <String>]`: Название связи.</span><span class="sxs-lookup"><span data-stu-id="10ba3-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="10ba3-138">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="10ba3-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10ba3-139">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10ba3-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="10ba3-140">`[ResourceProviderName <String>]`: имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10ba3-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="10ba3-141">`[Scope <String>]`: область действия связи.</span><span class="sxs-lookup"><span data-stu-id="10ba3-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="10ba3-142">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="10ba3-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="10ba3-143">Это строка в формате GUID (например, 00000000-0000-0000-0000-0000-0000000000000)</span><span class="sxs-lookup"><span data-stu-id="10ba3-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="10ba3-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10ba3-144">RELATED LINKS</span></span>

