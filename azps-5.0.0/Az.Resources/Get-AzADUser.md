---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 884d5086c8966da8622d48e85f5f4b3009fcc94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248207"
---
# <span data-ttu-id="78e84-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="78e84-101">Get-AzADUser</span></span>

## <span data-ttu-id="78e84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78e84-102">SYNOPSIS</span></span>
<span data-ttu-id="78e84-103">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78e84-103">Filters active directory users.</span></span>

## <span data-ttu-id="78e84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78e84-104">SYNTAX</span></span>

### <span data-ttu-id="78e84-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78e84-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78e84-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e84-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78e84-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e84-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78e84-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e84-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78e84-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e84-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78e84-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e84-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="78e84-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78e84-111">DESCRIPTION</span></span>
<span data-ttu-id="78e84-112">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78e84-112">Filters active directory users.</span></span>

## <span data-ttu-id="78e84-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78e84-113">EXAMPLES</span></span>

### <span data-ttu-id="78e84-114">Пример 1: список всех пользователей</span><span class="sxs-lookup"><span data-stu-id="78e84-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="78e84-115">Выводит список всех пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="78e84-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="78e84-116">Пример 2: список всех пользователей, использующих разбиение по страницам</span><span class="sxs-lookup"><span data-stu-id="78e84-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="78e84-117">Список первых пользователей рекламы 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="78e84-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="78e84-118">Пример 3: получение пользователя рекламы по имени субъекта-пользователя</span><span class="sxs-lookup"><span data-stu-id="78e84-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="78e84-119">Возвращает пользователя рекламы с основным именем пользователя " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="78e84-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="78e84-120">Пример 4: список по строке поиска</span><span class="sxs-lookup"><span data-stu-id="78e84-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="78e84-121">Список всех пользователей рекламы, отображаемое имя которых начинается с "Joe".</span><span class="sxs-lookup"><span data-stu-id="78e84-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="78e84-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78e84-122">PARAMETERS</span></span>

### <span data-ttu-id="78e84-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e84-123">-DefaultProfile</span></span>
<span data-ttu-id="78e84-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="78e84-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78e84-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78e84-125">-DisplayName</span></span>
<span data-ttu-id="78e84-126">Отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="78e84-126">The display name of the user.</span></span>

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

### <span data-ttu-id="78e84-127">-Почта</span><span class="sxs-lookup"><span data-stu-id="78e84-127">-Mail</span></span>
<span data-ttu-id="78e84-128">Почта пользователя.</span><span class="sxs-lookup"><span data-stu-id="78e84-128">The user mail.</span></span>

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

### <span data-ttu-id="78e84-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="78e84-129">-ObjectId</span></span>
<span data-ttu-id="78e84-130">Идентификатор объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="78e84-130">Object id of the user.</span></span>

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

### <span data-ttu-id="78e84-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="78e84-131">-StartsWith</span></span>
<span data-ttu-id="78e84-132">Используется для поиска пользователей, начинающихся с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="78e84-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="78e84-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="78e84-133">-UserPrincipalName</span></span>
<span data-ttu-id="78e84-134">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="78e84-134">UPN of the user.</span></span>

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

### <span data-ttu-id="78e84-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="78e84-135">-IncludeTotalCount</span></span>
<span data-ttu-id="78e84-136">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="78e84-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="78e84-137">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="78e84-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="78e84-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="78e84-138">-Skip</span></span>
<span data-ttu-id="78e84-139">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="78e84-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="78e84-140">-First</span><span class="sxs-lookup"><span data-stu-id="78e84-140">-First</span></span>
<span data-ttu-id="78e84-141">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="78e84-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="78e84-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e84-142">CommonParameters</span></span>
<span data-ttu-id="78e84-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78e84-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e84-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78e84-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e84-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78e84-145">INPUTS</span></span>

### <span data-ttu-id="78e84-146">System. String</span><span class="sxs-lookup"><span data-stu-id="78e84-146">System.String</span></span>

## <span data-ttu-id="78e84-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78e84-147">OUTPUTS</span></span>

### <span data-ttu-id="78e84-148">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="78e84-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="78e84-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="78e84-149">NOTES</span></span>

## <span data-ttu-id="78e84-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78e84-150">RELATED LINKS</span></span>

[<span data-ttu-id="78e84-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="78e84-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="78e84-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="78e84-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="78e84-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="78e84-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

