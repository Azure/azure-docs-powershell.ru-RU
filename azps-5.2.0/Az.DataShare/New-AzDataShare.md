---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324397"
---
# <span data-ttu-id="2861d-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="2861d-101">New-AzDataShare</span></span>

## <span data-ttu-id="2861d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2861d-102">SYNOPSIS</span></span>
<span data-ttu-id="2861d-103">Создает обойму данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2861d-103">Creates a azure data share.</span></span>

## <span data-ttu-id="2861d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2861d-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2861d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2861d-105">DESCRIPTION</span></span>
<span data-ttu-id="2861d-106">С **помощью cmdlet New-AzDataShare** в указанной учетной записи azure data share создается поделиться данными, задав имя группы ресурсов, имя учетной записи, имя и данные о предоставлении доступа.</span><span class="sxs-lookup"><span data-stu-id="2861d-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="2861d-107">Описание и условия использования — это необязательные параметры, которые можно настроить при создании обмена данными.</span><span class="sxs-lookup"><span data-stu-id="2861d-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="2861d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2861d-108">EXAMPLES</span></span>

### <span data-ttu-id="2861d-109">Пример 1. Создание обмена данными</span><span class="sxs-lookup"><span data-stu-id="2861d-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="2861d-110">Эта команда создает обилие данных AdsShare типа CopyBased в учетной записи викиAdsAccount группы ресурсов ADS с описанием и условиями использования.</span><span class="sxs-lookup"><span data-stu-id="2861d-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="2861d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2861d-111">PARAMETERS</span></span>

### <span data-ttu-id="2861d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2861d-112">-AccountName</span></span>
<span data-ttu-id="2861d-113">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2861d-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2861d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2861d-114">-DefaultProfile</span></span>
<span data-ttu-id="2861d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2861d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2861d-116">-Description</span><span class="sxs-lookup"><span data-stu-id="2861d-116">-Description</span></span>
<span data-ttu-id="2861d-117">Описание azure data share</span><span class="sxs-lookup"><span data-stu-id="2861d-117">Description of azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2861d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2861d-118">-Name</span></span>
<span data-ttu-id="2861d-119">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2861d-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2861d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2861d-120">-ResourceGroupName</span></span>
<span data-ttu-id="2861d-121">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="2861d-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2861d-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="2861d-122">-TermsOfUse</span></span>
<span data-ttu-id="2861d-123">Условия использования для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2861d-123">Terms of use for azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2861d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2861d-124">-Confirm</span></span>
<span data-ttu-id="2861d-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2861d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2861d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2861d-126">-WhatIf</span></span>
<span data-ttu-id="2861d-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2861d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2861d-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2861d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2861d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2861d-129">CommonParameters</span></span>
<span data-ttu-id="2861d-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2861d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2861d-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2861d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2861d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2861d-132">INPUTS</span></span>

### <span data-ttu-id="2861d-133">Нет</span><span class="sxs-lookup"><span data-stu-id="2861d-133">None</span></span>

## <span data-ttu-id="2861d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2861d-134">OUTPUTS</span></span>

### <span data-ttu-id="2861d-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2861d-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2861d-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2861d-136">NOTES</span></span>

## <span data-ttu-id="2861d-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2861d-137">RELATED LINKS</span></span>
