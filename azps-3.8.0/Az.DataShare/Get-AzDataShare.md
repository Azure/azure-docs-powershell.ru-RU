---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a01d67a5ebf98e07a9410903e4c00b4ed4ee70a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065434"
---
# <span data-ttu-id="d6808-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="d6808-101">Get-AzDataShare</span></span>

## <span data-ttu-id="d6808-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6808-102">SYNOPSIS</span></span>
<span data-ttu-id="d6808-103">Получение сведений об общих ресурсах данных.</span><span class="sxs-lookup"><span data-stu-id="d6808-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="d6808-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6808-104">SYNTAX</span></span>

### <span data-ttu-id="d6808-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6808-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6808-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6808-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6808-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6808-107">DESCRIPTION</span></span>
<span data-ttu-id="d6808-108">Командлет **Get-AzDataShare** получает сведения о ресурсах общих данных в службе общих данных Azure accoount.</span><span class="sxs-lookup"><span data-stu-id="d6808-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="d6808-109">Если вы задаете имя общего доступа к данным, этот командлет получает сведения об этом общем доступе к данным.</span><span class="sxs-lookup"><span data-stu-id="d6808-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="d6808-110">Если имя не задано, этот командлет получает сведения обо всех общих ресурсах в учетной записи для общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="d6808-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="d6808-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6808-111">EXAMPLES</span></span>

### <span data-ttu-id="d6808-112">Пример 1: получение определенного общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="d6808-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
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

<span data-ttu-id="d6808-113">Эта команда отображает сведения о AdsShare общего доступа к данным в WikiAdsAccount учетной записи для общего доступа к данным Azure и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6808-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="d6808-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6808-114">PARAMETERS</span></span>

### <span data-ttu-id="d6808-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="d6808-115">-AccountName</span></span>
<span data-ttu-id="d6808-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="d6808-116">Azure data share account name</span></span>

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

### <span data-ttu-id="d6808-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6808-117">-DefaultProfile</span></span>
<span data-ttu-id="d6808-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6808-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6808-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6808-119">-Name</span></span>
<span data-ttu-id="d6808-120">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="d6808-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6808-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6808-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6808-122">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="d6808-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d6808-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6808-123">-ResourceId</span></span>
<span data-ttu-id="d6808-124">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="d6808-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="d6808-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6808-125">CommonParameters</span></span>
<span data-ttu-id="d6808-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6808-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6808-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6808-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6808-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6808-128">INPUTS</span></span>

### <span data-ttu-id="d6808-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d6808-129">System.String</span></span>

## <span data-ttu-id="d6808-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6808-130">OUTPUTS</span></span>

### <span data-ttu-id="d6808-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="d6808-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="d6808-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6808-132">NOTES</span></span>

## <span data-ttu-id="d6808-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6808-133">RELATED LINKS</span></span>
