---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 78523d5bef3bfb2461bb524044da14f8aedbbc12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914001"
---
# <span data-ttu-id="71eba-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="71eba-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="71eba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71eba-102">SYNOPSIS</span></span>
<span data-ttu-id="71eba-103">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71eba-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71eba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71eba-104">SYNTAX</span></span>

### <span data-ttu-id="71eba-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71eba-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71eba-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="71eba-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71eba-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71eba-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71eba-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71eba-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71eba-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="71eba-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71eba-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="71eba-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="71eba-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71eba-111">DESCRIPTION</span></span>
<span data-ttu-id="71eba-112">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71eba-112">Filters active directory users.</span></span>

## <span data-ttu-id="71eba-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71eba-113">EXAMPLES</span></span>

### <span data-ttu-id="71eba-114">Пример 1: список всех пользователей</span><span class="sxs-lookup"><span data-stu-id="71eba-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="71eba-115">Выводит список всех пользователей AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71eba-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="71eba-116">Пример 2: список всех пользователей, использующих разбиение по страницам</span><span class="sxs-lookup"><span data-stu-id="71eba-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="71eba-117">Список первых пользователей рекламы 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71eba-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="71eba-118">Пример 3. получение пользователя рекламного объявления по имени субъекта-пользователя</span><span class="sxs-lookup"><span data-stu-id="71eba-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="71eba-119">Возвращает пользователя рекламы с основным именем пользователя " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="71eba-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="71eba-120">Пример 4: список по строке поиска</span><span class="sxs-lookup"><span data-stu-id="71eba-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="71eba-121">Список всех пользователей рекламы, отображаемое имя которых начинается с "Joe".</span><span class="sxs-lookup"><span data-stu-id="71eba-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="71eba-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71eba-122">PARAMETERS</span></span>

### <span data-ttu-id="71eba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71eba-123">-DefaultProfile</span></span>
<span data-ttu-id="71eba-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71eba-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71eba-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="71eba-125">-DisplayName</span></span>
<span data-ttu-id="71eba-126">Отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="71eba-126">The display name of the user.</span></span>

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

### <span data-ttu-id="71eba-127">-First</span><span class="sxs-lookup"><span data-stu-id="71eba-127">-First</span></span>
<span data-ttu-id="71eba-128">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="71eba-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="71eba-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="71eba-129">-IncludeTotalCount</span></span>
<span data-ttu-id="71eba-130">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="71eba-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="71eba-131">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="71eba-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="71eba-132">-Почта</span><span class="sxs-lookup"><span data-stu-id="71eba-132">-Mail</span></span>
<span data-ttu-id="71eba-133">Почта пользователя.</span><span class="sxs-lookup"><span data-stu-id="71eba-133">The user mail.</span></span>

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

### <span data-ttu-id="71eba-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="71eba-134">-ObjectId</span></span>
<span data-ttu-id="71eba-135">Идентификатор объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="71eba-135">Object id of the user.</span></span>

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

### <span data-ttu-id="71eba-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="71eba-136">-Skip</span></span>
<span data-ttu-id="71eba-137">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="71eba-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="71eba-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="71eba-138">-StartsWith</span></span>
<span data-ttu-id="71eba-139">Используется для поиска пользователей, начинающихся с предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="71eba-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="71eba-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="71eba-140">-UserPrincipalName</span></span>
<span data-ttu-id="71eba-141">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="71eba-141">UPN of the user.</span></span>

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

### <span data-ttu-id="71eba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71eba-142">CommonParameters</span></span>
<span data-ttu-id="71eba-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71eba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71eba-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71eba-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71eba-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71eba-145">INPUTS</span></span>

### <span data-ttu-id="71eba-146">System. String</span><span class="sxs-lookup"><span data-stu-id="71eba-146">System.String</span></span>

### <span data-ttu-id="71eba-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="71eba-147">System.Guid</span></span>

## <span data-ttu-id="71eba-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71eba-148">OUTPUTS</span></span>

### <span data-ttu-id="71eba-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="71eba-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="71eba-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="71eba-150">NOTES</span></span>

## <span data-ttu-id="71eba-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71eba-151">RELATED LINKS</span></span>

[<span data-ttu-id="71eba-152">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="71eba-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)



[<span data-ttu-id="71eba-153">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="71eba-153">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

