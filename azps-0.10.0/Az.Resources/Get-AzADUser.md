---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: b5690dfc1d85483b10fc7cd08606c4555784e8e0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398739"
---
# <span data-ttu-id="c9683-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c9683-101">Get-AzADUser</span></span>

## <span data-ttu-id="c9683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9683-102">SYNOPSIS</span></span>
<span data-ttu-id="c9683-103">Фильтрует активных пользователей каталогов.</span><span class="sxs-lookup"><span data-stu-id="c9683-103">Filters active directory users.</span></span>

## <span data-ttu-id="c9683-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9683-104">SYNTAX</span></span>

### <span data-ttu-id="c9683-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9683-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c9683-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9683-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c9683-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9683-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c9683-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9683-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c9683-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9683-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c9683-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9683-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c9683-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9683-111">DESCRIPTION</span></span>
<span data-ttu-id="c9683-112">Фильтрует активных пользователей каталогов.</span><span class="sxs-lookup"><span data-stu-id="c9683-112">Filters active directory users.</span></span>

## <span data-ttu-id="c9683-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9683-113">EXAMPLES</span></span>

### <span data-ttu-id="c9683-114">Пример 1. Список всех пользователей</span><span class="sxs-lookup"><span data-stu-id="c9683-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="c9683-115">Список всех пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="c9683-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="c9683-116">Пример 2. Список всех пользователей с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="c9683-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="c9683-117">Список первых 100 пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="c9683-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="c9683-118">Пример 3. Get AD user by user principal name</span><span class="sxs-lookup"><span data-stu-id="c9683-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="c9683-119">Возвращает пользователя AD с именем директора пользователя " foo@domain.com " .</span><span class="sxs-lookup"><span data-stu-id="c9683-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="c9683-120">Пример 4. Строка "Список по поиску"</span><span class="sxs-lookup"><span data-stu-id="c9683-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="c9683-121">Список всех пользователей AD, отображаемая имя которых начинается с "Сергей".</span><span class="sxs-lookup"><span data-stu-id="c9683-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="c9683-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9683-122">PARAMETERS</span></span>

### <span data-ttu-id="c9683-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9683-123">-DefaultProfile</span></span>
<span data-ttu-id="c9683-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c9683-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9683-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c9683-125">-DisplayName</span></span>
<span data-ttu-id="c9683-126">Отображаемая имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9683-126">The display name of the user.</span></span>

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

### <span data-ttu-id="c9683-127">-First</span><span class="sxs-lookup"><span data-stu-id="c9683-127">-First</span></span>
<span data-ttu-id="c9683-128">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="c9683-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="c9683-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c9683-129">-IncludeTotalCount</span></span>
<span data-ttu-id="c9683-130">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="c9683-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c9683-131">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="c9683-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="c9683-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="c9683-132">-Mail</span></span>
<span data-ttu-id="c9683-133">Почта пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9683-133">The user mail.</span></span>

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

### <span data-ttu-id="c9683-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c9683-134">-ObjectId</span></span>
<span data-ttu-id="c9683-135">ИД объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9683-135">Object id of the user.</span></span>

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

### <span data-ttu-id="c9683-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="c9683-136">-Skip</span></span>
<span data-ttu-id="c9683-137">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="c9683-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="c9683-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="c9683-138">-StartsWith</span></span>
<span data-ttu-id="c9683-139">Используется для поиска пользователей, которые начинаются с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="c9683-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="c9683-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c9683-140">-UserPrincipalName</span></span>
<span data-ttu-id="c9683-141">Имя пользователя(upn) пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9683-141">UPN of the user.</span></span>

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

### <span data-ttu-id="c9683-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9683-142">CommonParameters</span></span>
<span data-ttu-id="c9683-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9683-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9683-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9683-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9683-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9683-145">INPUTS</span></span>

### <span data-ttu-id="c9683-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c9683-146">System.String</span></span>

### <span data-ttu-id="c9683-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c9683-147">System.Guid</span></span>

## <span data-ttu-id="c9683-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9683-148">OUTPUTS</span></span>

### <span data-ttu-id="c9683-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="c9683-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="c9683-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9683-150">NOTES</span></span>

## <span data-ttu-id="c9683-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9683-151">RELATED LINKS</span></span>

[<span data-ttu-id="c9683-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c9683-152">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="c9683-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c9683-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

