---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732380"
---
# <span data-ttu-id="be738-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be738-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="be738-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be738-102">SYNOPSIS</span></span>
<span data-ttu-id="be738-103">Получение сведений об учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be738-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be738-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be738-104">SYNTAX</span></span>

### <span data-ttu-id="be738-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be738-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be738-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be738-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be738-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="be738-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be738-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be738-108">DESCRIPTION</span></span>
<span data-ttu-id="be738-109">Командлет **Get-AzureRmDataLakeAnalyticsAccount** получает сведения о учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be738-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="be738-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be738-110">EXAMPLES</span></span>

### <span data-ttu-id="be738-111">Пример 1: получение сведений об учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="be738-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="be738-112">Эта команда получает сведения о учетной записи с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="be738-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="be738-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be738-113">PARAMETERS</span></span>

### <span data-ttu-id="be738-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be738-114">-DefaultProfile</span></span>
<span data-ttu-id="be738-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="be738-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be738-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be738-116">-Name</span></span>
<span data-ttu-id="be738-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be738-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be738-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be738-118">-ResourceGroupName</span></span>
<span data-ttu-id="be738-119">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be738-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be738-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be738-120">CommonParameters</span></span>
<span data-ttu-id="be738-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be738-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be738-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be738-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be738-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be738-123">INPUTS</span></span>

### <span data-ttu-id="be738-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="be738-124">None</span></span>
<span data-ttu-id="be738-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="be738-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be738-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be738-126">OUTPUTS</span></span>

### <span data-ttu-id="be738-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be738-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="be738-128">Указанные данные учетной записи.</span><span class="sxs-lookup"><span data-stu-id="be738-128">The specified account details.</span></span>

### <span data-ttu-id="be738-129">Список<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="be738-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="be738-130">Список учетных записей в указанной группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="be738-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="be738-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="be738-131">NOTES</span></span>

## <span data-ttu-id="be738-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be738-132">RELATED LINKS</span></span>

[<span data-ttu-id="be738-133">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be738-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="be738-134">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be738-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="be738-135">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be738-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="be738-136">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be738-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


