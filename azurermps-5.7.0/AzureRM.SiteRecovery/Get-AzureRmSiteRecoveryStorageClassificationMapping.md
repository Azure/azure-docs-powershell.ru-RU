---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733973"
---
# <span data-ttu-id="7fce6-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7fce6-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="7fce6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fce6-102">SYNOPSIS</span></span>
<span data-ttu-id="7fce6-103">Получает сопоставление классификации хранилища при восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="7fce6-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fce6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fce6-104">SYNTAX</span></span>

### <span data-ttu-id="7fce6-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fce6-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fce6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7fce6-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fce6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fce6-107">DESCRIPTION</span></span>
<span data-ttu-id="7fce6-108">Командлет **Get-AzureRmSiteRecoveryStorageClassificationMapping** получает сопоставление классификации хранилища в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7fce6-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="7fce6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fce6-109">EXAMPLES</span></span>

## <span data-ttu-id="7fce6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fce6-110">PARAMETERS</span></span>

### <span data-ttu-id="7fce6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fce6-111">-DefaultProfile</span></span>
<span data-ttu-id="7fce6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fce6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fce6-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7fce6-113">-Name</span></span>
<span data-ttu-id="7fce6-114">Указывает имя сопоставления классификации хранилища, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7fce6-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fce6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fce6-115">CommonParameters</span></span>
<span data-ttu-id="7fce6-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fce6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fce6-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fce6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fce6-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fce6-118">INPUTS</span></span>

### <span data-ttu-id="7fce6-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="7fce6-119">None</span></span>
<span data-ttu-id="7fce6-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7fce6-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7fce6-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fce6-121">OUTPUTS</span></span>

### <span data-ttu-id="7fce6-122">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="7fce6-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="7fce6-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fce6-123">NOTES</span></span>

## <span data-ttu-id="7fce6-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fce6-124">RELATED LINKS</span></span>

[<span data-ttu-id="7fce6-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7fce6-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="7fce6-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7fce6-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
