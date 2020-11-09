---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312890"
---
# <span data-ttu-id="d1542-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="d1542-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="d1542-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1542-102">SYNOPSIS</span></span>
<span data-ttu-id="d1542-103">Удаление подписки на общий доступ</span><span class="sxs-lookup"><span data-stu-id="d1542-103">removes a share subscription</span></span>

## <span data-ttu-id="d1542-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1542-104">SYNTAX</span></span>

### <span data-ttu-id="d1542-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1542-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1542-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1542-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1542-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1542-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1542-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1542-108">DESCRIPTION</span></span>
<span data-ttu-id="d1542-109">Командлет **Remove-AzDataShareSubscription** удаляет подписку на общий доступ</span><span class="sxs-lookup"><span data-stu-id="d1542-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="d1542-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1542-110">EXAMPLES</span></span>

### <span data-ttu-id="d1542-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1542-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d1542-112">Эти команды удаляют sharesubscription с именем AdsShareSubscription из учетной записи WikiAds.</span><span class="sxs-lookup"><span data-stu-id="d1542-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="d1542-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1542-113">PARAMETERS</span></span>

### <span data-ttu-id="d1542-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="d1542-114">-AccountName</span></span>
<span data-ttu-id="d1542-115">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="d1542-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1542-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1542-116">-AsJob</span></span>
<span data-ttu-id="d1542-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="d1542-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="d1542-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1542-118">-DefaultProfile</span></span>
<span data-ttu-id="d1542-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1542-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1542-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1542-120">-InputObject</span></span>
<span data-ttu-id="d1542-121">Объект подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="d1542-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1542-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1542-122">-Name</span></span>
<span data-ttu-id="d1542-123">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="d1542-123">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1542-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1542-124">-PassThru</span></span>
<span data-ttu-id="d1542-125">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="d1542-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="d1542-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1542-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1542-127">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="d1542-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1542-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1542-128">-ResourceId</span></span>
<span data-ttu-id="d1542-129">Идентификатор ресурса для подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="d1542-129">The resource id of the azure data share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1542-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1542-130">-Confirm</span></span>
<span data-ttu-id="d1542-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1542-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1542-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1542-132">-WhatIf</span></span>
<span data-ttu-id="d1542-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1542-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1542-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1542-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1542-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1542-135">CommonParameters</span></span>
<span data-ttu-id="d1542-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1542-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1542-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1542-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1542-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1542-138">INPUTS</span></span>

### <span data-ttu-id="d1542-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1542-139">System.String</span></span>

### <span data-ttu-id="d1542-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="d1542-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="d1542-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1542-141">OUTPUTS</span></span>

### <span data-ttu-id="d1542-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1542-142">System.Boolean</span></span>

## <span data-ttu-id="d1542-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1542-143">NOTES</span></span>

## <span data-ttu-id="d1542-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1542-144">RELATED LINKS</span></span>
