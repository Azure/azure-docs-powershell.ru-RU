---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: ba169c54d2b4664473a0013be52e2d078827dcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564076"
---
# <span data-ttu-id="413c8-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="413c8-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="413c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="413c8-102">SYNOPSIS</span></span>
<span data-ttu-id="413c8-103">Извлекает список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="413c8-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="413c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="413c8-104">SYNTAX</span></span>

### <span data-ttu-id="413c8-105">ApplicationObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="413c8-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="413c8-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="413c8-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="413c8-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="413c8-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="413c8-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="413c8-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="413c8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="413c8-109">DESCRIPTION</span></span>
<span data-ttu-id="413c8-110">Командлет Get-AzureRmADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="413c8-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="413c8-111">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="413c8-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="413c8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="413c8-112">EXAMPLES</span></span>

### <span data-ttu-id="413c8-113">Пример 1. получение учетных данных приложения с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="413c8-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="413c8-114">Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="413c8-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="413c8-115">Пример 2: получение учетных данных приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="413c8-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="413c8-116">Возвращает приложение с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и преобразует его в командлет Get-AzureRmADAppCredential, чтобы получить список всех учетных данных для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="413c8-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="413c8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="413c8-117">PARAMETERS</span></span>

### <span data-ttu-id="413c8-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="413c8-118">-ApplicationId</span></span>
<span data-ttu-id="413c8-119">Идентификатор приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="413c8-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="413c8-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="413c8-120">-ApplicationObject</span></span>
<span data-ttu-id="413c8-121">Объект приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="413c8-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="413c8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413c8-122">-DefaultProfile</span></span>
<span data-ttu-id="413c8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="413c8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="413c8-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="413c8-124">-DisplayName</span></span>
<span data-ttu-id="413c8-125">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="413c8-125">The display name of the application.</span></span>

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

### <span data-ttu-id="413c8-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="413c8-126">-ObjectId</span></span>
<span data-ttu-id="413c8-127">Идентификатор объекта приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="413c8-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="413c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413c8-128">CommonParameters</span></span>
<span data-ttu-id="413c8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="413c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413c8-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413c8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="413c8-131">INPUTS</span></span>

### <span data-ttu-id="413c8-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="413c8-132">System.Guid</span></span>

### <span data-ttu-id="413c8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="413c8-133">System.String</span></span>

### <span data-ttu-id="413c8-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="413c8-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="413c8-135">Параметры: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="413c8-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="413c8-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="413c8-136">OUTPUTS</span></span>

### <span data-ttu-id="413c8-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="413c8-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="413c8-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="413c8-138">NOTES</span></span>

## <span data-ttu-id="413c8-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="413c8-139">RELATED LINKS</span></span>

[<span data-ttu-id="413c8-140">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="413c8-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="413c8-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="413c8-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="413c8-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="413c8-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

