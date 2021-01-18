---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505318"
---
# <span data-ttu-id="5c947-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="5c947-101">Get-AzADGroup</span></span>

## <span data-ttu-id="5c947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c947-102">SYNOPSIS</span></span>
<span data-ttu-id="5c947-103">Фильтрует группы активных каталогов.</span><span class="sxs-lookup"><span data-stu-id="5c947-103">Filters active directory groups.</span></span>

## <span data-ttu-id="5c947-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c947-104">SYNTAX</span></span>

### <span data-ttu-id="5c947-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c947-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5c947-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c947-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5c947-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c947-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5c947-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c947-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5c947-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c947-109">DESCRIPTION</span></span>
<span data-ttu-id="5c947-110">Фильтрует группы активных каталогов.</span><span class="sxs-lookup"><span data-stu-id="5c947-110">Filters active directory groups.</span></span>

## <span data-ttu-id="5c947-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c947-111">EXAMPLES</span></span>

### <span data-ttu-id="5c947-112">Пример 1. Список всех групп AD</span><span class="sxs-lookup"><span data-stu-id="5c947-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="5c947-113">Список всех групп AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="5c947-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="5c947-114">Пример 2. Список всех групп AD с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="5c947-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="5c947-115">Список первых 100 групп AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="5c947-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="5c947-116">Пример 3. Группировка AD по ид объекта</span><span class="sxs-lookup"><span data-stu-id="5c947-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="5c947-117">Возвращает группу AD с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="5c947-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5c947-118">Пример 4. Группы списков по строке поиска</span><span class="sxs-lookup"><span data-stu-id="5c947-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="5c947-119">Список всех групп AD, отображаемая имена которых начинается с "Сергей".</span><span class="sxs-lookup"><span data-stu-id="5c947-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="5c947-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c947-120">PARAMETERS</span></span>

### <span data-ttu-id="5c947-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c947-121">-DefaultProfile</span></span>
<span data-ttu-id="5c947-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c947-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c947-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5c947-123">-DisplayName</span></span>
<span data-ttu-id="5c947-124">Отображаемая группа.</span><span class="sxs-lookup"><span data-stu-id="5c947-124">The display name of the group.</span></span>

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

### <span data-ttu-id="5c947-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="5c947-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="5c947-126">Используется для поиска групп, которые начинаются с за предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="5c947-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="5c947-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5c947-127">-ObjectId</span></span>
<span data-ttu-id="5c947-128">Object id of the group.</span><span class="sxs-lookup"><span data-stu-id="5c947-128">Object id of the group.</span></span>

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

### <span data-ttu-id="5c947-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5c947-129">-IncludeTotalCount</span></span>
<span data-ttu-id="5c947-130">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="5c947-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="5c947-131">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="5c947-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5c947-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="5c947-132">-Skip</span></span>
<span data-ttu-id="5c947-133">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="5c947-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="5c947-134">-First</span><span class="sxs-lookup"><span data-stu-id="5c947-134">-First</span></span>
<span data-ttu-id="5c947-135">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="5c947-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="5c947-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c947-136">CommonParameters</span></span>
<span data-ttu-id="5c947-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c947-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c947-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c947-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c947-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c947-139">INPUTS</span></span>

### <span data-ttu-id="5c947-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5c947-140">System.String</span></span>

### <span data-ttu-id="5c947-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5c947-141">System.Guid</span></span>

## <span data-ttu-id="5c947-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c947-142">OUTPUTS</span></span>

### <span data-ttu-id="5c947-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5c947-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5c947-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c947-144">NOTES</span></span>

## <span data-ttu-id="5c947-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c947-145">RELATED LINKS</span></span>

[<span data-ttu-id="5c947-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5c947-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="5c947-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5c947-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="5c947-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5c947-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

