---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: b467d629b578e9f9883dac4c0a8e268f9007a373
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212964"
---
# <span data-ttu-id="96a53-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="96a53-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="96a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a53-102">SYNOPSIS</span></span>
<span data-ttu-id="96a53-103">Фильтрует активных руководителей службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="96a53-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="96a53-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96a53-104">SYNTAX</span></span>

### <span data-ttu-id="96a53-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96a53-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="96a53-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a53-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="96a53-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a53-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="96a53-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a53-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="96a53-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a53-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="96a53-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a53-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="96a53-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a53-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="96a53-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96a53-112">DESCRIPTION</span></span>
<span data-ttu-id="96a53-113">Фильтрует активных руководителей службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="96a53-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="96a53-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96a53-114">EXAMPLES</span></span>

### <span data-ttu-id="96a53-115">Пример 1. Основные принципы работы службы List AD</span><span class="sxs-lookup"><span data-stu-id="96a53-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="96a53-116">Список всех основных лиц служб AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="96a53-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="96a53-117">Пример 2. Список глав служб AD с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="96a53-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="96a53-118">Список первых 100 основных лиц служб AD в клиенте.</span><span class="sxs-lookup"><span data-stu-id="96a53-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="96a53-119">Пример 3. Списки участников-служб по spn</span><span class="sxs-lookup"><span data-stu-id="96a53-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="96a53-120">Список основных служб с spN "36f81fc3-b00f-48cd-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="96a53-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="96a53-121">Пример 4. Список глав служб по строке поиска</span><span class="sxs-lookup"><span data-stu-id="96a53-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="96a53-122">В этой списке перечислены все основные пользователи службЫ AD, отображаемая имя которых начинается с веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="96a53-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="96a53-123">Пример 5. Перечне основной суммы обслуживания путем piping</span><span class="sxs-lookup"><span data-stu-id="96a53-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="96a53-124">Получает приложение AD с ид объекта 39e64ec6-569b-4030-8e1c-c3c519a05d69' и передает его в Get-AzADServicePrincipal-Get-AzADServicePrincipal для списка всех участников-служб для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="96a53-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="96a53-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96a53-125">PARAMETERS</span></span>

### <span data-ttu-id="96a53-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="96a53-126">-ApplicationId</span></span>
<span data-ttu-id="96a53-127">ИД приложения-службы.</span><span class="sxs-lookup"><span data-stu-id="96a53-127">The service principal application id.</span></span>

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

### <span data-ttu-id="96a53-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="96a53-128">-ApplicationObject</span></span>
<span data-ttu-id="96a53-129">Объект приложения, для которого извлекается основная служба.</span><span class="sxs-lookup"><span data-stu-id="96a53-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="96a53-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a53-130">-DefaultProfile</span></span>
<span data-ttu-id="96a53-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96a53-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96a53-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="96a53-132">-DisplayName</span></span>
<span data-ttu-id="96a53-133">Отображаемая имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="96a53-133">The service principal display name.</span></span>

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

### <span data-ttu-id="96a53-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="96a53-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="96a53-135">Строка поиска с основной строкой запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="96a53-135">The service principal search string.</span></span>

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

### <span data-ttu-id="96a53-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="96a53-136">-ObjectId</span></span>
<span data-ttu-id="96a53-137">Object id of the service principal.</span><span class="sxs-lookup"><span data-stu-id="96a53-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="96a53-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="96a53-138">-ServicePrincipalName</span></span>
<span data-ttu-id="96a53-139">SpN службы.</span><span class="sxs-lookup"><span data-stu-id="96a53-139">SPN of the service.</span></span>

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

### <span data-ttu-id="96a53-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="96a53-140">-IncludeTotalCount</span></span>
<span data-ttu-id="96a53-141">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="96a53-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="96a53-142">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="96a53-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="96a53-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="96a53-143">-Skip</span></span>
<span data-ttu-id="96a53-144">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="96a53-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="96a53-145">-First</span><span class="sxs-lookup"><span data-stu-id="96a53-145">-First</span></span>
<span data-ttu-id="96a53-146">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="96a53-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="96a53-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a53-147">CommonParameters</span></span>
<span data-ttu-id="96a53-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a53-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a53-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96a53-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a53-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96a53-150">INPUTS</span></span>

### <span data-ttu-id="96a53-151">System.String</span><span class="sxs-lookup"><span data-stu-id="96a53-151">System.String</span></span>

### <span data-ttu-id="96a53-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="96a53-152">System.Guid</span></span>

### <span data-ttu-id="96a53-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="96a53-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="96a53-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96a53-154">OUTPUTS</span></span>

### <span data-ttu-id="96a53-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="96a53-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="96a53-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96a53-156">NOTES</span></span>

## <span data-ttu-id="96a53-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96a53-157">RELATED LINKS</span></span>

[<span data-ttu-id="96a53-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="96a53-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="96a53-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="96a53-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="96a53-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="96a53-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="96a53-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="96a53-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="96a53-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="96a53-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

