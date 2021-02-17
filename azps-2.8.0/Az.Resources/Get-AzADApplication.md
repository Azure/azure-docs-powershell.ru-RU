---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 545722e48095f8b77104bb6ff24b856bd76e3312
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407817"
---
# <span data-ttu-id="efcaf-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="efcaf-101">Get-AzADApplication</span></span>

## <span data-ttu-id="efcaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="efcaf-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efcaf-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="efcaf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="efcaf-104">SYNTAX</span></span>

### <span data-ttu-id="efcaf-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efcaf-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="efcaf-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efcaf-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="efcaf-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efcaf-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="efcaf-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="efcaf-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="efcaf-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="efcaf-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="efcaf-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="efcaf-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="efcaf-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efcaf-111">DESCRIPTION</span></span>
<span data-ttu-id="efcaf-112">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efcaf-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="efcaf-113">Для подметки приложений можно использовать ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="efcaf-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="efcaf-114">Если параметр не задан, извлекает все приложения в клиенте.</span><span class="sxs-lookup"><span data-stu-id="efcaf-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="efcaf-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="efcaf-115">EXAMPLES</span></span>

### <span data-ttu-id="efcaf-116">Пример 1. Список всех приложений</span><span class="sxs-lookup"><span data-stu-id="efcaf-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="efcaf-117">Список всех приложений, которые находятся в клиенте.</span><span class="sxs-lookup"><span data-stu-id="efcaf-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="efcaf-118">Пример 2. Список приложений с использованием разведки</span><span class="sxs-lookup"><span data-stu-id="efcaf-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="efcaf-119">Список первых 100 приложений для клиента.</span><span class="sxs-lookup"><span data-stu-id="efcaf-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="efcaf-120">Пример 3. Получение приложения по идентификатору URI</span><span class="sxs-lookup"><span data-stu-id="efcaf-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="efcaf-121">Возвращает приложение с идентификатором uri в качестве " http://mySecretApp1 " .</span><span class="sxs-lookup"><span data-stu-id="efcaf-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="efcaf-122">Пример 4. Получение приложения по ид объекта</span><span class="sxs-lookup"><span data-stu-id="efcaf-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="efcaf-123">Получает приложение с ид объекта '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span><span class="sxs-lookup"><span data-stu-id="efcaf-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="efcaf-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efcaf-124">PARAMETERS</span></span>

### <span data-ttu-id="efcaf-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="efcaf-125">-ApplicationId</span></span>
<span data-ttu-id="efcaf-126">ИД приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="efcaf-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="efcaf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcaf-127">-DefaultProfile</span></span>
<span data-ttu-id="efcaf-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="efcaf-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efcaf-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="efcaf-129">-DisplayName</span></span>
<span data-ttu-id="efcaf-130">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="efcaf-130">The display name of the application.</span></span>

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

### <span data-ttu-id="efcaf-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="efcaf-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="efcaf-132">Получить все приложения, начиная с отображаемом имени.</span><span class="sxs-lookup"><span data-stu-id="efcaf-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="efcaf-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="efcaf-133">-IdentifierUri</span></span>
<span data-ttu-id="efcaf-134">Уникальный идентификатор Uri приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="efcaf-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="efcaf-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="efcaf-135">-ObjectId</span></span>
<span data-ttu-id="efcaf-136">ИД объекта приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="efcaf-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="efcaf-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="efcaf-137">-IncludeTotalCount</span></span>
<span data-ttu-id="efcaf-138">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="efcaf-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="efcaf-139">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="efcaf-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="efcaf-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="efcaf-140">-Skip</span></span>
<span data-ttu-id="efcaf-141">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="efcaf-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="efcaf-142">-First</span><span class="sxs-lookup"><span data-stu-id="efcaf-142">-First</span></span>
<span data-ttu-id="efcaf-143">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="efcaf-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="efcaf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcaf-144">CommonParameters</span></span>
<span data-ttu-id="efcaf-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efcaf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcaf-146">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efcaf-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcaf-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efcaf-147">INPUTS</span></span>

### <span data-ttu-id="efcaf-148">System.String</span><span class="sxs-lookup"><span data-stu-id="efcaf-148">System.String</span></span>

### <span data-ttu-id="efcaf-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="efcaf-149">System.Guid</span></span>

## <span data-ttu-id="efcaf-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="efcaf-150">OUTPUTS</span></span>

### <span data-ttu-id="efcaf-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="efcaf-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="efcaf-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="efcaf-152">NOTES</span></span>

## <span data-ttu-id="efcaf-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efcaf-153">RELATED LINKS</span></span>

[<span data-ttu-id="efcaf-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="efcaf-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="efcaf-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="efcaf-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="efcaf-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="efcaf-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="efcaf-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="efcaf-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)


[<span data-ttu-id="efcaf-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="efcaf-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

