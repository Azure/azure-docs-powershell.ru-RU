---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: a4d1831114db40295e30b30e0fb12621caff2c89
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398858"
---
# <span data-ttu-id="b096d-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b096d-101">Get-AzADApplication</span></span>

## <span data-ttu-id="b096d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b096d-102">SYNOPSIS</span></span>
<span data-ttu-id="b096d-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b096d-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="b096d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b096d-104">SYNTAX</span></span>

### <span data-ttu-id="b096d-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b096d-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b096d-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b096d-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b096d-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b096d-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b096d-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b096d-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b096d-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b096d-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b096d-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="b096d-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b096d-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b096d-111">DESCRIPTION</span></span>
<span data-ttu-id="b096d-112">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b096d-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="b096d-113">Для подметки приложений можно использовать ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="b096d-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="b096d-114">Если параметр не задан, извлекает все приложения в клиенте.</span><span class="sxs-lookup"><span data-stu-id="b096d-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="b096d-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b096d-115">EXAMPLES</span></span>

### <span data-ttu-id="b096d-116">Пример 1. Список всех приложений</span><span class="sxs-lookup"><span data-stu-id="b096d-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="b096d-117">Список всех приложений, которые находятся в клиенте.</span><span class="sxs-lookup"><span data-stu-id="b096d-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="b096d-118">Пример 2. Список приложений с использованием разведки</span><span class="sxs-lookup"><span data-stu-id="b096d-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="b096d-119">Список первых 100 приложений для клиента.</span><span class="sxs-lookup"><span data-stu-id="b096d-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="b096d-120">Пример 3. Получение приложения по идентификатору URI</span><span class="sxs-lookup"><span data-stu-id="b096d-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="b096d-121">Возвращает приложение с идентификатором uri в качестве " http://mySecretApp1 " .</span><span class="sxs-lookup"><span data-stu-id="b096d-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="b096d-122">Пример 4. Получение приложения по ид объекта</span><span class="sxs-lookup"><span data-stu-id="b096d-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="b096d-123">Получает приложение с ид объекта '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span><span class="sxs-lookup"><span data-stu-id="b096d-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="b096d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b096d-124">PARAMETERS</span></span>

### <span data-ttu-id="b096d-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b096d-125">-ApplicationId</span></span>
<span data-ttu-id="b096d-126">ИД приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="b096d-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="b096d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b096d-127">-DefaultProfile</span></span>
<span data-ttu-id="b096d-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b096d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b096d-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b096d-129">-DisplayName</span></span>
<span data-ttu-id="b096d-130">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="b096d-130">The display name of the application.</span></span>

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

### <span data-ttu-id="b096d-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="b096d-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="b096d-132">Получить все приложения, начиная с отображаемом имени.</span><span class="sxs-lookup"><span data-stu-id="b096d-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="b096d-133">-First</span><span class="sxs-lookup"><span data-stu-id="b096d-133">-First</span></span>
<span data-ttu-id="b096d-134">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="b096d-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b096d-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="b096d-135">-IdentifierUri</span></span>
<span data-ttu-id="b096d-136">Уникальный идентификатор Uri приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="b096d-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="b096d-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b096d-137">-IncludeTotalCount</span></span>
<span data-ttu-id="b096d-138">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="b096d-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b096d-139">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="b096d-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b096d-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b096d-140">-ObjectId</span></span>
<span data-ttu-id="b096d-141">ИД объекта приложения, извлекаемого из приложения.</span><span class="sxs-lookup"><span data-stu-id="b096d-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b096d-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="b096d-142">-Skip</span></span>
<span data-ttu-id="b096d-143">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="b096d-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b096d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b096d-144">CommonParameters</span></span>
<span data-ttu-id="b096d-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b096d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b096d-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b096d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b096d-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b096d-147">INPUTS</span></span>

### <span data-ttu-id="b096d-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b096d-148">System.Guid</span></span>

### <span data-ttu-id="b096d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b096d-149">System.String</span></span>

## <span data-ttu-id="b096d-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b096d-150">OUTPUTS</span></span>

### <span data-ttu-id="b096d-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b096d-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="b096d-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b096d-152">NOTES</span></span>

## <span data-ttu-id="b096d-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b096d-153">RELATED LINKS</span></span>

[<span data-ttu-id="b096d-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b096d-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="b096d-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b096d-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="b096d-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b096d-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="b096d-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b096d-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)


[<span data-ttu-id="b096d-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b096d-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

