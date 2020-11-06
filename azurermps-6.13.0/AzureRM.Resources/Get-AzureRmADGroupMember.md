---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: ffc04a6b1560845a0c29db4d000270fe91aa8ff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570192"
---
# <span data-ttu-id="47e71-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="47e71-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="47e71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47e71-102">SYNOPSIS</span></span>
<span data-ttu-id="47e71-103">Список участников группы БАННЕРов в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="47e71-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47e71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47e71-104">SYNTAX</span></span>

### <span data-ttu-id="47e71-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47e71-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="47e71-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47e71-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="47e71-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47e71-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="47e71-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47e71-108">DESCRIPTION</span></span>
<span data-ttu-id="47e71-109">Список участников группы БАННЕРов в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="47e71-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="47e71-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47e71-110">EXAMPLES</span></span>

### <span data-ttu-id="47e71-111">Пример 1: члены списка по идентификатору объекта группы рекламы</span><span class="sxs-lookup"><span data-stu-id="47e71-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="47e71-112">Список участников группы Active Directory с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="47e71-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="47e71-113">Пример 2: члены списка по идентификатору объекта группы Active Directory с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="47e71-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="47e71-114">Список первых 100 участников группы Active Directory с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="47e71-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="47e71-115">Пример 3: список членов по конвейеру</span><span class="sxs-lookup"><span data-stu-id="47e71-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="47e71-116">Получает группу БАННЕРов с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и добавляет ее в командлет Get-AzureRmADGroupMember, чтобы вывести список всех участников этой группы.</span><span class="sxs-lookup"><span data-stu-id="47e71-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="47e71-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47e71-117">PARAMETERS</span></span>

### <span data-ttu-id="47e71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e71-118">-DefaultProfile</span></span>
<span data-ttu-id="47e71-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47e71-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47e71-120">-First</span><span class="sxs-lookup"><span data-stu-id="47e71-120">-First</span></span>
<span data-ttu-id="47e71-121">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="47e71-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="47e71-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="47e71-122">-GroupDisplayName</span></span>
<span data-ttu-id="47e71-123">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="47e71-123">The display name of the group.</span></span>

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

### <span data-ttu-id="47e71-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="47e71-124">-GroupObject</span></span>
<span data-ttu-id="47e71-125">Объект Group, из которого вы перечислите элементы.</span><span class="sxs-lookup"><span data-stu-id="47e71-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47e71-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="47e71-126">-GroupObjectId</span></span>
<span data-ttu-id="47e71-127">Идентификатор объекта группы.</span><span class="sxs-lookup"><span data-stu-id="47e71-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e71-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="47e71-128">-IncludeTotalCount</span></span>
<span data-ttu-id="47e71-129">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="47e71-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="47e71-130">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="47e71-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="47e71-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="47e71-131">-Skip</span></span>
<span data-ttu-id="47e71-132">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="47e71-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="47e71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e71-133">CommonParameters</span></span>
<span data-ttu-id="47e71-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47e71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e71-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e71-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e71-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47e71-136">INPUTS</span></span>

### <span data-ttu-id="47e71-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="47e71-137">System.Guid</span></span>

### <span data-ttu-id="47e71-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="47e71-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="47e71-139">Параметры: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47e71-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="47e71-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47e71-140">OUTPUTS</span></span>

### <span data-ttu-id="47e71-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="47e71-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="47e71-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="47e71-142">NOTES</span></span>

## <span data-ttu-id="47e71-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47e71-143">RELATED LINKS</span></span>

[<span data-ttu-id="47e71-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="47e71-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="47e71-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="47e71-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

