---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561552"
---
# <span data-ttu-id="33737-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33737-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="33737-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33737-102">SYNOPSIS</span></span>
<span data-ttu-id="33737-103">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33737-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33737-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33737-104">SYNTAX</span></span>

### <span data-ttu-id="33737-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33737-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33737-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="33737-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33737-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33737-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33737-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="33737-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33737-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33737-109">DESCRIPTION</span></span>
<span data-ttu-id="33737-110">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33737-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="33737-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33737-111">EXAMPLES</span></span>

### <span data-ttu-id="33737-112">Фильтрация субъектов-служб с помощью SPN</span><span class="sxs-lookup"><span data-stu-id="33737-112">Filters service principals using SPN</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="33737-113">Получает субъектов-служб с 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span><span class="sxs-lookup"><span data-stu-id="33737-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="33737-114">Фильтрация субъектов-служб с помощью строки поиска</span><span class="sxs-lookup"><span data-stu-id="33737-114">Filters service principals using Search String</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="33737-115">Фильтрует всех участников AD-служб с отображаемым именем, начинающимся с "веб".</span><span class="sxs-lookup"><span data-stu-id="33737-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="33737-116">Участники служб рекламы в списке</span><span class="sxs-lookup"><span data-stu-id="33737-116">List AD service principals</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="33737-117">Получает всех участников службы AD.</span><span class="sxs-lookup"><span data-stu-id="33737-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="33737-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33737-118">PARAMETERS</span></span>

### <span data-ttu-id="33737-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33737-119">-DefaultProfile</span></span>
<span data-ttu-id="33737-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="33737-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33737-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="33737-121">-ObjectId</span></span>
<span data-ttu-id="33737-122">Идентификатор объекта субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="33737-122">Object id of the service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33737-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="33737-123">-SearchString</span></span>
<span data-ttu-id="33737-124">Выбор всех субъектов-служб с отображаемым именем, начинающимся с этого значения.</span><span class="sxs-lookup"><span data-stu-id="33737-124">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33737-125">-Намерено</span><span class="sxs-lookup"><span data-stu-id="33737-125">-ServicePrincipalName</span></span>
<span data-ttu-id="33737-126">SPN службы.</span><span class="sxs-lookup"><span data-stu-id="33737-126">SPN of the service.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33737-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33737-127">CommonParameters</span></span>
<span data-ttu-id="33737-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33737-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33737-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33737-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33737-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33737-130">INPUTS</span></span>

### <span data-ttu-id="33737-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="33737-131">None</span></span>
<span data-ttu-id="33737-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="33737-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33737-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33737-133">OUTPUTS</span></span>

### <span data-ttu-id="33737-134">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="33737-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="33737-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="33737-135">NOTES</span></span>

## <span data-ttu-id="33737-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33737-136">RELATED LINKS</span></span>

[<span data-ttu-id="33737-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33737-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33737-138">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33737-138">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33737-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33737-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33737-140">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="33737-140">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="33737-141">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="33737-141">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

