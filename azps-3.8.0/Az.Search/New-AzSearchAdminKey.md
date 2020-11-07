---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ae925d39dab3b56e70cb7c42b320e57eb7f7811a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912616"
---
# <span data-ttu-id="a2eb5-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a2eb5-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="a2eb5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="a2eb5-103">Повторное создание ключа администратора для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="a2eb5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2eb5-104">SYNTAX</span></span>

### <span data-ttu-id="a2eb5-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2eb5-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2eb5-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2eb5-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2eb5-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2eb5-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2eb5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2eb5-108">DESCRIPTION</span></span>
<span data-ttu-id="a2eb5-109">Командлет **New-AzSearchAdminKey** заново создает ключ администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="a2eb5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2eb5-110">EXAMPLES</span></span>

### <span data-ttu-id="a2eb5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2eb5-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="a2eb5-112">В примере повторно создается первичный ключ службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="a2eb5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2eb5-113">PARAMETERS</span></span>

### <span data-ttu-id="a2eb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2eb5-114">-DefaultProfile</span></span>
<span data-ttu-id="a2eb5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eb5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a2eb5-116">-Force</span></span>
<span data-ttu-id="a2eb5-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a2eb5-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="a2eb5-118">-KeyKind</span></span>
<span data-ttu-id="a2eb5-119">Ключ администратора службы поиска (основной/дополнительный).</span><span class="sxs-lookup"><span data-stu-id="a2eb5-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="a2eb5-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a2eb5-120">-ParentObject</span></span>
<span data-ttu-id="a2eb5-121">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a2eb5-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a2eb5-122">-ParentResourceId</span></span>
<span data-ttu-id="a2eb5-123">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a2eb5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2eb5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2eb5-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-125">Resource Group name.</span></span>

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

### <span data-ttu-id="a2eb5-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a2eb5-126">-ServiceName</span></span>
<span data-ttu-id="a2eb5-127">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-127">Search Service name.</span></span>

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

### <span data-ttu-id="a2eb5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2eb5-128">-Confirm</span></span>
<span data-ttu-id="a2eb5-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2eb5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2eb5-130">-WhatIf</span></span>
<span data-ttu-id="a2eb5-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2eb5-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2eb5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2eb5-133">CommonParameters</span></span>
<span data-ttu-id="a2eb5-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2eb5-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2eb5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2eb5-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2eb5-136">INPUTS</span></span>

### <span data-ttu-id="a2eb5-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a2eb5-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a2eb5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a2eb5-138">System.String</span></span>

## <span data-ttu-id="a2eb5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2eb5-139">OUTPUTS</span></span>

### <span data-ttu-id="a2eb5-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a2eb5-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="a2eb5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2eb5-141">NOTES</span></span>

## <span data-ttu-id="a2eb5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2eb5-142">RELATED LINKS</span></span>

[<span data-ttu-id="a2eb5-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="a2eb5-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
