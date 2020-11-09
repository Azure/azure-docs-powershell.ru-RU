---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314459"
---
# <span data-ttu-id="a2fa4-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="a2fa4-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="a2fa4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fa4-103">Получить связь.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-103">Get an association.</span></span>

## <span data-ttu-id="a2fa4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2fa4-104">SYNTAX</span></span>

### <span data-ttu-id="a2fa4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2fa4-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a2fa4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a2fa4-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2fa4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a2fa4-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2fa4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2fa4-108">DESCRIPTION</span></span>
<span data-ttu-id="a2fa4-109">Получить связь.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-109">Get an association.</span></span>

## <span data-ttu-id="a2fa4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2fa4-110">EXAMPLES</span></span>

### <span data-ttu-id="a2fa4-111">Пример 1: сопоставление настраиваемого поставщика для списка</span><span class="sxs-lookup"><span data-stu-id="a2fa4-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="a2fa4-112">Перечисление всех связей между пользовательскими поставщиками для заданной области.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="a2fa4-113">Пример 2: получение связи</span><span class="sxs-lookup"><span data-stu-id="a2fa4-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="a2fa4-114">Получение сведений об одной ассоциации CustomProvider</span><span class="sxs-lookup"><span data-stu-id="a2fa4-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="a2fa4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2fa4-115">PARAMETERS</span></span>

### <span data-ttu-id="a2fa4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fa4-116">-DefaultProfile</span></span>
<span data-ttu-id="a2fa4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2fa4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2fa4-118">-InputObject</span></span>
<span data-ttu-id="a2fa4-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2fa4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2fa4-120">-Name</span></span>
<span data-ttu-id="a2fa4-121">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-121">The name of the association.</span></span>

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

### <span data-ttu-id="a2fa4-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="a2fa4-122">-Scope</span></span>
<span data-ttu-id="a2fa4-123">Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-123">The scope of the association.</span></span>

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

### <span data-ttu-id="a2fa4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fa4-124">CommonParameters</span></span>
<span data-ttu-id="a2fa4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fa4-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2fa4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fa4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2fa4-127">INPUTS</span></span>

### <span data-ttu-id="a2fa4-128">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="a2fa4-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="a2fa4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2fa4-129">OUTPUTS</span></span>

### <span data-ttu-id="a2fa4-130">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="a2fa4-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="a2fa4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2fa4-131">NOTES</span></span>

<span data-ttu-id="a2fa4-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a2fa4-132">ALIASES</span></span>

<span data-ttu-id="a2fa4-133">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a2fa4-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2fa4-134">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2fa4-135">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2fa4-136">INPUTOBJECT <ICustomProvidersIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a2fa4-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2fa4-137">`[AssociationName <String>]`: Имя связи.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="a2fa4-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a2fa4-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2fa4-139">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a2fa4-140">`[ResourceProviderName <String>]`: Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="a2fa4-141">`[Scope <String>]`: Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="a2fa4-142">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a2fa4-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a2fa4-143">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a2fa4-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a2fa4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2fa4-144">RELATED LINKS</span></span>

