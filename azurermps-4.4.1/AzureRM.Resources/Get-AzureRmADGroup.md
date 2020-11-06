---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562200"
---
# <span data-ttu-id="95c22-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="95c22-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="95c22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95c22-102">SYNOPSIS</span></span>
<span data-ttu-id="95c22-103">Фильтрует группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95c22-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95c22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95c22-104">SYNTAX</span></span>

### <span data-ttu-id="95c22-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95c22-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95c22-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="95c22-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95c22-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95c22-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95c22-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95c22-108">DESCRIPTION</span></span>
<span data-ttu-id="95c22-109">Фильтрует группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95c22-109">Filters active directory groups.</span></span>

## <span data-ttu-id="95c22-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95c22-110">EXAMPLES</span></span>

### <span data-ttu-id="95c22-111">--------------------------Группы фильтров с использованием идентификатора объекта--------------------------</span><span class="sxs-lookup"><span data-stu-id="95c22-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="95c22-112">Получает группу с ИД 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="95c22-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="95c22-113">--------------------------Группы фильтров с помощью строки поиска--------------------------</span><span class="sxs-lookup"><span data-stu-id="95c22-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="95c22-114">Фильтрует все группы баннеров, в отображаемом имени которых есть Joe.</span><span class="sxs-lookup"><span data-stu-id="95c22-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="95c22-115">--------------------------Групп рекламы--------------------------</span><span class="sxs-lookup"><span data-stu-id="95c22-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="95c22-116">Получает все группы Active Directory</span><span class="sxs-lookup"><span data-stu-id="95c22-116">Gets all AD groups</span></span>

## <span data-ttu-id="95c22-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95c22-117">PARAMETERS</span></span>

### <span data-ttu-id="95c22-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="95c22-118">-ObjectId</span></span>
<span data-ttu-id="95c22-119">Идентификатор объекта группы.</span><span class="sxs-lookup"><span data-stu-id="95c22-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="95c22-120">-SearchString</span><span class="sxs-lookup"><span data-stu-id="95c22-120">-SearchString</span></span>
<span data-ttu-id="95c22-121">Отображаемое имя группы</span><span class="sxs-lookup"><span data-stu-id="95c22-121">The group display name</span></span>

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

### <span data-ttu-id="95c22-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c22-122">-DefaultProfile</span></span>
<span data-ttu-id="95c22-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95c22-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95c22-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c22-124">CommonParameters</span></span>
<span data-ttu-id="95c22-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95c22-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c22-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c22-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c22-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95c22-127">INPUTS</span></span>

## <span data-ttu-id="95c22-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95c22-128">OUTPUTS</span></span>

### <span data-ttu-id="95c22-129">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="95c22-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="95c22-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="95c22-130">NOTES</span></span>

## <span data-ttu-id="95c22-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95c22-131">RELATED LINKS</span></span>

[<span data-ttu-id="95c22-132">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="95c22-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="95c22-133">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="95c22-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="95c22-134">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="95c22-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

