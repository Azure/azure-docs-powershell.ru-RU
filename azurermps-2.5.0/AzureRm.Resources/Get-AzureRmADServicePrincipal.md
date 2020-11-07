---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 10d95102058c759f9b2641f233bd590364945c71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913750"
---
# <span data-ttu-id="cd284-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cd284-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="cd284-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd284-102">SYNOPSIS</span></span>
<span data-ttu-id="cd284-103">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cd284-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd284-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd284-104">SYNTAX</span></span>

### <span data-ttu-id="cd284-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd284-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cd284-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd284-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cd284-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd284-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cd284-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd284-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cd284-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd284-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cd284-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd284-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cd284-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd284-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="cd284-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd284-112">DESCRIPTION</span></span>
<span data-ttu-id="cd284-113">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cd284-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="cd284-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd284-114">EXAMPLES</span></span>

### <span data-ttu-id="cd284-115">Пример 1: список участников службы AD</span><span class="sxs-lookup"><span data-stu-id="cd284-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="cd284-116">Выводит список всех участников службы AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="cd284-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="cd284-117">Пример 2: список участников AD-службы с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="cd284-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="cd284-118">В этом списке указаны первые участники службы AD 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="cd284-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="cd284-119">Пример 3: список участников службы по имени SPN</span><span class="sxs-lookup"><span data-stu-id="cd284-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="cd284-120">Список участников-служб с именем участника-службы "36f81fc3-b00f-48cd-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="cd284-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="cd284-121">Пример 4: список субъектов-служб по строке поиска</span><span class="sxs-lookup"><span data-stu-id="cd284-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="cd284-122">Список всех участников службы AD, отображаемое имя которых начинается с "веб".</span><span class="sxs-lookup"><span data-stu-id="cd284-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="cd284-123">Пример 5: перечисление участников службы по конвейеру</span><span class="sxs-lookup"><span data-stu-id="cd284-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="cd284-124">Получает РЕКЛАМное приложение с идентификатором объекта "39e64ec6-569b-4030-8e1c-c3c519a05d69" и преобразует его в командлет Get-AzureRmADServicePrincipal, чтобы получить список всех участников-служб для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="cd284-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="cd284-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd284-125">PARAMETERS</span></span>

### <span data-ttu-id="cd284-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cd284-126">-ApplicationId</span></span>
<span data-ttu-id="cd284-127">Идентификатор приложения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="cd284-127">The service principal application id.</span></span>

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

### <span data-ttu-id="cd284-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="cd284-128">-ApplicationObject</span></span>
<span data-ttu-id="cd284-129">Объект приложения, для которого извлекается субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="cd284-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd284-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd284-130">-DefaultProfile</span></span>
<span data-ttu-id="cd284-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cd284-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd284-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd284-132">-DisplayName</span></span>
<span data-ttu-id="cd284-133">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="cd284-133">The service principal display name.</span></span>

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

### <span data-ttu-id="cd284-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="cd284-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="cd284-135">Строка поиска субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="cd284-135">The service principal search string.</span></span>

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

### <span data-ttu-id="cd284-136">-First</span><span class="sxs-lookup"><span data-stu-id="cd284-136">-First</span></span>
<span data-ttu-id="cd284-137">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="cd284-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="cd284-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="cd284-138">-IncludeTotalCount</span></span>
<span data-ttu-id="cd284-139">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="cd284-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="cd284-140">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="cd284-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="cd284-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cd284-141">-ObjectId</span></span>
<span data-ttu-id="cd284-142">Идентификатор объекта субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="cd284-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="cd284-143">-Намерено</span><span class="sxs-lookup"><span data-stu-id="cd284-143">-ServicePrincipalName</span></span>
<span data-ttu-id="cd284-144">SPN службы.</span><span class="sxs-lookup"><span data-stu-id="cd284-144">SPN of the service.</span></span>

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

### <span data-ttu-id="cd284-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="cd284-145">-Skip</span></span>
<span data-ttu-id="cd284-146">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="cd284-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cd284-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd284-147">CommonParameters</span></span>
<span data-ttu-id="cd284-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd284-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd284-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd284-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd284-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd284-150">INPUTS</span></span>

### <span data-ttu-id="cd284-151">System. String</span><span class="sxs-lookup"><span data-stu-id="cd284-151">System.String</span></span>

### <span data-ttu-id="cd284-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cd284-152">System.Guid</span></span>

### <span data-ttu-id="cd284-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="cd284-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="cd284-154">Параметры: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd284-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="cd284-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd284-155">OUTPUTS</span></span>

### <span data-ttu-id="cd284-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cd284-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="cd284-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd284-157">NOTES</span></span>

## <span data-ttu-id="cd284-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd284-158">RELATED LINKS</span></span>

[<span data-ttu-id="cd284-159">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cd284-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)



[<span data-ttu-id="cd284-160">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cd284-160">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="cd284-161">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cd284-161">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="cd284-162">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="cd284-162">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

