---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732224"
---
# <span data-ttu-id="b8e50-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b8e50-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="b8e50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8e50-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e50-103">Получение сведений об учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8e50-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8e50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8e50-104">SYNTAX</span></span>

### <span data-ttu-id="b8e50-105">Все в подписке (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8e50-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8e50-106">Все в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b8e50-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8e50-107">Конкретный счет</span><span class="sxs-lookup"><span data-stu-id="b8e50-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8e50-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8e50-108">DESCRIPTION</span></span>
<span data-ttu-id="b8e50-109">Командлет **Get-AzureRmDataLakeAnalyticsAccount** получает сведения о учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8e50-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="b8e50-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8e50-110">EXAMPLES</span></span>

### <span data-ttu-id="b8e50-111">Пример 1: получение сведений об учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b8e50-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="b8e50-112">Эта команда получает сведения о учетной записи с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="b8e50-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="b8e50-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8e50-113">PARAMETERS</span></span>

### <span data-ttu-id="b8e50-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8e50-114">-Name</span></span>
<span data-ttu-id="b8e50-115">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8e50-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e50-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e50-116">-ResourceGroupName</span></span>
<span data-ttu-id="b8e50-117">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8e50-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e50-118">-DefaultProfile</span></span>
<span data-ttu-id="b8e50-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e50-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8e50-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e50-120">CommonParameters</span></span>
<span data-ttu-id="b8e50-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8e50-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e50-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e50-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e50-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8e50-123">INPUTS</span></span>

## <span data-ttu-id="b8e50-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8e50-124">OUTPUTS</span></span>

### <span data-ttu-id="b8e50-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b8e50-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="b8e50-126">Указанные данные учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b8e50-126">The specified account details.</span></span>

### <span data-ttu-id="b8e50-127">Список<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="b8e50-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="b8e50-128">Список учетных записей в указанной группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="b8e50-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="b8e50-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8e50-129">NOTES</span></span>

## <span data-ttu-id="b8e50-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8e50-130">RELATED LINKS</span></span>

[<span data-ttu-id="b8e50-131">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b8e50-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b8e50-132">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b8e50-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b8e50-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b8e50-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b8e50-134">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b8e50-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


