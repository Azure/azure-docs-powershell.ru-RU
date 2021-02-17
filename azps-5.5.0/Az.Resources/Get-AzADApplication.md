---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 68344fcafa16187651615c95ec2fb41d0bbbfb82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212977"
---
# <span data-ttu-id="7f283-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7f283-101">Get-AzADApplication</span></span>

## <span data-ttu-id="7f283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f283-102">SYNOPSIS</span></span>
<span data-ttu-id="7f283-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f283-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="7f283-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f283-104">SYNTAX</span></span>

### <span data-ttu-id="7f283-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f283-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7f283-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f283-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7f283-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f283-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7f283-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f283-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7f283-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f283-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7f283-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f283-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7f283-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f283-111">DESCRIPTION</span></span>
<span data-ttu-id="7f283-112">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f283-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="7f283-113">Для подметки приложений можно использовать ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="7f283-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="7f283-114">Если параметр не задан, извлекает все приложения в клиенте.</span><span class="sxs-lookup"><span data-stu-id="7f283-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="7f283-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f283-115">EXAMPLES</span></span>

### <span data-ttu-id="7f283-116">Пример 1. Список всех приложений</span><span class="sxs-lookup"><span data-stu-id="7f283-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="7f283-117">Список всех приложений, которые находятся в клиенте.</span><span class="sxs-lookup"><span data-stu-id="7f283-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="7f283-118">Пример 2. Список приложений с использованием разведки</span><span class="sxs-lookup"><span data-stu-id="7f283-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="7f283-119">Список первых 100 приложений для клиента.</span><span class="sxs-lookup"><span data-stu-id="7f283-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="7f283-120">Пример 3. Получение приложения по идентификатору URI</span><span class="sxs-lookup"><span data-stu-id="7f283-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="7f283-121">Возвращает приложение с идентификатором uri в качестве " http://mySecretApp1 " .</span><span class="sxs-lookup"><span data-stu-id="7f283-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="7f283-122">Пример 4. Получение приложения по ид объекта</span><span class="sxs-lookup"><span data-stu-id="7f283-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="7f283-123">Получает приложение с ид объекта '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span><span class="sxs-lookup"><span data-stu-id="7f283-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="7f283-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f283-124">PARAMETERS</span></span>

### <span data-ttu-id="7f283-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7f283-125">-ApplicationId</span></span>
<span data-ttu-id="7f283-126">ИД приложения для получения.</span><span class="sxs-lookup"><span data-stu-id="7f283-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="7f283-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f283-127">-DefaultProfile</span></span>
<span data-ttu-id="7f283-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7f283-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f283-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7f283-129">-DisplayName</span></span>
<span data-ttu-id="7f283-130">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="7f283-130">The display name of the application.</span></span>

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

### <span data-ttu-id="7f283-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="7f283-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="7f283-132">Получить все приложения, начиная с отображаемом имени.</span><span class="sxs-lookup"><span data-stu-id="7f283-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f283-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="7f283-133">-IdentifierUri</span></span>
<span data-ttu-id="7f283-134">Уникальный идентификатор Uri приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="7f283-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f283-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7f283-135">-ObjectId</span></span>
<span data-ttu-id="7f283-136">ИД объекта приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="7f283-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f283-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7f283-137">-IncludeTotalCount</span></span>
<span data-ttu-id="7f283-138">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="7f283-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="7f283-139">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="7f283-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="7f283-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="7f283-140">-Skip</span></span>
<span data-ttu-id="7f283-141">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="7f283-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="7f283-142">-First</span><span class="sxs-lookup"><span data-stu-id="7f283-142">-First</span></span>
<span data-ttu-id="7f283-143">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="7f283-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="7f283-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f283-144">CommonParameters</span></span>
<span data-ttu-id="7f283-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f283-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f283-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f283-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f283-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f283-147">INPUTS</span></span>

### <span data-ttu-id="7f283-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7f283-148">System.String</span></span>

### <span data-ttu-id="7f283-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7f283-149">System.Guid</span></span>

## <span data-ttu-id="7f283-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f283-150">OUTPUTS</span></span>

### <span data-ttu-id="7f283-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7f283-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7f283-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f283-152">NOTES</span></span>

## <span data-ttu-id="7f283-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f283-153">RELATED LINKS</span></span>

[<span data-ttu-id="7f283-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f283-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="7f283-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f283-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="7f283-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f283-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="7f283-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7f283-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="7f283-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7f283-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="7f283-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7f283-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

