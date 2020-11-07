---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910961"
---
# <span data-ttu-id="00939-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="00939-101">Get-AzADUser</span></span>

## <span data-ttu-id="00939-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00939-102">SYNOPSIS</span></span>
<span data-ttu-id="00939-103">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00939-103">Filters active directory users.</span></span>

## <span data-ttu-id="00939-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00939-104">SYNTAX</span></span>

### <span data-ttu-id="00939-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00939-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00939-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="00939-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00939-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00939-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00939-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00939-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00939-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="00939-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00939-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="00939-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="00939-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00939-111">DESCRIPTION</span></span>
<span data-ttu-id="00939-112">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00939-112">Filters active directory users.</span></span>

## <span data-ttu-id="00939-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00939-113">EXAMPLES</span></span>

### <span data-ttu-id="00939-114">Пример 1: список всех пользователей</span><span class="sxs-lookup"><span data-stu-id="00939-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="00939-115">Выводит список всех пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="00939-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="00939-116">Пример 2: список всех пользователей, использующих разбиение по страницам</span><span class="sxs-lookup"><span data-stu-id="00939-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="00939-117">Список первых пользователей рекламы 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="00939-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="00939-118">Пример 3. получение пользователя рекламного объявления по имени субъекта-пользователя</span><span class="sxs-lookup"><span data-stu-id="00939-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="00939-119">Возвращает пользователя рекламы с основным именем пользователя " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="00939-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="00939-120">Пример 4: список по строке поиска</span><span class="sxs-lookup"><span data-stu-id="00939-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="00939-121">Список всех пользователей рекламы, отображаемое имя которых начинается с "Joe".</span><span class="sxs-lookup"><span data-stu-id="00939-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="00939-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00939-122">PARAMETERS</span></span>

### <span data-ttu-id="00939-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00939-123">-DefaultProfile</span></span>
<span data-ttu-id="00939-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="00939-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00939-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="00939-125">-DisplayName</span></span>
<span data-ttu-id="00939-126">Отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="00939-126">The display name of the user.</span></span>

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

### <span data-ttu-id="00939-127">-First</span><span class="sxs-lookup"><span data-stu-id="00939-127">-First</span></span>
<span data-ttu-id="00939-128">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="00939-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="00939-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="00939-129">-IncludeTotalCount</span></span>
<span data-ttu-id="00939-130">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="00939-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="00939-131">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="00939-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="00939-132">-Почта</span><span class="sxs-lookup"><span data-stu-id="00939-132">-Mail</span></span>
<span data-ttu-id="00939-133">Почта пользователя.</span><span class="sxs-lookup"><span data-stu-id="00939-133">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00939-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="00939-134">-ObjectId</span></span>
<span data-ttu-id="00939-135">Идентификатор объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="00939-135">Object id of the user.</span></span>

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

### <span data-ttu-id="00939-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="00939-136">-Skip</span></span>
<span data-ttu-id="00939-137">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="00939-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="00939-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="00939-138">-StartsWith</span></span>
<span data-ttu-id="00939-139">Используется для поиска пользователей, начинающихся с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="00939-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="00939-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="00939-140">-UserPrincipalName</span></span>
<span data-ttu-id="00939-141">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="00939-141">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00939-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00939-142">CommonParameters</span></span>
<span data-ttu-id="00939-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00939-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00939-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00939-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00939-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00939-145">INPUTS</span></span>

### <span data-ttu-id="00939-146">System. String</span><span class="sxs-lookup"><span data-stu-id="00939-146">System.String</span></span>

### <span data-ttu-id="00939-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="00939-147">System.Guid</span></span>

## <span data-ttu-id="00939-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00939-148">OUTPUTS</span></span>

### <span data-ttu-id="00939-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="00939-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="00939-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="00939-150">NOTES</span></span>

## <span data-ttu-id="00939-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00939-151">RELATED LINKS</span></span>

[<span data-ttu-id="00939-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="00939-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="00939-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="00939-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="00939-154">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="00939-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

