---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b0390f4ec9ec7c141e7d059c88d7aeb4b9c8507d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721399"
---
# <span data-ttu-id="0459e-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0459e-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0459e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0459e-102">SYNOPSIS</span></span>
<span data-ttu-id="0459e-103">Получение сведений об учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0459e-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0459e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0459e-104">SYNTAX</span></span>

### <span data-ttu-id="0459e-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0459e-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0459e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0459e-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0459e-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="0459e-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0459e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0459e-108">DESCRIPTION</span></span>
<span data-ttu-id="0459e-109">Командлет **Get-AzDataLakeAnalyticsAccount** получает сведения о учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0459e-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0459e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0459e-110">EXAMPLES</span></span>

### <span data-ttu-id="0459e-111">Пример 1: получение сведений об учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0459e-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="0459e-112">Эта команда получает сведения о учетной записи с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="0459e-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="0459e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0459e-113">PARAMETERS</span></span>

### <span data-ttu-id="0459e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0459e-114">-DefaultProfile</span></span>
<span data-ttu-id="0459e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0459e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0459e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0459e-116">-Name</span></span>
<span data-ttu-id="0459e-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0459e-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0459e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0459e-118">-ResourceGroupName</span></span>
<span data-ttu-id="0459e-119">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0459e-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0459e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0459e-120">CommonParameters</span></span>
<span data-ttu-id="0459e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0459e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0459e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0459e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0459e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0459e-123">INPUTS</span></span>

### <span data-ttu-id="0459e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0459e-124">System.String</span></span>

## <span data-ttu-id="0459e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0459e-125">OUTPUTS</span></span>

### <span data-ttu-id="0459e-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0459e-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="0459e-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="0459e-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="0459e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0459e-128">NOTES</span></span>

## <span data-ttu-id="0459e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0459e-129">RELATED LINKS</span></span>

[<span data-ttu-id="0459e-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0459e-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0459e-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0459e-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0459e-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0459e-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0459e-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0459e-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


