---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 5f019f413e7ae0efa2013412499fcf34bd94a248
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910972"
---
# <span data-ttu-id="71d43-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="71d43-101">Get-AzADApplication</span></span>

## <span data-ttu-id="71d43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71d43-102">SYNOPSIS</span></span>
<span data-ttu-id="71d43-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71d43-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="71d43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71d43-104">SYNTAX</span></span>

### <span data-ttu-id="71d43-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71d43-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71d43-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d43-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71d43-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d43-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71d43-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d43-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71d43-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d43-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="71d43-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d43-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="71d43-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d43-111">DESCRIPTION</span></span>
<span data-ttu-id="71d43-112">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71d43-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="71d43-113">Поиск приложения можно выполнить с помощью ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="71d43-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="71d43-114">Если параметр не указан, выводятся все приложения, набираемые в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71d43-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="71d43-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71d43-115">EXAMPLES</span></span>

### <span data-ttu-id="71d43-116">Пример 1: список всех приложений</span><span class="sxs-lookup"><span data-stu-id="71d43-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="71d43-117">Список всех приложений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71d43-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="71d43-118">Пример 2. Перечисление приложений с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="71d43-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="71d43-119">Список первых приложений 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71d43-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="71d43-120">Пример 3: получение идентификатора URI для приложения</span><span class="sxs-lookup"><span data-stu-id="71d43-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="71d43-121">Получает приложение с URI идентификатора как " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="71d43-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="71d43-122">Пример 4: получение приложения по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="71d43-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="71d43-123">Возвращает приложение с идентификатором объекта "39e64ec6-569b-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="71d43-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="71d43-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71d43-124">PARAMETERS</span></span>

### <span data-ttu-id="71d43-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="71d43-125">-ApplicationId</span></span>
<span data-ttu-id="71d43-126">Идентификатор приложения для извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="71d43-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="71d43-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d43-127">-DefaultProfile</span></span>
<span data-ttu-id="71d43-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71d43-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71d43-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="71d43-129">-DisplayName</span></span>
<span data-ttu-id="71d43-130">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="71d43-130">The display name of the application.</span></span>

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

### <span data-ttu-id="71d43-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="71d43-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="71d43-132">Получение всех приложений, начинающихся с отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="71d43-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="71d43-133">-First</span><span class="sxs-lookup"><span data-stu-id="71d43-133">-First</span></span>
<span data-ttu-id="71d43-134">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="71d43-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="71d43-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="71d43-135">-IdentifierUri</span></span>
<span data-ttu-id="71d43-136">Уникальный идентификатор URI извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="71d43-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="71d43-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="71d43-137">-IncludeTotalCount</span></span>
<span data-ttu-id="71d43-138">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="71d43-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="71d43-139">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="71d43-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="71d43-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="71d43-140">-ObjectId</span></span>
<span data-ttu-id="71d43-141">Идентификатор объекта извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="71d43-141">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="71d43-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="71d43-142">-Skip</span></span>
<span data-ttu-id="71d43-143">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="71d43-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="71d43-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d43-144">CommonParameters</span></span>
<span data-ttu-id="71d43-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71d43-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d43-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d43-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d43-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71d43-147">INPUTS</span></span>

### <span data-ttu-id="71d43-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="71d43-148">System.Guid</span></span>

### <span data-ttu-id="71d43-149">System. String</span><span class="sxs-lookup"><span data-stu-id="71d43-149">System.String</span></span>

## <span data-ttu-id="71d43-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d43-150">OUTPUTS</span></span>

### <span data-ttu-id="71d43-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="71d43-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="71d43-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="71d43-152">NOTES</span></span>

## <span data-ttu-id="71d43-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71d43-153">RELATED LINKS</span></span>

[<span data-ttu-id="71d43-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="71d43-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="71d43-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="71d43-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="71d43-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="71d43-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="71d43-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="71d43-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="71d43-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="71d43-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="71d43-159">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="71d43-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

