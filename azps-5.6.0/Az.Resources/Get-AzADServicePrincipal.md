---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 659c2a026099eaa8764030b86a40d9ca6d4d2333
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961704"
---
# <span data-ttu-id="67f20-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="67f20-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="67f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f20-102">SYNOPSIS</span></span>
<span data-ttu-id="67f20-103">Фильтрует активных руководителей службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="67f20-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="67f20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67f20-104">SYNTAX</span></span>

### <span data-ttu-id="67f20-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67f20-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="67f20-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="67f20-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="67f20-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67f20-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="67f20-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67f20-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="67f20-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67f20-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="67f20-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67f20-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="67f20-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="67f20-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="67f20-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67f20-112">DESCRIPTION</span></span>
<span data-ttu-id="67f20-113">Фильтрует активных руководителей службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="67f20-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="67f20-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67f20-114">EXAMPLES</span></span>

### <span data-ttu-id="67f20-115">Пример 1. Основные принципы работы службы List AD</span><span class="sxs-lookup"><span data-stu-id="67f20-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="67f20-116">Список всех основных лиц служб AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="67f20-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="67f20-117">Пример 2. Список глав служб AD с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="67f20-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="67f20-118">Список первых 100 основных лиц служб AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="67f20-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="67f20-119">Пример 3. Списки участников-служб по spn</span><span class="sxs-lookup"><span data-stu-id="67f20-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="67f20-120">Список основных служб с spN "36f81fc3-b00f-48cd-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="67f20-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="67f20-121">Пример 4. Список глав служб по строке поиска</span><span class="sxs-lookup"><span data-stu-id="67f20-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="67f20-122">В этом списке перечислены все основные пользователи службЫ AD, отображаемая имя которых начинается с веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="67f20-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="67f20-123">Пример 5. Перечне основной суммы обслуживания путем piping</span><span class="sxs-lookup"><span data-stu-id="67f20-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="67f20-124">Получает приложение AD с ид объекта 39e64ec6-569b-4030-8e1c-c3c519a05d69' и передает его в Get-AzADServicePrincipal-Get-AzADServicePrincipal, чтобы перечислить всех участников обслуживания для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="67f20-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="67f20-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67f20-125">PARAMETERS</span></span>

### <span data-ttu-id="67f20-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67f20-126">-ApplicationId</span></span>
<span data-ttu-id="67f20-127">ИД приложения-службы.</span><span class="sxs-lookup"><span data-stu-id="67f20-127">The service principal application id.</span></span>

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

### <span data-ttu-id="67f20-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="67f20-128">-ApplicationObject</span></span>
<span data-ttu-id="67f20-129">Объект приложения, для которого извлекается основная служба.</span><span class="sxs-lookup"><span data-stu-id="67f20-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="67f20-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f20-130">-DefaultProfile</span></span>
<span data-ttu-id="67f20-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="67f20-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f20-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="67f20-132">-DisplayName</span></span>
<span data-ttu-id="67f20-133">Отображаемая имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="67f20-133">The service principal display name.</span></span>

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

### <span data-ttu-id="67f20-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="67f20-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="67f20-135">Строка поиска с основной строкой запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="67f20-135">The service principal search string.</span></span>

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

### <span data-ttu-id="67f20-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="67f20-136">-ObjectId</span></span>
<span data-ttu-id="67f20-137">Object id of the service principal.</span><span class="sxs-lookup"><span data-stu-id="67f20-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="67f20-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="67f20-138">-ServicePrincipalName</span></span>
<span data-ttu-id="67f20-139">SpN службы.</span><span class="sxs-lookup"><span data-stu-id="67f20-139">SPN of the service.</span></span>

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

### <span data-ttu-id="67f20-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="67f20-140">-IncludeTotalCount</span></span>
<span data-ttu-id="67f20-141">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="67f20-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="67f20-142">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="67f20-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="67f20-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="67f20-143">-Skip</span></span>
<span data-ttu-id="67f20-144">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="67f20-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="67f20-145">-First</span><span class="sxs-lookup"><span data-stu-id="67f20-145">-First</span></span>
<span data-ttu-id="67f20-146">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="67f20-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="67f20-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f20-147">CommonParameters</span></span>
<span data-ttu-id="67f20-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f20-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f20-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67f20-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f20-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67f20-150">INPUTS</span></span>

### <span data-ttu-id="67f20-151">System.String</span><span class="sxs-lookup"><span data-stu-id="67f20-151">System.String</span></span>

### <span data-ttu-id="67f20-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="67f20-152">System.Guid</span></span>

### <span data-ttu-id="67f20-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="67f20-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="67f20-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67f20-154">OUTPUTS</span></span>

### <span data-ttu-id="67f20-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="67f20-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="67f20-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67f20-156">NOTES</span></span>

## <span data-ttu-id="67f20-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67f20-157">RELATED LINKS</span></span>

[<span data-ttu-id="67f20-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="67f20-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="67f20-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="67f20-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="67f20-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="67f20-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="67f20-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="67f20-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="67f20-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="67f20-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

