---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 80df38532d5d5ce14b27f40bed04678e80752fca
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407001"
---
# <span data-ttu-id="4e307-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4e307-101">Get-AzADUser</span></span>

## <span data-ttu-id="4e307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e307-102">SYNOPSIS</span></span>
<span data-ttu-id="4e307-103">Фильтрует активных пользователей каталогов.</span><span class="sxs-lookup"><span data-stu-id="4e307-103">Filters active directory users.</span></span>

## <span data-ttu-id="4e307-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e307-104">SYNTAX</span></span>

### <span data-ttu-id="4e307-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e307-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4e307-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e307-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4e307-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e307-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4e307-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e307-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4e307-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e307-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4e307-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e307-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4e307-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e307-111">DESCRIPTION</span></span>
<span data-ttu-id="4e307-112">Фильтрует активных пользователей каталогов.</span><span class="sxs-lookup"><span data-stu-id="4e307-112">Filters active directory users.</span></span>

## <span data-ttu-id="4e307-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e307-113">EXAMPLES</span></span>

### <span data-ttu-id="4e307-114">Пример 1. Список всех пользователей</span><span class="sxs-lookup"><span data-stu-id="4e307-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="4e307-115">Список всех пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="4e307-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="4e307-116">Пример 2. Список всех пользователей с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="4e307-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="4e307-117">Список первых 100 пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="4e307-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="4e307-118">Пример 3. Get AD user by user principal name</span><span class="sxs-lookup"><span data-stu-id="4e307-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="4e307-119">Возвращает пользователя AD с именем директора пользователя " foo@domain.com " .</span><span class="sxs-lookup"><span data-stu-id="4e307-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="4e307-120">Пример 4. Строка "Список по поиску"</span><span class="sxs-lookup"><span data-stu-id="4e307-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="4e307-121">Список всех пользователей AD, отображаемая имя которых начинается с "Сергей".</span><span class="sxs-lookup"><span data-stu-id="4e307-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="4e307-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e307-122">PARAMETERS</span></span>

### <span data-ttu-id="4e307-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e307-123">-DefaultProfile</span></span>
<span data-ttu-id="4e307-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4e307-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e307-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4e307-125">-DisplayName</span></span>
<span data-ttu-id="4e307-126">Отображаемая имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e307-126">The display name of the user.</span></span>

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

### <span data-ttu-id="4e307-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="4e307-127">-Mail</span></span>
<span data-ttu-id="4e307-128">Почта пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e307-128">The user mail.</span></span>

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

### <span data-ttu-id="4e307-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4e307-129">-ObjectId</span></span>
<span data-ttu-id="4e307-130">ИД объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e307-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e307-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="4e307-131">-StartsWith</span></span>
<span data-ttu-id="4e307-132">Используется для поиска пользователей, которые начинаются с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="4e307-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="4e307-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4e307-133">-UserPrincipalName</span></span>
<span data-ttu-id="4e307-134">Имя пользователя(upn) пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e307-134">UPN of the user.</span></span>

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

### <span data-ttu-id="4e307-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4e307-135">-IncludeTotalCount</span></span>
<span data-ttu-id="4e307-136">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="4e307-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="4e307-137">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="4e307-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="4e307-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="4e307-138">-Skip</span></span>
<span data-ttu-id="4e307-139">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="4e307-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="4e307-140">-First</span><span class="sxs-lookup"><span data-stu-id="4e307-140">-First</span></span>
<span data-ttu-id="4e307-141">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="4e307-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="4e307-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e307-142">CommonParameters</span></span>
<span data-ttu-id="4e307-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e307-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e307-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e307-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e307-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e307-145">INPUTS</span></span>

### <span data-ttu-id="4e307-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4e307-146">System.String</span></span>

## <span data-ttu-id="4e307-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e307-147">OUTPUTS</span></span>

### <span data-ttu-id="4e307-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="4e307-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="4e307-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e307-149">NOTES</span></span>

## <span data-ttu-id="4e307-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e307-150">RELATED LINKS</span></span>

[<span data-ttu-id="4e307-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4e307-151">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="4e307-152">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4e307-152">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

