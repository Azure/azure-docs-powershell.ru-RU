---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: f2a9f5f5689d4e0d7907df481e22c2d8864266ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066633"
---
# <span data-ttu-id="e4f0e-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="e4f0e-101">New-AzDataShare</span></span>

## <span data-ttu-id="e4f0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f0e-103">Создание общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-103">Creates a azure data share.</span></span>

## <span data-ttu-id="e4f0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4f0e-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f0e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f0e-106">Командлет **New-AzDataShare** создает общий ресурс данных в указанной учетной записи для общего доступа к данным Azure, предоставляя имя группы ресурсов, имя учетной записи, общий доступ к имени и доступному типу.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="e4f0e-107">Описание и условия использования — необязательные параметры, которые можно настроить при создании общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="e4f0e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4f0e-108">EXAMPLES</span></span>

### <span data-ttu-id="e4f0e-109">Пример 1: создание общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="e4f0e-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="e4f0e-110">Эта команда создает общий ресурс данных с именем AdsShare из CopyBased в учетной записи для общего доступа к данным, WikiAdsAccount в разделе Реклама в группах ресурсов, с описанием и условиями использования.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="e4f0e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4f0e-111">PARAMETERS</span></span>

### <span data-ttu-id="e4f0e-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e4f0e-112">-AccountName</span></span>
<span data-ttu-id="e4f0e-113">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="e4f0e-113">Azure data share account name</span></span>

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

### <span data-ttu-id="e4f0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f0e-114">-DefaultProfile</span></span>
<span data-ttu-id="e4f0e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4f0e-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="e4f0e-116">-Description</span></span>
<span data-ttu-id="e4f0e-117">Описание общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="e4f0e-117">Description of azure data share</span></span>

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

### <span data-ttu-id="e4f0e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4f0e-118">-Name</span></span>
<span data-ttu-id="e4f0e-119">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="e4f0e-119">Azure data share name</span></span>

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

### <span data-ttu-id="e4f0e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f0e-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4f0e-121">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="e4f0e-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e4f0e-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="e4f0e-122">-TermsOfUse</span></span>
<span data-ttu-id="e4f0e-123">Условия использования для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="e4f0e-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="e4f0e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4f0e-124">-Confirm</span></span>
<span data-ttu-id="e4f0e-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f0e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f0e-126">-WhatIf</span></span>
<span data-ttu-id="e4f0e-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f0e-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f0e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f0e-129">CommonParameters</span></span>
<span data-ttu-id="e4f0e-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4f0e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f0e-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f0e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f0e-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4f0e-132">INPUTS</span></span>

### <span data-ttu-id="e4f0e-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="e4f0e-133">None</span></span>

## <span data-ttu-id="e4f0e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4f0e-134">OUTPUTS</span></span>

### <span data-ttu-id="e4f0e-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="e4f0e-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="e4f0e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4f0e-136">NOTES</span></span>

## <span data-ttu-id="e4f0e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4f0e-137">RELATED LINKS</span></span>
