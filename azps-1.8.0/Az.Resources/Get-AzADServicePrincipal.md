---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 0dc49732a6e6ad614a0330c3fe24b412be898a54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729452"
---
# <span data-ttu-id="d16bd-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d16bd-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="d16bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d16bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d16bd-103">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d16bd-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="d16bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d16bd-104">SYNTAX</span></span>

### <span data-ttu-id="d16bd-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d16bd-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d16bd-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16bd-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d16bd-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16bd-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d16bd-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16bd-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d16bd-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16bd-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d16bd-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16bd-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d16bd-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16bd-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d16bd-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d16bd-112">DESCRIPTION</span></span>
<span data-ttu-id="d16bd-113">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d16bd-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="d16bd-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d16bd-114">EXAMPLES</span></span>

### <span data-ttu-id="d16bd-115">Пример 1: список участников службы AD</span><span class="sxs-lookup"><span data-stu-id="d16bd-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="d16bd-116">Выводит список всех участников службы AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d16bd-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="d16bd-117">Пример 2: список участников AD-службы с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="d16bd-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="d16bd-118">В этом списке указаны первые участники службы AD 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d16bd-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="d16bd-119">Пример 3: список участников службы по имени SPN</span><span class="sxs-lookup"><span data-stu-id="d16bd-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="d16bd-120">Список участников-служб с именем участника-службы "36f81fc3-b00f-48cd-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="d16bd-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="d16bd-121">Пример 4: список субъектов-служб по строке поиска</span><span class="sxs-lookup"><span data-stu-id="d16bd-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="d16bd-122">Список всех участников службы AD, отображаемое имя которых начинается с "веб".</span><span class="sxs-lookup"><span data-stu-id="d16bd-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="d16bd-123">Пример 5: перечисление участников службы по конвейеру</span><span class="sxs-lookup"><span data-stu-id="d16bd-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="d16bd-124">Получает РЕКЛАМное приложение с идентификатором объекта "39e64ec6-569b-4030-8e1c-c3c519a05d69" и преобразует его в командлет Get-AzADServicePrincipal, чтобы получить список всех участников-служб для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="d16bd-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="d16bd-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d16bd-125">PARAMETERS</span></span>

### <span data-ttu-id="d16bd-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d16bd-126">-ApplicationId</span></span>
<span data-ttu-id="d16bd-127">Идентификатор приложения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d16bd-127">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16bd-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d16bd-128">-ApplicationObject</span></span>
<span data-ttu-id="d16bd-129">Объект приложения, для которого извлекается субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="d16bd-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d16bd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16bd-130">-DefaultProfile</span></span>
<span data-ttu-id="d16bd-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d16bd-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d16bd-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d16bd-132">-DisplayName</span></span>
<span data-ttu-id="d16bd-133">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d16bd-133">The service principal display name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16bd-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="d16bd-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="d16bd-135">Строка поиска субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d16bd-135">The service principal search string.</span></span>

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

### <span data-ttu-id="d16bd-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d16bd-136">-ObjectId</span></span>
<span data-ttu-id="d16bd-137">Идентификатор объекта субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d16bd-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="d16bd-138">-Намерено</span><span class="sxs-lookup"><span data-stu-id="d16bd-138">-ServicePrincipalName</span></span>
<span data-ttu-id="d16bd-139">SPN службы.</span><span class="sxs-lookup"><span data-stu-id="d16bd-139">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16bd-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d16bd-140">-IncludeTotalCount</span></span>
<span data-ttu-id="d16bd-141">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="d16bd-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d16bd-142">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="d16bd-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d16bd-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="d16bd-143">-Skip</span></span>
<span data-ttu-id="d16bd-144">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="d16bd-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="d16bd-145">-First</span><span class="sxs-lookup"><span data-stu-id="d16bd-145">-First</span></span>
<span data-ttu-id="d16bd-146">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="d16bd-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="d16bd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16bd-147">CommonParameters</span></span>
<span data-ttu-id="d16bd-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d16bd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16bd-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d16bd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16bd-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d16bd-150">INPUTS</span></span>

### <span data-ttu-id="d16bd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d16bd-151">System.String</span></span>

### <span data-ttu-id="d16bd-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d16bd-152">System.Guid</span></span>

### <span data-ttu-id="d16bd-153">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d16bd-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d16bd-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d16bd-154">OUTPUTS</span></span>

### <span data-ttu-id="d16bd-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d16bd-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="d16bd-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="d16bd-156">NOTES</span></span>

## <span data-ttu-id="d16bd-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d16bd-157">RELATED LINKS</span></span>

[<span data-ttu-id="d16bd-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d16bd-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="d16bd-159">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d16bd-159">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="d16bd-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d16bd-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="d16bd-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d16bd-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="d16bd-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d16bd-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

