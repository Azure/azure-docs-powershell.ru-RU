---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561456"
---
# <span data-ttu-id="d4686-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d4686-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="d4686-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4686-102">SYNOPSIS</span></span>
<span data-ttu-id="d4686-103">Создание сопоставления классификации хранилища при восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="d4686-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4686-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4686-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4686-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4686-105">DESCRIPTION</span></span>
<span data-ttu-id="d4686-106">Командлет **New-AzureRmSiteRecoveryStorageClassificationMapping** создает сопоставление классификации хранилища в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4686-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="d4686-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4686-107">EXAMPLES</span></span>

## <span data-ttu-id="d4686-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4686-108">PARAMETERS</span></span>

### <span data-ttu-id="d4686-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4686-109">-DefaultProfile</span></span>
<span data-ttu-id="d4686-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4686-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4686-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d4686-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4686-112">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d4686-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="d4686-113">Задает основное сопоставление классификации хранилища.</span><span class="sxs-lookup"><span data-stu-id="d4686-113">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4686-114">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d4686-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="d4686-115">Указывает сопоставление классификации хранилища для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4686-115">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4686-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4686-116">CommonParameters</span></span>
<span data-ttu-id="d4686-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4686-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4686-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4686-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4686-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4686-119">INPUTS</span></span>

### <span data-ttu-id="d4686-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d4686-120">ASRStorageClassification</span></span>
<span data-ttu-id="d4686-121">Параметр "PrimaryStorageClassification" принимает значение типа "ASRStorageClassification" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d4686-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="d4686-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4686-122">OUTPUTS</span></span>

### <span data-ttu-id="d4686-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d4686-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4686-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4686-124">NOTES</span></span>

## <span data-ttu-id="d4686-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4686-125">RELATED LINKS</span></span>

[<span data-ttu-id="d4686-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d4686-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="d4686-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d4686-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
