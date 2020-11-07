---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
ms.openlocfilehash: fa7ea6f1e53b94a349d51856432f1c01b2e89ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733131"
---
# <span data-ttu-id="54cfb-101">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="54cfb-101">New-AzureRmSearchAdminKey</span></span>

## <span data-ttu-id="54cfb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="54cfb-103">Повторное создание ключа администратора для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="54cfb-103">Regenerates an admin key of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54cfb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54cfb-104">SYNTAX</span></span>

### <span data-ttu-id="54cfb-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54cfb-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54cfb-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54cfb-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54cfb-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54cfb-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54cfb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54cfb-108">DESCRIPTION</span></span>
<span data-ttu-id="54cfb-109">Командлет **New-AzureRmSearchAdminKey** заново создает ключ администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="54cfb-109">The **New-AzureRmSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="54cfb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54cfb-110">EXAMPLES</span></span>

### <span data-ttu-id="54cfb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54cfb-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="54cfb-112">В примере повторно создается первичный ключ службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="54cfb-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="54cfb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54cfb-113">PARAMETERS</span></span>

### <span data-ttu-id="54cfb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cfb-114">-DefaultProfile</span></span>
<span data-ttu-id="54cfb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54cfb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54cfb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="54cfb-116">-Force</span></span>
<span data-ttu-id="54cfb-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="54cfb-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="54cfb-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="54cfb-118">-KeyKind</span></span>
<span data-ttu-id="54cfb-119">Ключ администратора службы поиска (основной/дополнительный).</span><span class="sxs-lookup"><span data-stu-id="54cfb-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cfb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="54cfb-120">-ParentObject</span></span>
<span data-ttu-id="54cfb-121">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="54cfb-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54cfb-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="54cfb-122">-ParentResourceId</span></span>
<span data-ttu-id="54cfb-123">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="54cfb-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54cfb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54cfb-124">-ResourceGroupName</span></span>
<span data-ttu-id="54cfb-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54cfb-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cfb-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="54cfb-126">-ServiceName</span></span>
<span data-ttu-id="54cfb-127">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="54cfb-127">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cfb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54cfb-128">-Confirm</span></span>
<span data-ttu-id="54cfb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54cfb-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cfb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54cfb-130">-WhatIf</span></span>
<span data-ttu-id="54cfb-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54cfb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54cfb-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54cfb-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cfb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cfb-133">CommonParameters</span></span>
<span data-ttu-id="54cfb-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54cfb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cfb-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54cfb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cfb-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54cfb-136">INPUTS</span></span>

### <span data-ttu-id="54cfb-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="54cfb-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="54cfb-138">Параметры: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="54cfb-138">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="54cfb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="54cfb-139">System.String</span></span>

## <span data-ttu-id="54cfb-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54cfb-140">OUTPUTS</span></span>

### <span data-ttu-id="54cfb-141">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="54cfb-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="54cfb-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="54cfb-142">NOTES</span></span>

## <span data-ttu-id="54cfb-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54cfb-143">RELATED LINKS</span></span>

[<span data-ttu-id="54cfb-144">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="54cfb-144">Get-AzureRmSearchAdminKeyPair</span></span>](./Get-AzureRmSearchAdminKeyPair.md)
