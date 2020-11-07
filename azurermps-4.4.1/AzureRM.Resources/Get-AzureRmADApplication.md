---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732695"
---
# <span data-ttu-id="bf448-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf448-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="bf448-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf448-102">SYNOPSIS</span></span>
<span data-ttu-id="bf448-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bf448-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf448-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf448-104">SYNTAX</span></span>

### <span data-ttu-id="bf448-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf448-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf448-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf448-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf448-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf448-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf448-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf448-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf448-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf448-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf448-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf448-110">DESCRIPTION</span></span>
<span data-ttu-id="bf448-111">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bf448-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="bf448-112">Поиск приложения можно выполнить с помощью ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="bf448-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="bf448-113">Если параметр не указан, выводятся все приложения, набираемые в клиенте.</span><span class="sxs-lookup"><span data-stu-id="bf448-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="bf448-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf448-114">EXAMPLES</span></span>

### <span data-ttu-id="bf448-115">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf448-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="bf448-116">Список всех приложений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="bf448-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="bf448-117">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf448-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="bf448-118">Получает приложение с URI идентификатора как " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="bf448-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="bf448-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf448-119">PARAMETERS</span></span>

### <span data-ttu-id="bf448-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf448-120">-ApplicationId</span></span>
<span data-ttu-id="bf448-121">Идентификатор приложения для извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="bf448-121">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="bf448-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="bf448-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="bf448-123">Получение всех приложений, начинающихся с отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="bf448-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf448-124">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="bf448-124">-IdentifierUri</span></span>
<span data-ttu-id="bf448-125">Уникальный идентификатор URI извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="bf448-125">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="bf448-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bf448-126">-ObjectId</span></span>
<span data-ttu-id="bf448-127">Идентификатор объекта извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="bf448-127">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="bf448-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf448-128">-DefaultProfile</span></span>
<span data-ttu-id="bf448-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf448-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf448-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf448-130">CommonParameters</span></span>
<span data-ttu-id="bf448-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf448-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf448-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf448-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf448-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf448-133">INPUTS</span></span>

## <span data-ttu-id="bf448-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf448-134">OUTPUTS</span></span>

### <span data-ttu-id="bf448-135">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="bf448-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="bf448-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf448-136">NOTES</span></span>

## <span data-ttu-id="bf448-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf448-137">RELATED LINKS</span></span>

[<span data-ttu-id="bf448-138">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bf448-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="bf448-139">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bf448-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="bf448-140">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bf448-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="bf448-141">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf448-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="bf448-142">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf448-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="bf448-143">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf448-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

