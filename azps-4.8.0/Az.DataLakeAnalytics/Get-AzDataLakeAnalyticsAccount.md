---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079710"
---
# <span data-ttu-id="c0db4-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0db4-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="c0db4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0db4-102">SYNOPSIS</span></span>
<span data-ttu-id="c0db4-103">Получение сведений об учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0db4-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c0db4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0db4-104">SYNTAX</span></span>

### <span data-ttu-id="c0db4-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0db4-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0db4-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c0db4-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0db4-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="c0db4-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0db4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0db4-108">DESCRIPTION</span></span>
<span data-ttu-id="c0db4-109">Командлет **Get-AzDataLakeAnalyticsAccount** получает сведения о учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0db4-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c0db4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0db4-110">EXAMPLES</span></span>

### <span data-ttu-id="c0db4-111">Пример 1: получение сведений об учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c0db4-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="c0db4-112">Эта команда получает сведения о учетной записи с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="c0db4-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="c0db4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0db4-113">PARAMETERS</span></span>

### <span data-ttu-id="c0db4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0db4-114">-DefaultProfile</span></span>
<span data-ttu-id="c0db4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0db4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0db4-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0db4-116">-Name</span></span>
<span data-ttu-id="c0db4-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0db4-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c0db4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0db4-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0db4-119">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0db4-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c0db4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0db4-120">CommonParameters</span></span>
<span data-ttu-id="c0db4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0db4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0db4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0db4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0db4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0db4-123">INPUTS</span></span>

### <span data-ttu-id="c0db4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c0db4-124">System.String</span></span>

## <span data-ttu-id="c0db4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0db4-125">OUTPUTS</span></span>

### <span data-ttu-id="c0db4-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0db4-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="c0db4-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="c0db4-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="c0db4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0db4-128">NOTES</span></span>

## <span data-ttu-id="c0db4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0db4-129">RELATED LINKS</span></span>

[<span data-ttu-id="c0db4-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0db4-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c0db4-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0db4-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c0db4-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0db4-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c0db4-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0db4-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


