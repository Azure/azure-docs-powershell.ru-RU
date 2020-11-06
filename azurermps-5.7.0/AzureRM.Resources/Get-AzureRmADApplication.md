---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567419"
---
# <span data-ttu-id="bc45e-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bc45e-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="bc45e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc45e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc45e-103">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc45e-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc45e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc45e-104">SYNTAX</span></span>

### <span data-ttu-id="bc45e-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc45e-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc45e-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc45e-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc45e-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc45e-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc45e-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc45e-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc45e-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc45e-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc45e-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc45e-110">DESCRIPTION</span></span>
<span data-ttu-id="bc45e-111">Список существующих приложений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc45e-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="bc45e-112">Поиск приложения можно выполнить с помощью ObjectId, ApplicationId, IdentifierUri или DisplayName.</span><span class="sxs-lookup"><span data-stu-id="bc45e-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="bc45e-113">Если параметр не указан, выводятся все приложения, набираемые в клиенте.</span><span class="sxs-lookup"><span data-stu-id="bc45e-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="bc45e-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc45e-114">EXAMPLES</span></span>

### <span data-ttu-id="bc45e-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc45e-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="bc45e-116">Список всех приложений в клиенте.</span><span class="sxs-lookup"><span data-stu-id="bc45e-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="bc45e-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bc45e-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="bc45e-118">Получает приложение с URI идентификатора как " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="bc45e-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="bc45e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc45e-119">PARAMETERS</span></span>

### <span data-ttu-id="bc45e-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bc45e-120">-ApplicationId</span></span>
<span data-ttu-id="bc45e-121">Идентификатор приложения для извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="bc45e-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc45e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc45e-122">-DefaultProfile</span></span>
<span data-ttu-id="bc45e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bc45e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc45e-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="bc45e-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="bc45e-125">Получение всех приложений, начинающихся с отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="bc45e-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc45e-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="bc45e-126">-IdentifierUri</span></span>
<span data-ttu-id="bc45e-127">Уникальный идентификатор URI извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="bc45e-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc45e-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bc45e-128">-ObjectId</span></span>
<span data-ttu-id="bc45e-129">Идентификатор объекта извлекаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="bc45e-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc45e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc45e-130">CommonParameters</span></span>
<span data-ttu-id="bc45e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc45e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc45e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc45e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc45e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc45e-133">INPUTS</span></span>

### <span data-ttu-id="bc45e-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="bc45e-134">None</span></span>
<span data-ttu-id="bc45e-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bc45e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc45e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc45e-136">OUTPUTS</span></span>

### <span data-ttu-id="bc45e-137">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="bc45e-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="bc45e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc45e-138">NOTES</span></span>

## <span data-ttu-id="bc45e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc45e-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc45e-140">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bc45e-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="bc45e-141">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bc45e-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="bc45e-142">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bc45e-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="bc45e-143">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bc45e-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="bc45e-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bc45e-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="bc45e-145">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bc45e-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

