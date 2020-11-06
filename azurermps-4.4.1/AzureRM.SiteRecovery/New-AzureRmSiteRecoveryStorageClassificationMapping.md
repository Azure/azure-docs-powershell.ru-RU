---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2520dd90eed1362f4d499eb88ce88dec33f1338c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559495"
---
# <span data-ttu-id="624c6-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="624c6-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="624c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="624c6-102">SYNOPSIS</span></span>
<span data-ttu-id="624c6-103">Создание сопоставления классификации хранилища при восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="624c6-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="624c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="624c6-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="624c6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="624c6-105">DESCRIPTION</span></span>
<span data-ttu-id="624c6-106">Командлет **New-AzureRmSiteRecoveryStorageClassificationMapping** создает сопоставление классификации хранилища в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="624c6-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="624c6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="624c6-107">EXAMPLES</span></span>

## <span data-ttu-id="624c6-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="624c6-108">PARAMETERS</span></span>

### <span data-ttu-id="624c6-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="624c6-109">-Name</span></span>
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

### <span data-ttu-id="624c6-110">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="624c6-110">-PrimaryStorageClassification</span></span>
<span data-ttu-id="624c6-111">Задает основное сопоставление классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="624c6-111">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="624c6-112">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="624c6-112">-RecoveryStorageClassification</span></span>
<span data-ttu-id="624c6-113">Указывает сопоставление классификации хранилища для восстановления.</span><span class="sxs-lookup"><span data-stu-id="624c6-113">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="624c6-114">-DefaultProfile</span></span>
<span data-ttu-id="624c6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="624c6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="624c6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="624c6-116">CommonParameters</span></span>
<span data-ttu-id="624c6-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="624c6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="624c6-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="624c6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="624c6-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="624c6-119">INPUTS</span></span>

### <span data-ttu-id="624c6-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="624c6-120">ASRStorageClassification</span></span>
<span data-ttu-id="624c6-121">Параметр "PrimaryStorageClassification" принимает значение типа "ASRStorageClassification" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="624c6-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="624c6-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="624c6-122">OUTPUTS</span></span>

### <span data-ttu-id="624c6-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="624c6-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="624c6-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="624c6-124">NOTES</span></span>

## <span data-ttu-id="624c6-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="624c6-125">RELATED LINKS</span></span>

[<span data-ttu-id="624c6-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="624c6-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="624c6-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="624c6-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
