---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568685"
---
# <span data-ttu-id="bc837-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc837-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="bc837-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc837-102">SYNOPSIS</span></span>
<span data-ttu-id="bc837-103">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc837-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc837-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc837-104">SYNTAX</span></span>

### <span data-ttu-id="bc837-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc837-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc837-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc837-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc837-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc837-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc837-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc837-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc837-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc837-109">DESCRIPTION</span></span>
<span data-ttu-id="bc837-110">Фильтрует субъектов-служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc837-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="bc837-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc837-111">EXAMPLES</span></span>

### <span data-ttu-id="bc837-112">--------------------------Отфильтровать субъекты-службы с помощью SPN--------------------------</span><span class="sxs-lookup"><span data-stu-id="bc837-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="bc837-113">Получает субъектов-служб с 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span><span class="sxs-lookup"><span data-stu-id="bc837-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="bc837-114">--------------------------Отфильтровать субъекты-службы с помощью строки поиска--------------------------</span><span class="sxs-lookup"><span data-stu-id="bc837-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="bc837-115">Фильтрует всех участников AD-служб с отображаемым именем, начинающимся с "веб".</span><span class="sxs-lookup"><span data-stu-id="bc837-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="bc837-116">Субъекты-службы--------------------------списка--------------------------</span><span class="sxs-lookup"><span data-stu-id="bc837-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="bc837-117">Получает всех участников службы AD.</span><span class="sxs-lookup"><span data-stu-id="bc837-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="bc837-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc837-118">PARAMETERS</span></span>

### <span data-ttu-id="bc837-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bc837-119">-ObjectId</span></span>
<span data-ttu-id="bc837-120">Идентификатор объекта субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bc837-120">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-121">-SearchString</span><span class="sxs-lookup"><span data-stu-id="bc837-121">-SearchString</span></span>
<span data-ttu-id="bc837-122">Выбор всех субъектов-служб с отображаемым именем, начинающимся с этого значения.</span><span class="sxs-lookup"><span data-stu-id="bc837-122">Fetches all service principals that have the display name starting with this value.</span></span>

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

### <span data-ttu-id="bc837-123">-Намерено</span><span class="sxs-lookup"><span data-stu-id="bc837-123">-ServicePrincipalName</span></span>
<span data-ttu-id="bc837-124">SPN службы.</span><span class="sxs-lookup"><span data-stu-id="bc837-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc837-125">-DefaultProfile</span></span>
<span data-ttu-id="bc837-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc837-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc837-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc837-127">CommonParameters</span></span>
<span data-ttu-id="bc837-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc837-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc837-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc837-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc837-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc837-130">INPUTS</span></span>

## <span data-ttu-id="bc837-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc837-131">OUTPUTS</span></span>

### <span data-ttu-id="bc837-132">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="bc837-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="bc837-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc837-133">NOTES</span></span>

## <span data-ttu-id="bc837-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc837-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc837-135">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc837-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="bc837-136">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc837-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="bc837-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc837-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="bc837-138">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bc837-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="bc837-139">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="bc837-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

