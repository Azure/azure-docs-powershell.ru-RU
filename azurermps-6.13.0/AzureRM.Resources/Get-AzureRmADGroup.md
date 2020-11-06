---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 8dc8188d9408c1b8e37fe44b149ceebeaf12ee4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564068"
---
# <span data-ttu-id="d9d7f-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="d9d7f-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="d9d7f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d7f-103">Фильтрует группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d7f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9d7f-104">SYNTAX</span></span>

### <span data-ttu-id="d9d7f-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9d7f-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9d7f-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d7f-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9d7f-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d7f-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9d7f-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d7f-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d9d7f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9d7f-109">DESCRIPTION</span></span>
<span data-ttu-id="d9d7f-110">Фильтрует группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-110">Filters active directory groups.</span></span>

## <span data-ttu-id="d9d7f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9d7f-111">EXAMPLES</span></span>

### <span data-ttu-id="d9d7f-112">Пример 1-список всех рекламных групп</span><span class="sxs-lookup"><span data-stu-id="d9d7f-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="d9d7f-113">Список всех групп рекламных объявлений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="d9d7f-114">Пример 2. Перечисление всех групп рекламных объявлений с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="d9d7f-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="d9d7f-115">Список первых групп рекламных объявлений 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="d9d7f-116">Пример 3. получить группу рекламных объявлений по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="d9d7f-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="d9d7f-117">Получает группу БАННЕРов с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="d9d7f-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="d9d7f-118">Пример 4: список групп по строке поиска</span><span class="sxs-lookup"><span data-stu-id="d9d7f-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="d9d7f-119">Список всех групп рекламных объявлений, отображаемое имя которых начинается с "Joe".</span><span class="sxs-lookup"><span data-stu-id="d9d7f-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="d9d7f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9d7f-120">PARAMETERS</span></span>

### <span data-ttu-id="d9d7f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d7f-121">-DefaultProfile</span></span>
<span data-ttu-id="d9d7f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9d7f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d7f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d9d7f-123">-DisplayName</span></span>
<span data-ttu-id="d9d7f-124">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-124">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d7f-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="d9d7f-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="d9d7f-126">Используется для поиска групп, начинающихся с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d7f-127">-First</span><span class="sxs-lookup"><span data-stu-id="d9d7f-127">-First</span></span>
<span data-ttu-id="d9d7f-128">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-128">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d7f-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d9d7f-129">-IncludeTotalCount</span></span>
<span data-ttu-id="d9d7f-130">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d9d7f-131">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d9d7f-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d9d7f-132">-ObjectId</span></span>
<span data-ttu-id="d9d7f-133">Идентификатор объекта группы.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-133">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d7f-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="d9d7f-134">-Skip</span></span>
<span data-ttu-id="d9d7f-135">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-135">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d7f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d7f-136">CommonParameters</span></span>
<span data-ttu-id="d9d7f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9d7f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d7f-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d7f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d7f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9d7f-139">INPUTS</span></span>

### <span data-ttu-id="d9d7f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d9d7f-140">System.String</span></span>

### <span data-ttu-id="d9d7f-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d9d7f-141">System.Guid</span></span>

## <span data-ttu-id="d9d7f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9d7f-142">OUTPUTS</span></span>

### <span data-ttu-id="d9d7f-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="d9d7f-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="d9d7f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9d7f-144">NOTES</span></span>

## <span data-ttu-id="d9d7f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9d7f-145">RELATED LINKS</span></span>

[<span data-ttu-id="d9d7f-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d9d7f-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="d9d7f-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d9d7f-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d9d7f-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="d9d7f-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

