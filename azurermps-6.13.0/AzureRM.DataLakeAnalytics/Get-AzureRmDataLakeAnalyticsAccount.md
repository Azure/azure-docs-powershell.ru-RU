---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 32c7478e7e2419a8f83c839efd841f25446a96c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560955"
---
# <span data-ttu-id="d5007-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d5007-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d5007-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5007-102">SYNOPSIS</span></span>
<span data-ttu-id="d5007-103">Получение сведений об учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5007-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5007-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5007-104">SYNTAX</span></span>

### <span data-ttu-id="d5007-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5007-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5007-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d5007-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5007-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="d5007-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5007-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5007-108">DESCRIPTION</span></span>
<span data-ttu-id="d5007-109">Командлет **Get-AzureRmDataLakeAnalyticsAccount** получает сведения о учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5007-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d5007-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5007-110">EXAMPLES</span></span>

### <span data-ttu-id="d5007-111">Пример 1: получение сведений об учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d5007-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d5007-112">Эта команда получает сведения о учетной записи с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="d5007-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="d5007-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5007-113">PARAMETERS</span></span>

### <span data-ttu-id="d5007-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5007-114">-DefaultProfile</span></span>
<span data-ttu-id="d5007-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d5007-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5007-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5007-116">-Name</span></span>
<span data-ttu-id="d5007-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5007-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5007-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5007-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5007-119">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5007-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5007-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5007-120">CommonParameters</span></span>
<span data-ttu-id="d5007-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5007-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5007-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5007-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5007-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5007-123">INPUTS</span></span>

### <span data-ttu-id="d5007-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d5007-124">System.String</span></span>

## <span data-ttu-id="d5007-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5007-125">OUTPUTS</span></span>

### <span data-ttu-id="d5007-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d5007-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d5007-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5007-127">NOTES</span></span>

## <span data-ttu-id="d5007-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5007-128">RELATED LINKS</span></span>

[<span data-ttu-id="d5007-129">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d5007-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d5007-130">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d5007-130">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d5007-131">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d5007-131">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d5007-132">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d5007-132">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


