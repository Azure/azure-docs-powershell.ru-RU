---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: afcb95eca70c005023bacc2b2d71d9fda54c9259
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066501"
---
# <span data-ttu-id="46448-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="46448-101">Get-AzADApplication</span></span>

## <span data-ttu-id="46448-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46448-102">SYNOPSIS</span></span>
<span data-ttu-id="46448-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46448-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="46448-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46448-104">SYNTAX</span></span>

### <span data-ttu-id="46448-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46448-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="46448-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46448-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="46448-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46448-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="46448-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="46448-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="46448-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="46448-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="46448-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="46448-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="46448-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46448-111">DESCRIPTION</span></span>
<span data-ttu-id="46448-112">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46448-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="46448-113">Поиск приложения можно выполнить с помощью ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="46448-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="46448-114">Если параметр не указан, выводятся все приложения, набираемые в клиенте.</span><span class="sxs-lookup"><span data-stu-id="46448-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="46448-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46448-115">EXAMPLES</span></span>

### <span data-ttu-id="46448-116">Пример 1: список всех приложений</span><span class="sxs-lookup"><span data-stu-id="46448-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="46448-117">Список всех приложений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="46448-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="46448-118">Пример 2. Перечисление приложений с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="46448-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="46448-119">Список первых приложений 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="46448-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="46448-120">Пример 3: получение идентификатора URI для приложения</span><span class="sxs-lookup"><span data-stu-id="46448-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="46448-121">Получает приложение с URI идентификатора как " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="46448-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="46448-122">Пример 4: получение приложения по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="46448-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="46448-123">Возвращает приложение с идентификатором объекта "39e64ec6-569b-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="46448-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="46448-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46448-124">PARAMETERS</span></span>

### <span data-ttu-id="46448-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="46448-125">-ApplicationId</span></span>
<span data-ttu-id="46448-126">Идентификатор приложения для извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="46448-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="46448-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46448-127">-DefaultProfile</span></span>
<span data-ttu-id="46448-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="46448-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46448-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="46448-129">-DisplayName</span></span>
<span data-ttu-id="46448-130">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="46448-130">The display name of the application.</span></span>

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

### <span data-ttu-id="46448-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="46448-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="46448-132">Получение всех приложений, начинающихся с отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="46448-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="46448-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="46448-133">-IdentifierUri</span></span>
<span data-ttu-id="46448-134">Уникальный идентификатор URI извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="46448-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="46448-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="46448-135">-ObjectId</span></span>
<span data-ttu-id="46448-136">Идентификатор объекта извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="46448-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="46448-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="46448-137">-IncludeTotalCount</span></span>
<span data-ttu-id="46448-138">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="46448-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="46448-139">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="46448-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="46448-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="46448-140">-Skip</span></span>
<span data-ttu-id="46448-141">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="46448-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="46448-142">-First</span><span class="sxs-lookup"><span data-stu-id="46448-142">-First</span></span>
<span data-ttu-id="46448-143">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="46448-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="46448-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46448-144">CommonParameters</span></span>
<span data-ttu-id="46448-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46448-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46448-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46448-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46448-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46448-147">INPUTS</span></span>

### <span data-ttu-id="46448-148">System. String</span><span class="sxs-lookup"><span data-stu-id="46448-148">System.String</span></span>

### <span data-ttu-id="46448-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="46448-149">System.Guid</span></span>

## <span data-ttu-id="46448-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46448-150">OUTPUTS</span></span>

### <span data-ttu-id="46448-151">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="46448-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="46448-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="46448-152">NOTES</span></span>

## <span data-ttu-id="46448-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46448-153">RELATED LINKS</span></span>

[<span data-ttu-id="46448-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="46448-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="46448-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="46448-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="46448-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="46448-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="46448-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="46448-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="46448-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="46448-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="46448-159">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="46448-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

