---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 1c8d061dae3d2334b422e6f9e4e3c2b7bb75abcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568291"
---
# <span data-ttu-id="37c44-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="37c44-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="37c44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37c44-102">SYNOPSIS</span></span>
<span data-ttu-id="37c44-103">Получает сопоставление классификации хранилища при восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="37c44-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37c44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37c44-104">SYNTAX</span></span>

### <span data-ttu-id="37c44-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37c44-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37c44-106">ByName</span><span class="sxs-lookup"><span data-stu-id="37c44-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37c44-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37c44-107">DESCRIPTION</span></span>
<span data-ttu-id="37c44-108">Командлет **Get-AzureRmSiteRecoveryStorageClassificationMapping** получает сопоставление классификации хранилища в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="37c44-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="37c44-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37c44-109">EXAMPLES</span></span>

## <span data-ttu-id="37c44-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37c44-110">PARAMETERS</span></span>

### <span data-ttu-id="37c44-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37c44-111">-Name</span></span>
<span data-ttu-id="37c44-112">Указывает имя сопоставления классификации хранилища, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="37c44-112">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c44-113">-DefaultProfile</span></span>
<span data-ttu-id="37c44-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37c44-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37c44-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c44-115">CommonParameters</span></span>
<span data-ttu-id="37c44-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37c44-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c44-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c44-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c44-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37c44-118">INPUTS</span></span>

## <span data-ttu-id="37c44-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37c44-119">OUTPUTS</span></span>

### <span data-ttu-id="37c44-120">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="37c44-120">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="37c44-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="37c44-121">NOTES</span></span>

## <span data-ttu-id="37c44-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37c44-122">RELATED LINKS</span></span>

[<span data-ttu-id="37c44-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="37c44-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="37c44-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="37c44-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
