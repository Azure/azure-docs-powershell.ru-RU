---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 1b8a1c5c0a8161993be4d1e8c5f8d4bf9119d4b0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404281"
---
# <span data-ttu-id="e1aa3-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e1aa3-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="e1aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1aa3-103">Фильтрует активных руководителей службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="e1aa3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1aa3-104">SYNTAX</span></span>

### <span data-ttu-id="e1aa3-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1aa3-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e1aa3-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1aa3-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e1aa3-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1aa3-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e1aa3-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1aa3-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e1aa3-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1aa3-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e1aa3-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1aa3-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e1aa3-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1aa3-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e1aa3-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1aa3-112">DESCRIPTION</span></span>
<span data-ttu-id="e1aa3-113">Фильтрует активных руководителей службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="e1aa3-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1aa3-114">EXAMPLES</span></span>

### <span data-ttu-id="e1aa3-115">Пример 1. Основные принципы работы службы List AD</span><span class="sxs-lookup"><span data-stu-id="e1aa3-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="e1aa3-116">Список всех основных лиц служб AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="e1aa3-117">Пример 2. Основные принципы работы службы List AD с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="e1aa3-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="e1aa3-118">Список первых 100 основных лиц служб AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="e1aa3-119">Пример 3. Основные принципы обслуживания списков по spn</span><span class="sxs-lookup"><span data-stu-id="e1aa3-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="e1aa3-120">Список основных служб с spN "36f81fc3-b00f-48cd-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="e1aa3-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="e1aa3-121">Пример 4. Список глав служб по строке поиска</span><span class="sxs-lookup"><span data-stu-id="e1aa3-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="e1aa3-122">В этой списке перечислены все основные пользователи службЫ AD, отображаемая имя которых начинается с веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="e1aa3-123">Пример 5. Основные стороны служб списка путем перена доверений</span><span class="sxs-lookup"><span data-stu-id="e1aa3-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="e1aa3-124">Получает приложение AD с ид объекта 39e64ec6-569b-4030-8e1c-c3c519a05d69' и передает его в Get-AzADServicePrincipal-Get-AzADServicePrincipal, чтобы перечислить всех участников обслуживания для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="e1aa3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1aa3-125">PARAMETERS</span></span>

### <span data-ttu-id="e1aa3-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e1aa3-126">-ApplicationId</span></span>
<span data-ttu-id="e1aa3-127">ИД приложения-службы.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-127">The service principal application id.</span></span>

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

### <span data-ttu-id="e1aa3-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e1aa3-128">-ApplicationObject</span></span>
<span data-ttu-id="e1aa3-129">Объект приложения, для которого извлекется основной-сервис.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="e1aa3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1aa3-130">-DefaultProfile</span></span>
<span data-ttu-id="e1aa3-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e1aa3-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1aa3-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1aa3-132">-DisplayName</span></span>
<span data-ttu-id="e1aa3-133">Отображаемая имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-133">The service principal display name.</span></span>

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

### <span data-ttu-id="e1aa3-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="e1aa3-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="e1aa3-135">Строка поиска с основной строкой запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-135">The service principal search string.</span></span>

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

### <span data-ttu-id="e1aa3-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e1aa3-136">-ObjectId</span></span>
<span data-ttu-id="e1aa3-137">Object id of the service principal.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="e1aa3-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e1aa3-138">-ServicePrincipalName</span></span>
<span data-ttu-id="e1aa3-139">SpN службы.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-139">SPN of the service.</span></span>

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

### <span data-ttu-id="e1aa3-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e1aa3-140">-IncludeTotalCount</span></span>
<span data-ttu-id="e1aa3-141">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e1aa3-142">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e1aa3-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="e1aa3-143">-Skip</span></span>
<span data-ttu-id="e1aa3-144">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="e1aa3-145">-First</span><span class="sxs-lookup"><span data-stu-id="e1aa3-145">-First</span></span>
<span data-ttu-id="e1aa3-146">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="e1aa3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1aa3-147">CommonParameters</span></span>
<span data-ttu-id="e1aa3-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1aa3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1aa3-149">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1aa3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1aa3-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1aa3-150">INPUTS</span></span>

### <span data-ttu-id="e1aa3-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e1aa3-151">System.String</span></span>

### <span data-ttu-id="e1aa3-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e1aa3-152">System.Guid</span></span>

### <span data-ttu-id="e1aa3-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e1aa3-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e1aa3-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1aa3-154">OUTPUTS</span></span>

### <span data-ttu-id="e1aa3-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e1aa3-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e1aa3-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1aa3-156">NOTES</span></span>

## <span data-ttu-id="e1aa3-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1aa3-157">RELATED LINKS</span></span>

[<span data-ttu-id="e1aa3-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e1aa3-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)


[<span data-ttu-id="e1aa3-159">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e1aa3-159">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="e1aa3-160">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e1aa3-160">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="e1aa3-161">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e1aa3-161">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

