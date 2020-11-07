---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732585"
---
# <span data-ttu-id="28030-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28030-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="28030-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28030-102">SYNOPSIS</span></span>
<span data-ttu-id="28030-103">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28030-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28030-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28030-104">SYNTAX</span></span>

### <span data-ttu-id="28030-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28030-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28030-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="28030-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28030-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28030-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28030-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28030-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28030-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="28030-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28030-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="28030-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="28030-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28030-111">DESCRIPTION</span></span>
<span data-ttu-id="28030-112">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28030-112">Filters active directory users.</span></span>

## <span data-ttu-id="28030-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28030-113">EXAMPLES</span></span>

### <span data-ttu-id="28030-114">Пример 1: список всех пользователей</span><span class="sxs-lookup"><span data-stu-id="28030-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="28030-115">Выводит список всех пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="28030-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="28030-116">Пример 2: список всех пользователей, использующих разбиение по страницам</span><span class="sxs-lookup"><span data-stu-id="28030-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="28030-117">Список первых пользователей рекламы 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="28030-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="28030-118">Пример 3. получение пользователя рекламного объявления по имени субъекта-пользователя</span><span class="sxs-lookup"><span data-stu-id="28030-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="28030-119">Возвращает пользователя рекламы с основным именем пользователя " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="28030-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="28030-120">Пример 4: список по строке поиска</span><span class="sxs-lookup"><span data-stu-id="28030-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="28030-121">Список всех пользователей рекламы, отображаемое имя которых начинается с "Joe".</span><span class="sxs-lookup"><span data-stu-id="28030-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="28030-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28030-122">PARAMETERS</span></span>

### <span data-ttu-id="28030-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28030-123">-DefaultProfile</span></span>
<span data-ttu-id="28030-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="28030-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28030-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="28030-125">-DisplayName</span></span>
<span data-ttu-id="28030-126">Отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="28030-126">The display name of the user.</span></span>

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

### <span data-ttu-id="28030-127">-First</span><span class="sxs-lookup"><span data-stu-id="28030-127">-First</span></span>
<span data-ttu-id="28030-128">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="28030-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="28030-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="28030-129">-IncludeTotalCount</span></span>
<span data-ttu-id="28030-130">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="28030-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="28030-131">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="28030-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="28030-132">-Почта</span><span class="sxs-lookup"><span data-stu-id="28030-132">-Mail</span></span>
<span data-ttu-id="28030-133">Почта пользователя.</span><span class="sxs-lookup"><span data-stu-id="28030-133">The user mail.</span></span>

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

### <span data-ttu-id="28030-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="28030-134">-ObjectId</span></span>
<span data-ttu-id="28030-135">Идентификатор объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="28030-135">Object id of the user.</span></span>

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

### <span data-ttu-id="28030-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="28030-136">-Skip</span></span>
<span data-ttu-id="28030-137">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="28030-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="28030-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="28030-138">-StartsWith</span></span>
<span data-ttu-id="28030-139">Используется для поиска пользователей, начинающихся с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="28030-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="28030-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="28030-140">-UserPrincipalName</span></span>
<span data-ttu-id="28030-141">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="28030-141">UPN of the user.</span></span>

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

### <span data-ttu-id="28030-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28030-142">CommonParameters</span></span>
<span data-ttu-id="28030-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28030-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28030-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28030-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28030-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28030-145">INPUTS</span></span>

### <span data-ttu-id="28030-146">System. String</span><span class="sxs-lookup"><span data-stu-id="28030-146">System.String</span></span>

### <span data-ttu-id="28030-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="28030-147">System.Guid</span></span>

## <span data-ttu-id="28030-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28030-148">OUTPUTS</span></span>

### <span data-ttu-id="28030-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="28030-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="28030-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="28030-150">NOTES</span></span>

## <span data-ttu-id="28030-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28030-151">RELATED LINKS</span></span>

[<span data-ttu-id="28030-152">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28030-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="28030-153">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28030-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="28030-154">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28030-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

