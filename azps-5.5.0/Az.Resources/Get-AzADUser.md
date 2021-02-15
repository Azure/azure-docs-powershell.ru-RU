---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 884d5086c8966da8622d48e85f5f4b3009fcc94f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217761"
---
# <span data-ttu-id="be956-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="be956-101">Get-AzADUser</span></span>

## <span data-ttu-id="be956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be956-102">SYNOPSIS</span></span>
<span data-ttu-id="be956-103">Фильтрует активных пользователей каталогов.</span><span class="sxs-lookup"><span data-stu-id="be956-103">Filters active directory users.</span></span>

## <span data-ttu-id="be956-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be956-104">SYNTAX</span></span>

### <span data-ttu-id="be956-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be956-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="be956-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="be956-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="be956-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be956-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="be956-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be956-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="be956-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="be956-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="be956-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="be956-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="be956-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be956-111">DESCRIPTION</span></span>
<span data-ttu-id="be956-112">Фильтрует активных пользователей каталогов.</span><span class="sxs-lookup"><span data-stu-id="be956-112">Filters active directory users.</span></span>

## <span data-ttu-id="be956-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be956-113">EXAMPLES</span></span>

### <span data-ttu-id="be956-114">Пример 1. Список всех пользователей</span><span class="sxs-lookup"><span data-stu-id="be956-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="be956-115">Список всех пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="be956-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="be956-116">Пример 2. Список всех пользователей с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="be956-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="be956-117">Список первых 100 пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="be956-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="be956-118">Пример 3. Get AD user by user principal name</span><span class="sxs-lookup"><span data-stu-id="be956-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="be956-119">Возвращает пользователя AD с именем директора пользователя " foo@domain.com " .</span><span class="sxs-lookup"><span data-stu-id="be956-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="be956-120">Пример 4. Строка "Список по поиску"</span><span class="sxs-lookup"><span data-stu-id="be956-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="be956-121">Список всех пользователей AD, отображаемая имя которых начинается с "Сергей".</span><span class="sxs-lookup"><span data-stu-id="be956-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="be956-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be956-122">PARAMETERS</span></span>

### <span data-ttu-id="be956-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be956-123">-DefaultProfile</span></span>
<span data-ttu-id="be956-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="be956-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be956-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="be956-125">-DisplayName</span></span>
<span data-ttu-id="be956-126">Отображаемая имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="be956-126">The display name of the user.</span></span>

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

### <span data-ttu-id="be956-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="be956-127">-Mail</span></span>
<span data-ttu-id="be956-128">Почта пользователя.</span><span class="sxs-lookup"><span data-stu-id="be956-128">The user mail.</span></span>

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

### <span data-ttu-id="be956-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="be956-129">-ObjectId</span></span>
<span data-ttu-id="be956-130">ИД объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="be956-130">Object id of the user.</span></span>

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

### <span data-ttu-id="be956-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="be956-131">-StartsWith</span></span>
<span data-ttu-id="be956-132">Используется для поиска пользователей, которые начинаются с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="be956-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="be956-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="be956-133">-UserPrincipalName</span></span>
<span data-ttu-id="be956-134">Имя пользователя(upn) пользователя.</span><span class="sxs-lookup"><span data-stu-id="be956-134">UPN of the user.</span></span>

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

### <span data-ttu-id="be956-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="be956-135">-IncludeTotalCount</span></span>
<span data-ttu-id="be956-136">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="be956-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="be956-137">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="be956-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="be956-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="be956-138">-Skip</span></span>
<span data-ttu-id="be956-139">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="be956-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="be956-140">-First</span><span class="sxs-lookup"><span data-stu-id="be956-140">-First</span></span>
<span data-ttu-id="be956-141">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="be956-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="be956-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be956-142">CommonParameters</span></span>
<span data-ttu-id="be956-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be956-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be956-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be956-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be956-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be956-145">INPUTS</span></span>

### <span data-ttu-id="be956-146">System.String</span><span class="sxs-lookup"><span data-stu-id="be956-146">System.String</span></span>

## <span data-ttu-id="be956-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be956-147">OUTPUTS</span></span>

### <span data-ttu-id="be956-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="be956-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="be956-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be956-149">NOTES</span></span>

## <span data-ttu-id="be956-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be956-150">RELATED LINKS</span></span>

[<span data-ttu-id="be956-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="be956-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="be956-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="be956-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="be956-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="be956-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

