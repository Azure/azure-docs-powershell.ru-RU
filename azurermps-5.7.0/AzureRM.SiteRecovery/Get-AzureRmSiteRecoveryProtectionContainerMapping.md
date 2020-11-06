---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 31887397c6b9b0a3a18a4af3cb4b4faca7c4a91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567907"
---
# <span data-ttu-id="ac17f-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ac17f-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="ac17f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac17f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac17f-103">Получение сопоставлений контейнеров для восстановления сайта Azure site Protection.</span><span class="sxs-lookup"><span data-stu-id="ac17f-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac17f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac17f-104">SYNTAX</span></span>

### <span data-ttu-id="ac17f-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac17f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac17f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ac17f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac17f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac17f-107">DESCRIPTION</span></span>
<span data-ttu-id="ac17f-108">Командлет **Get-AzureRmSiteRecoveryProtectionContainerMapping** получает сведения о контейнере защиты для сопоставлений политик в хранилище.</span><span class="sxs-lookup"><span data-stu-id="ac17f-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="ac17f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac17f-109">EXAMPLES</span></span>

## <span data-ttu-id="ac17f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac17f-110">PARAMETERS</span></span>

### <span data-ttu-id="ac17f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac17f-111">-DefaultProfile</span></span>
<span data-ttu-id="ac17f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac17f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac17f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac17f-113">-Name</span></span>
<span data-ttu-id="ac17f-114">Указывает имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="ac17f-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac17f-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ac17f-115">-ProtectionContainer</span></span>
<span data-ttu-id="ac17f-116">Указывает объект контейнера защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ac17f-116">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac17f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac17f-117">CommonParameters</span></span>
<span data-ttu-id="ac17f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac17f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac17f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac17f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac17f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac17f-120">INPUTS</span></span>

### <span data-ttu-id="ac17f-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ac17f-121">ASRProtectionContainer</span></span>
<span data-ttu-id="ac17f-122">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ac17f-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="ac17f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac17f-123">OUTPUTS</span></span>

### <span data-ttu-id="ac17f-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ac17f-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ac17f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac17f-125">NOTES</span></span>

## <span data-ttu-id="ac17f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac17f-126">RELATED LINKS</span></span>

[<span data-ttu-id="ac17f-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ac17f-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="ac17f-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ac17f-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
