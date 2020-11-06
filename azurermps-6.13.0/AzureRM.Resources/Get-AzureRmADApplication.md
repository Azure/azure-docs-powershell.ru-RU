---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564072"
---
# <span data-ttu-id="f373e-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f373e-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="f373e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f373e-102">SYNOPSIS</span></span>
<span data-ttu-id="f373e-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f373e-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f373e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f373e-104">SYNTAX</span></span>

### <span data-ttu-id="f373e-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f373e-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f373e-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f373e-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f373e-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f373e-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f373e-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f373e-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f373e-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f373e-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f373e-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="f373e-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f373e-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f373e-111">DESCRIPTION</span></span>
<span data-ttu-id="f373e-112">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f373e-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="f373e-113">Поиск приложения можно выполнить с помощью ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="f373e-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="f373e-114">Если параметр не указан, выводятся все приложения, набираемые в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f373e-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="f373e-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f373e-115">EXAMPLES</span></span>

### <span data-ttu-id="f373e-116">Пример 1: список всех приложений</span><span class="sxs-lookup"><span data-stu-id="f373e-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="f373e-117">Список всех приложений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f373e-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="f373e-118">Пример 2. Перечисление приложений с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="f373e-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="f373e-119">Список первых приложений 100 в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f373e-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="f373e-120">Пример 3: получение идентификатора URI для приложения</span><span class="sxs-lookup"><span data-stu-id="f373e-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="f373e-121">Получает приложение с URI идентификатора как " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="f373e-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="f373e-122">Пример 4: получение приложения по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="f373e-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="f373e-123">Возвращает приложение с идентификатором объекта "39e64ec6-569b-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="f373e-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="f373e-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f373e-124">PARAMETERS</span></span>

### <span data-ttu-id="f373e-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f373e-125">-ApplicationId</span></span>
<span data-ttu-id="f373e-126">Идентификатор приложения для извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f373e-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="f373e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f373e-127">-DefaultProfile</span></span>
<span data-ttu-id="f373e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f373e-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f373e-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f373e-129">-DisplayName</span></span>
<span data-ttu-id="f373e-130">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="f373e-130">The display name of the application.</span></span>

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

### <span data-ttu-id="f373e-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="f373e-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="f373e-132">Получение всех приложений, начинающихся с отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="f373e-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="f373e-133">-First</span><span class="sxs-lookup"><span data-stu-id="f373e-133">-First</span></span>
<span data-ttu-id="f373e-134">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="f373e-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="f373e-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="f373e-135">-IdentifierUri</span></span>
<span data-ttu-id="f373e-136">Уникальный идентификатор URI извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f373e-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="f373e-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f373e-137">-IncludeTotalCount</span></span>
<span data-ttu-id="f373e-138">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="f373e-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f373e-139">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="f373e-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="f373e-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f373e-140">-ObjectId</span></span>
<span data-ttu-id="f373e-141">Идентификатор объекта извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f373e-141">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="f373e-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="f373e-142">-Skip</span></span>
<span data-ttu-id="f373e-143">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="f373e-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f373e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f373e-144">CommonParameters</span></span>
<span data-ttu-id="f373e-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f373e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f373e-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f373e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f373e-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f373e-147">INPUTS</span></span>

### <span data-ttu-id="f373e-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f373e-148">System.Guid</span></span>

### <span data-ttu-id="f373e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f373e-149">System.String</span></span>

## <span data-ttu-id="f373e-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f373e-150">OUTPUTS</span></span>

### <span data-ttu-id="f373e-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f373e-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="f373e-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="f373e-152">NOTES</span></span>

## <span data-ttu-id="f373e-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f373e-153">RELATED LINKS</span></span>

[<span data-ttu-id="f373e-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f373e-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="f373e-155">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f373e-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="f373e-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f373e-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="f373e-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f373e-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="f373e-158">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f373e-158">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="f373e-159">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f373e-159">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

