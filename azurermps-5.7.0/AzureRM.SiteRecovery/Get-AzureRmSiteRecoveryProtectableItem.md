---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567909"
---
# <span data-ttu-id="91f3b-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="91f3b-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="91f3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="91f3b-103">Получите доступ к защищенным элементам в контейнере защиты.</span><span class="sxs-lookup"><span data-stu-id="91f3b-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91f3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91f3b-104">SYNTAX</span></span>

### <span data-ttu-id="91f3b-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91f3b-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91f3b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="91f3b-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91f3b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="91f3b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91f3b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91f3b-108">DESCRIPTION</span></span>
<span data-ttu-id="91f3b-109">Командлет **Get-AzureRmSiteRecoveryProtectableItem** получает защищенные элементы в контейнере защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="91f3b-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="91f3b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91f3b-110">EXAMPLES</span></span>

## <span data-ttu-id="91f3b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91f3b-111">PARAMETERS</span></span>

### <span data-ttu-id="91f3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f3b-112">-DefaultProfile</span></span>
<span data-ttu-id="91f3b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91f3b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91f3b-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="91f3b-114">-FriendlyName</span></span>
<span data-ttu-id="91f3b-115">Указывает понятное имя защищенного элемента Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="91f3b-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f3b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91f3b-116">-Name</span></span>
<span data-ttu-id="91f3b-117">Указывает имя защищенного элемента Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="91f3b-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="91f3b-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="91f3b-118">-ProtectionContainer</span></span>
<span data-ttu-id="91f3b-119">Указывает объект контейнера защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="91f3b-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="91f3b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f3b-120">CommonParameters</span></span>
<span data-ttu-id="91f3b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91f3b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f3b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f3b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f3b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91f3b-123">INPUTS</span></span>

### <span data-ttu-id="91f3b-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="91f3b-124">ASRProtectionContainer</span></span>
<span data-ttu-id="91f3b-125">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="91f3b-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="91f3b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91f3b-126">OUTPUTS</span></span>

### <span data-ttu-id="91f3b-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="91f3b-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="91f3b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="91f3b-128">NOTES</span></span>

## <span data-ttu-id="91f3b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91f3b-129">RELATED LINKS</span></span>

[<span data-ttu-id="91f3b-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="91f3b-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="91f3b-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="91f3b-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
