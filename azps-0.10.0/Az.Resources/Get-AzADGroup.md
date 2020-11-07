---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 42696be07c560d24d1d87542873b6795497c370c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910965"
---
# <span data-ttu-id="ba251-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="ba251-101">Get-AzADGroup</span></span>

## <span data-ttu-id="ba251-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba251-102">SYNOPSIS</span></span>
<span data-ttu-id="ba251-103">Фильтрует группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba251-103">Filters active directory groups.</span></span>

## <span data-ttu-id="ba251-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba251-104">SYNTAX</span></span>

### <span data-ttu-id="ba251-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba251-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ba251-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba251-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ba251-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba251-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ba251-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba251-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ba251-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba251-109">DESCRIPTION</span></span>
<span data-ttu-id="ba251-110">Фильтрует группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba251-110">Filters active directory groups.</span></span>

## <span data-ttu-id="ba251-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba251-111">EXAMPLES</span></span>

### <span data-ttu-id="ba251-112">Пример 1-список всех рекламных групп</span><span class="sxs-lookup"><span data-stu-id="ba251-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzADGroup
```

<span data-ttu-id="ba251-113">Список всех групп рекламных объявлений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ba251-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="ba251-114">Пример 2. Перечисление всех групп рекламных объявлений с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="ba251-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="ba251-115">Список первых групп рекламных объявлений 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ba251-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="ba251-116">Пример 3. получить группу рекламных объявлений по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="ba251-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="ba251-117">Получает группу БАННЕРов с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="ba251-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ba251-118">Пример 4: список групп по строке поиска</span><span class="sxs-lookup"><span data-stu-id="ba251-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="ba251-119">Список всех групп рекламных объявлений, отображаемое имя которых начинается с "Joe".</span><span class="sxs-lookup"><span data-stu-id="ba251-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="ba251-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba251-120">PARAMETERS</span></span>

### <span data-ttu-id="ba251-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba251-121">-DefaultProfile</span></span>
<span data-ttu-id="ba251-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba251-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba251-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ba251-123">-DisplayName</span></span>
<span data-ttu-id="ba251-124">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="ba251-124">The display name of the group.</span></span>

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

### <span data-ttu-id="ba251-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="ba251-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="ba251-126">Используется для поиска групп, начинающихся с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="ba251-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="ba251-127">-First</span><span class="sxs-lookup"><span data-stu-id="ba251-127">-First</span></span>
<span data-ttu-id="ba251-128">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="ba251-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="ba251-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ba251-129">-IncludeTotalCount</span></span>
<span data-ttu-id="ba251-130">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="ba251-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ba251-131">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="ba251-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ba251-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ba251-132">-ObjectId</span></span>
<span data-ttu-id="ba251-133">Идентификатор объекта группы.</span><span class="sxs-lookup"><span data-stu-id="ba251-133">Object id of the group.</span></span>

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

### <span data-ttu-id="ba251-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="ba251-134">-Skip</span></span>
<span data-ttu-id="ba251-135">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="ba251-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="ba251-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba251-136">CommonParameters</span></span>
<span data-ttu-id="ba251-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba251-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba251-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba251-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba251-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba251-139">INPUTS</span></span>

### <span data-ttu-id="ba251-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ba251-140">System.String</span></span>

### <span data-ttu-id="ba251-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ba251-141">System.Guid</span></span>

## <span data-ttu-id="ba251-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba251-142">OUTPUTS</span></span>

### <span data-ttu-id="ba251-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ba251-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ba251-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba251-144">NOTES</span></span>

## <span data-ttu-id="ba251-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba251-145">RELATED LINKS</span></span>

[<span data-ttu-id="ba251-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ba251-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="ba251-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ba251-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="ba251-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="ba251-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

