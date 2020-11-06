---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2d215afda7c2c26aa178421fb52ddaff8c6ac831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566093"
---
# <span data-ttu-id="dcbae-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="dcbae-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="dcbae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcbae-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbae-103">Удаляет сопоставление классификации хранилища из восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="dcbae-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcbae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcbae-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcbae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcbae-105">DESCRIPTION</span></span>
<span data-ttu-id="dcbae-106">Командлет **Remove-AzureRmSiteRecoveryStorageClassificationMapping** удаляет сопоставление классификации хранилища из Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dcbae-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="dcbae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcbae-107">EXAMPLES</span></span>

## <span data-ttu-id="dcbae-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcbae-108">PARAMETERS</span></span>

### <span data-ttu-id="dcbae-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbae-109">-DefaultProfile</span></span>
<span data-ttu-id="dcbae-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcbae-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcbae-111">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="dcbae-111">-StorageClassificationMapping</span></span>
<span data-ttu-id="dcbae-112">Указывает сопоставление классификаций хранилища, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dcbae-112">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbae-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbae-113">CommonParameters</span></span>
<span data-ttu-id="dcbae-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcbae-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbae-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcbae-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbae-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcbae-116">INPUTS</span></span>

### <span data-ttu-id="dcbae-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="dcbae-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="dcbae-118">Параметр "StorageClassificationMapping" принимает значение типа "ASRStorageClassificationMapping" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dcbae-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="dcbae-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcbae-119">OUTPUTS</span></span>

### <span data-ttu-id="dcbae-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dcbae-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dcbae-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcbae-121">NOTES</span></span>

## <span data-ttu-id="dcbae-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcbae-122">RELATED LINKS</span></span>

[<span data-ttu-id="dcbae-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="dcbae-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="dcbae-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="dcbae-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
