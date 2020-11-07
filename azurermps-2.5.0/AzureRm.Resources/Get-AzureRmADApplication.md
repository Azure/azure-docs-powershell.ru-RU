---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 4e7abd4a3b33f54e5a0ec0bdde01e3fe11da31c4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913753"
---
# <span data-ttu-id="94e7c-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="94e7c-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="94e7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="94e7c-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94e7c-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94e7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94e7c-104">SYNTAX</span></span>

### <span data-ttu-id="94e7c-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94e7c-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="94e7c-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e7c-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="94e7c-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e7c-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="94e7c-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e7c-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="94e7c-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e7c-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="94e7c-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e7c-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="94e7c-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e7c-111">DESCRIPTION</span></span>
<span data-ttu-id="94e7c-112">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94e7c-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="94e7c-113">Поиск приложения можно выполнить с помощью ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="94e7c-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="94e7c-114">Если параметр не указан, выводятся все приложения, набираемые в клиенте.</span><span class="sxs-lookup"><span data-stu-id="94e7c-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="94e7c-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94e7c-115">EXAMPLES</span></span>

### <span data-ttu-id="94e7c-116">Пример 1: список всех приложений</span><span class="sxs-lookup"><span data-stu-id="94e7c-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="94e7c-117">Список всех приложений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="94e7c-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="94e7c-118">Пример 2. Перечисление приложений с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="94e7c-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="94e7c-119">Список первых приложений 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="94e7c-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="94e7c-120">Пример 3: получение идентификатора URI для приложения</span><span class="sxs-lookup"><span data-stu-id="94e7c-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="94e7c-121">Получает приложение с URI идентификатора как " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="94e7c-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="94e7c-122">Пример 4: получение приложения по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="94e7c-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="94e7c-123">Возвращает приложение с идентификатором объекта "39e64ec6-569b-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="94e7c-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="94e7c-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94e7c-124">PARAMETERS</span></span>

### <span data-ttu-id="94e7c-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="94e7c-125">-ApplicationId</span></span>
<span data-ttu-id="94e7c-126">Идентификатор приложения для извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="94e7c-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="94e7c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e7c-127">-DefaultProfile</span></span>
<span data-ttu-id="94e7c-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94e7c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94e7c-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="94e7c-129">-DisplayName</span></span>
<span data-ttu-id="94e7c-130">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="94e7c-130">The display name of the application.</span></span>

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

### <span data-ttu-id="94e7c-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="94e7c-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="94e7c-132">Получение всех приложений, начинающихся с отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="94e7c-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="94e7c-133">-First</span><span class="sxs-lookup"><span data-stu-id="94e7c-133">-First</span></span>
<span data-ttu-id="94e7c-134">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="94e7c-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="94e7c-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="94e7c-135">-IdentifierUri</span></span>
<span data-ttu-id="94e7c-136">Уникальный идентификатор URI извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="94e7c-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="94e7c-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="94e7c-137">-IncludeTotalCount</span></span>
<span data-ttu-id="94e7c-138">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="94e7c-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="94e7c-139">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="94e7c-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="94e7c-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="94e7c-140">-ObjectId</span></span>
<span data-ttu-id="94e7c-141">Идентификатор объекта извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="94e7c-141">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="94e7c-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="94e7c-142">-Skip</span></span>
<span data-ttu-id="94e7c-143">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="94e7c-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="94e7c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e7c-144">CommonParameters</span></span>
<span data-ttu-id="94e7c-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94e7c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e7c-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e7c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e7c-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94e7c-147">INPUTS</span></span>

### <span data-ttu-id="94e7c-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="94e7c-148">System.Guid</span></span>

### <span data-ttu-id="94e7c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="94e7c-149">System.String</span></span>

## <span data-ttu-id="94e7c-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e7c-150">OUTPUTS</span></span>

### <span data-ttu-id="94e7c-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="94e7c-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="94e7c-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="94e7c-152">NOTES</span></span>

## <span data-ttu-id="94e7c-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94e7c-153">RELATED LINKS</span></span>

[<span data-ttu-id="94e7c-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="94e7c-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="94e7c-155">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="94e7c-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="94e7c-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="94e7c-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="94e7c-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="94e7c-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)



[<span data-ttu-id="94e7c-158">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="94e7c-158">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

